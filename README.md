# Hermes Skills

> A curated collection of **80 skills** organized into **20 plugins** for AI coding agents.

> **Source:** Skills extracted from [NousResearch/hermes-agent](https://github.com/NousResearch/hermes-agent) v0.10.0

[中文版](README_zh.md)

## Install

### Claude Code
```bash
claude plugin install rnben/hermes-skills
claude plugin install rnben/hermes-skills#github-skills  # individual plugin
```

### Hermes Agent
```bash
hermes skills tap add rnben/hermes-skills
hermes skills tap add rnben/hermes-skills#mlops-skills  # individual category
```

### OpenCode / Generic
```bash
git clone https://github.com/rnben/hermes-skills.git
# OpenCode: Add to .opencode/config.json:
# { "skills": { "enabled": true, "directory": "hermes-skills/.opencode/skills" } }
# Generic: Copy skills/ folder to your project
```

## All Skills

| # | Skill | Description | Project |
|---|-------|-------------|---------|
| 1 | `apple-notes` | Manage Apple Notes via memo CLI | https://github.com/sindresorhus/memo-cli |
| 2 | `apple-reminders` | Manage Apple Reminders via remindctl | https://github.com/steipete/remindctl |
| 3 | `findmy` | Track Apple devices and AirTags | https://developer.apple.com/find-my/ |
| 4 | `imessage` | Send/receive iMessages/SMS | https://github.com/steipete/tap |
| 5 | `claude-code` | Delegate tasks to Claude Code CLI | https://docs.anthropic.com/en/docs/claude-code |
| 6 | `codex` | Delegate tasks to OpenAI Codex CLI | https://github.com/openai/codex |
| 7 | `hermes-agent` | Hermes Agent full guide | https://github.com/NousResearch/hermes-agent |
| 8 | `opencode` | Delegate tasks to OpenCode CLI | https://opencode.ai |
| 9 | `architecture-diagram` | Dark-themed SVG architecture diagrams | https://github.com/Cocoon-AI/architecture-diagram-generator |
| 10 | `ascii-art` | Generate ASCII art (571 fonts) | https://github.com/jasonbrown20599/pyfiglet |
| 11 | `ascii-video` | Convert media to colored ASCII video | https://github.com/NousResearch/hermes-agent |
| 12 | `creative-ideation` | Generate project ideas via constraints | https://github.com/NousResearch/hermes-agent |
| 13 | `excalidraw` | Hand-drawn style diagrams | https://excalidraw.com |
| 14 | `manim-video` | Math/tech animations (Manim) | https://github.com/ManimCommunity/manim |
| 15 | `p5js` | Interactive generative visual art | https://p5js.org |
| 16 | `popular-web-designs` | 54 design systems from real sites | https://github.com/NousResearch/hermes-agent |
| 17 | `songwriting-and-ai-music` | Songwriting + AI music | https://github.com/NousResearch/hermes-agent |
| 18 | `jupyter-live-kernel` | Stateful Python via Jupyter kernel | https://github.com/hamelsmu/hamelnb |
| 19 | `webhook-subscriptions` | Webhook subscriptions for events | https://github.com/NousResearch/hermes-agent |
| 20 | `dogfood` | Systematic QA testing of web apps | https://github.com/NousResearch/hermes-agent |
| 21 | `himalaya` | IMAP/SMTP email management CLI | https://github.com/pimalaya/himalaya |
| 22 | `minecraft-modpack-server` | Modded Minecraft server setup | https://github.com/NousResearch/hermes-agent |
| 23 | `pokemon-player` | Auto-play Pokemon via emulation | https://github.com/NousResearch/hermes-agent |
| 24 | `codebase-inspection` | Codebase stats: LOC, language breakdown | https://github.com/ramonhdez/pygount |
| 25 | `github-auth` | GitHub authentication (HTTPS/SSH/gh) | https://docs.github.com/en/authentication |
| 26 | `github-code-review` | Analyze git diffs for code review | https://docs.github.com/en/pull-requests/review |
| 27 | `github-issues` | Create, manage, close GitHub issues | https://docs.github.com/en/issues |
| 28 | `github-pr-workflow` | Full PR lifecycle: branch to merge | https://docs.github.com/en/pull-requests |
| 29 | `github-repo-management` | Clone, create, fork, manage repos | https://docs.github.com/en/repositories |
| 30 | `find-nearby` | Find nearby places via OSM | https://www.openstreetmap.org |
| 31 | `mcporter` | MCP server management CLI | https://mcporter.dev |
| 32 | `native-mcp` | Built-in MCP client | https://modelcontextprotocol.io |
| 33 | `gif-search` | Search/download GIFs from Tenor | https://tenor.com |
| 34 | `heartmula` | Open-source music generation | https://github.com/nateraw/heartmula |
| 35 | `songsee` | Audio spectrograms and visualization | https://github.com/steipete/songsee |
| 36 | `youtube-content` | YouTube transcript extraction | https://github.com/NousResearch/hermes-agent |
| 37 | `audiocraft` | Text-to-music/sound generation | https://github.com/facebookresearch/audiocraft |
| 38 | `axolotl` | LLM fine-tuning (100+ models) | https://github.com/OpenAccess-AI-Collective/axolotl |
| 39 | `clip` | Vision-language zero-shot model | https://github.com/openai/CLIP |
| 40 | `dspy` | Declarative AI systems via DSPy | https://github.com/stanfordnlp/dspy |
| 41 | `gguf` | GGUF/llama.cpp quantization | https://github.com/ggerganov/llama.cpp |
| 42 | `grpo-rl-training` | GRPO/RL fine-tuning with TRL | https://github.com/huggingface/trl |
| 43 | `guidance` | Constrained LLM output via regex | https://github.com/guidance-ai/guidance |
| 44 | `huggingface-hub` | Hugging Face Hub CLI | https://huggingface.co |
| 45 | `llama-cpp` | LLM inference on CPU/Apple Silicon | https://github.com/ggerganov/llama.cpp |
| 46 | `lm-evaluation-harness` | Evaluate LLMs on 60+ benchmarks | https://github.com/EleutherAI/lm-evaluation-harness |
| 47 | `modal` | Serverless GPU cloud for ML | https://modal.com |
| 48 | `obliteratus` | Remove refusal behaviors from LLMs | https://github.com/gwpl/obliteratus |
| 49 | `outlines` | Guaranteed JSON/XML/code generation | https://github.com/dottxt-ai/outlines |
| 50 | `peft` | LoRA/QLoRA efficient fine-tuning | https://github.com/huggingface/peft |
| 51 | `pytorch-fsdp` | PyTorch FSDP training guide | https://pytorch.org/docs/stable/fsdp.html |
| 52 | `segment-anything` | Image segmentation foundation model | https://github.com/facebookresearch/segment-anything |
| 53 | `stable-diffusion` | Text-to-image generation | https://github.com/huggingface/diffusers |
| 54 | `trl-fine-tuning` | SFT/DPO/PPO/GRPO fine-tuning | https://github.com/huggingface/trl |
| 55 | `unsloth` | Fast fine-tuning (2-5x faster) | https://github.com/unslothai/unsloth |
| 56 | `vllm` | High-throughput LLM serving | https://github.com/vllm-project/vllm |
| 57 | `weights-and-biases` | ML experiment tracking and sweeps | https://wandb.ai |
| 58 | `whisper` | Speech recognition, 99 languages | https://github.com/openai/whisper |
| 59 | `obsidian` | Read/search Obsidian notes | https://obsidian.md |
| 60 | `feishu-content-extraction` | Extract Feishu blog articles | https://github.com/NousResearch/hermes-agent |
| 61 | `google-workspace` | Gmail/Drive/Sheets/Docs integration | https://github.com/NousResearch/hermes-agent |
| 62 | `linear` | Manage Linear issues via GraphQL | https://linear.app |
| 63 | `nano-pdf` | Edit PDFs with natural language | https://pypi.org/project/nano-pdf/ |
| 64 | `notion` | Notion pages/databases API | https://developers.notion.com |
| 65 | `ocr-and-documents` | Extract text from PDFs/scans | https://github.com/pymupdf/PyMuPDF |
| 66 | `powerpoint` | Create and handle PPTX | https://python-pptx.readthedocs.io |
| 67 | `godmode` | LLM jailbreak via G0DM0D3 | https://github.com/NousResearch/hermes-agent |
| 68 | `arxiv` | Search arXiv academic papers | https://arxiv.org |
| 69 | `blogwatcher` | Monitor blogs and RSS feeds | https://github.com/JulienTant/blogwatcher-cli |
| 70 | `llm-wiki` | Interlinked Markdown knowledge base | https://github.com/karpathy/llm-wiki |
| 71 | `polymarket` | Polymarket prediction data | https://polymarket.com |
| 72 | `research-paper-writing` | End-to-end ML/AI paper writing | https://github.com/NousResearch/hermes-agent |
| 73 | `openhue` | Philips Hue light control | https://www.openhue.io/cli |
| 74 | `xitter` | X/Twitter terminal client | https://github.com/Infatoshi/x-cli |
| 75 | `plan` | Plan mode: inspect and write plan | https://github.com/NousResearch/hermes-agent |
| 76 | `requesting-code-review` | Pre-commit security + quality scan | https://github.com/NousResearch/hermes-agent |
| 77 | `subagent-driven-development` | Subagent dispatch + 2-stage review | https://github.com/NousResearch/hermes-agent |
| 78 | `systematic-debugging` | 4-phase root cause investigation | https://github.com/NousResearch/hermes-agent |
| 79 | `test-driven-development` | TDD RED-GREEN-REFACTOR cycle | https://github.com/NousResearch/hermes-agent |
| 80 | `writing-plans` | Multi-step implementation plans | https://github.com/NousResearch/hermes-agent |

---

## Directory Structure

```
hermes-skills/
├── .claude-plugin/       # Claude Code marketplace
├── skills/               # Hermes Agent + generic
├── README.md             # This file
└── README_zh.md          # Chinese version
```

## License

MIT
