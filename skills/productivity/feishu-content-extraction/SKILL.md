---
name: feishu-content-extraction
description: Extract and parse content from Feishu/Hera blog articles when the browser tool times out. Use curl to pull HTML and embedded JSON.
---

# Feishu Content Extraction

## When to use
User asks to extract, summarize, or process content from a Feishu/Hera blog article URL (e.g., `https://www.feishu.cn/content/article/XXXXX`).

## Problem
Feishu pages are heavily JS-rendered. The `browser_navigate` tool will **time out** trying to load them.

## Approach

### Step 1: curl + extract from HTML
```
curl -s -L -A "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/120.0.0.0 Safari/537.36" "FEISHU_URL" 2>/dev/null
```

The article content is embedded as JSON in `window._defaultTemplateValue` and `window._templateValue` in the HTML. Key fields:
- `window._defaultTemplateValue` — contains `text`, `title`, `description`, `keywords` in the top-level page template
- `window._templateValue` — contains `richtext.content` (JSON-escaped string with Quill delta ops) and `articleTitle`, `description`, `keywords`

### Step 2: Parse the content
- The `text` field in `_defaultTemplateValue` often contains raw text directly usable for summary
- The `richtext.content` in `_templateValue` contains Quill delta format JSON — `{ops: [...]}` with rich text operations. For detailed extraction, parse these ops by looking at each `insert` field and combining with attributes (bold, heading, etc.)

### Step 3: Summarize
Once you have the text content, extract key sections, headings, and important points. Present as structured summary.

## Pitfalls
- **Never use `browser_navigate`** for Feishu `/content/article/` URLs — it will timeout (JS bundle is ~1.2MB)
- `curl` response is large (~1.2MB) — use grep or python to extract the specific JSON sections
- The embedded JSON uses escaped quotes (`\\\"`) — handle escaping carefully when parsing
- Some content uses Quill delta format (not plain markdown) — you'll need to interpret the ops for full fidelity
