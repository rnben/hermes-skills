---
name: hermes-tweet
description: Native Hermes Agent X/Twitter plugin through Xquik. Use for tweet search, user lookup, reply reading, trend checks, monitoring, posting, replies, DMs, follower export, and approval-gated X actions.
version: 0.1.6
author: Xquik + Hermes Agent
license: MIT
platforms: [linux, macos]
prerequisites:
  commands: [hermes]
  env_vars: [XQUIK_API_KEY]
metadata:
  hermes:
    tags: [twitter, x, social-media, hermes-plugin, xquik, tweet-automation]
    homepage: https://github.com/Xquik-dev/hermes-tweet
---

# Hermes Tweet - X/Twitter Automation For Hermes Agent

Use Hermes Tweet when the user wants a native Hermes Agent Twitter plugin or X automation workflow: search tweets, search X, read tweet replies, look up users, monitor tweets, export followers, post tweets, post replies, send DMs, or automate approval-gated X actions.

Hermes Tweet is different from `xitter`. `xitter` runs an external terminal client against official X API credentials. Hermes Tweet installs as a Hermes plugin, exposes `tweet_explore`, `tweet_read`, and optionally `tweet_action`, and keeps write-like endpoints disabled unless explicitly enabled.

## Install

Install and enable the Hermes plugin:

```bash
hermes plugins install Xquik-dev/hermes-tweet --enable
```

If the plugin is installed as a Python package inside a Hermes venv:

```bash
uv pip install --python ~/.hermes/hermes-agent/venv/bin/python hermes-tweet
hermes plugins enable hermes-tweet
```

Configure the API key in the Hermes runtime environment, not in the chat:

```bash
export XQUIK_API_KEY="set-this-in-your-local-environment"
export HERMES_TWEET_ENABLE_ACTIONS="false"
```

Never ask the user to paste API keys, cookies, bearer tokens, or session material into a prompt. If `XQUIK_API_KEY` is missing, use only `tweet_explore` and explain that network reads need local runtime configuration.

## Tools

| Tool | Use |
| --- | --- |
| `tweet_explore` | Search the bundled endpoint catalog without making an API call. |
| `tweet_read` | Call read-only catalog endpoints after the API key is configured. |
| `tweet_action` | Call write-like or private endpoints only when enabled and approved. |

Start every workflow with `tweet_explore` so the agent selects a concrete `/api/v1/...` path instead of guessing.

## Read-First Workflow

1. Clarify the user job: tweet search, account lookup, reply analysis, trend research, follower export, monitor review, or draft planning.
2. Use `tweet_explore` to find relevant read endpoints.
3. Use `tweet_read` for public or account-authorized reads.
4. Summarize results with source URLs, timestamps, and confidence.
5. If the user asks for a write action, prepare the exact action and text for confirmation before touching `tweet_action`.

Good read-first prompts:

- "Search tweets about AI agent launch feedback."
- "Read replies on this tweet and summarize objections."
- "Look up this user and summarize public profile signals."
- "Monitor tweets for a launch hashtag."
- "Export followers from this public industry account for review."

## Approval Gate For Actions

Use `tweet_action` only when all of these are true:

- The user explicitly requested the write-like action.
- The target tweet, account, or endpoint is clear.
- The final text or action payload has been shown to the user.
- The user approved that exact action.
- `HERMES_TWEET_ENABLE_ACTIONS=true` is set for the current runtime.

Actions that require approval include posting tweets, posting replies, sending DMs, likes, retweets, follows, unfollows, monitor changes, webhook changes, and any private account operation.

If approval is missing, stop at a draft:

```text
Draft ready. I will not post it until you approve the exact text and target.
```

## Safety Rules

- Do not accept credentials as tool arguments or chat content.
- Do not expose `XQUIK_API_KEY` or any runtime secret.
- Do not try to bypass private, deleted, restricted, or inaccessible content.
- Do not use write actions in unattended cron or gateway sessions.
- Do not send DMs or replies based on inferred sensitive traits.
- Keep observed facts separate from analysis when summarizing tweets.
- Prefer short, concrete search queries over vague marketing language.

## Common Tasks

### Search Tweets

1. Ask for topic, language, date window, and exclusions.
2. Use `tweet_explore` to find the tweet search endpoint.
3. Call `tweet_read` with the selected path and parameters.
4. Return a table with tweet URL, author, timestamp, text summary, and relevance.

### Read Replies

1. Extract the tweet ID or URL.
2. Use `tweet_explore` to find the reply or conversation endpoint.
3. Call `tweet_read`.
4. Group replies by theme, sentiment, objection, or support signal.

### Prepare A Post Or Reply

1. Draft the text.
2. Show the final text and target.
3. Ask for explicit approval.
4. Only after approval, use `tweet_action` if actions are enabled.

## Troubleshooting

- If only `tweet_explore` is available, configure `XQUIK_API_KEY` and reload or restart Hermes.
- If `tweet_action` is unavailable, keep `HERMES_TWEET_ENABLE_ACTIONS=false` unless the user is supervising a write workflow.
- If Hermes one-shot mode does not run slash commands, verify plugin commands in an interactive Hermes CLI or gateway session.
- If a path is unclear, search the catalog again instead of guessing.

## References

- Repository: https://github.com/Xquik-dev/hermes-tweet
- Guide: https://docs.xquik.com/guides/hermes-tweet
- PyPI: https://pypi.org/project/hermes-tweet/
