# Hermes 技能

> 为 AI 编码助手整理的 **80 个技能**，组织为 **20 个插件**。

> **来源：** 技能提取自 [NousResearch/hermes-agent](https://github.com/NousResearch/hermes-agent) v0.10.0

[English](README.md)

## 安装

### Claude Code
```bash
claude plugin install rnben/hermes-skills
claude plugin install rnben/hermes-skills#github-skills  # 单个插件
```

### Hermes Agent
```bash
hermes skills tap add rnben/hermes-skills
hermes skills tap add rnben/hermes-skills#mlops-skills  # 单个类别
```

### OpenCode / 通用
```bash
git clone https://github.com/rnben/hermes-skills.git
# OpenCode: 在 .opencode/config.json 中添加:
# { "skills": { "enabled": true, "directory": "hermes-skills/.opencode/skills" } }
# 通用：复制 skills/ 文件夹到你的项目
```

## 全部技能

| 序号 | 技能 | 描述 | 项目 |
|------|------|------|------|
| 1 | `apple-notes` | 管理 Apple 备忘录 | https://github.com/sindresorhus/memo-cli |
| 2 | `apple-reminders` | 管理 Apple 提醒事项 | https://github.com/steipete/remindctl |
| 3 | `findmy` | 追踪 Apple 设备和 AirTag | https://developer.apple.com/find-my/ |
| 4 | `imessage` | 发送/接收 iMessage/SMS | https://github.com/steipete/tap |
| 5 | `claude-code` | 委托任务给 Claude Code | https://docs.anthropic.com/en/docs/claude-code |
| 6 | `codex` | 委托任务给 OpenAI Codex | https://github.com/openai/codex |
| 7 | `hermes-agent` | Hermes Agent 完整指南 | https://github.com/NousResearch/hermes-agent |
| 8 | `opencode` | 委托任务给 OpenCode CLI | https://opencode.ai |
| 9 | `architecture-diagram` | 深色主题 SVG 架构图 | https://github.com/Cocoon-AI/architecture-diagram-generator |
| 10 | `ascii-art` | 生成 ASCII 艺术 | https://github.com/jasonbrown20599/pyfiglet |
| 11 | `ascii-video` | 将媒体转为 ASCII 视频 | https://github.com/NousResearch/hermes-agent |
| 12 | `creative-ideation` | 通过创意约束生成灵感 | https://github.com/NousResearch/hermes-agent |
| 13 | `excalidraw` | 手绘风格图表 | https://excalidraw.com |
| 14 | `manim-video` | 数学/技术动画 | https://github.com/ManimCommunity/manim |
| 15 | `p5js` | 交互式视觉艺术 | https://p5js.org |
| 16 | `popular-web-designs` | 54 个真实网站设计系统 | https://github.com/NousResearch/hermes-agent |
| 17 | `songwriting-and-ai-music` | 歌曲创作和 AI 音乐 | https://github.com/NousResearch/hermes-agent |
| 18 | `jupyter-live-kernel` | 通过 Jupyter 内核迭代 Python | https://github.com/hamelsmu/hamelnb |
| 19 | `webhook-subscriptions` | Webhook 订阅 | https://github.com/NousResearch/hermes-agent |
| 20 | `dogfood` | Web 应用自动化测试 | https://github.com/NousResearch/hermes-agent |
| 21 | `himalaya` | 终端邮件管理 | https://github.com/pimalaya/himalaya |
| 22 | `minecraft-modpack-server` | 模组 Minecraft 服务器 | https://github.com/NousResearch/hermes-agent |
| 23 | `pokemon-player` | 自动玩 Pokemon | https://github.com/NousResearch/hermes-agent |
| 24 | `codebase-inspection` | 代码库统计 | https://github.com/ramonhdez/pygount |
| 25 | `github-auth` | GitHub 认证 | https://docs.github.com/en/authentication |
| 26 | `github-code-review` | 代码审查 | https://docs.github.com/en/pull-requests/review |
| 27 | `github-issues` | 管理 GitHub issues | https://docs.github.com/en/issues |
| 28 | `github-pr-workflow` | PR 完整工作流 | https://docs.github.com/en/pull-requests |
| 29 | `github-repo-management` | GitHub 仓库管理 | https://docs.github.com/en/repositories |
| 30 | `find-nearby` | 查找附近地点 | https://www.openstreetmap.org |
| 31 | `mcporter` | MCP 服务器管理 | https://mcporter.dev |
| 32 | `native-mcp` | 内置 MCP 客户端 | https://modelcontextprotocol.io |
| 33 | `gif-search` | Tenor GIF 搜索 | https://tenor.com |
| 34 | `heartmula` | 开源音乐生成 | https://github.com/nateraw/heartmula |
| 35 | `songsee` | 音频频谱分析 | https://github.com/steipete/songsee |
| 36 | `youtube-content` | YouTube 字幕提取 | https://github.com/NousResearch/hermes-agent |
| 37 | `audiocraft` | 文本转音乐/音效 | https://github.com/facebookresearch/audiocraft |
| 38 | `axolotl` | LLM 微调（100+ 模型） | https://github.com/OpenAccess-AI-Collective/axolotl |
| 39 | `clip` | 视觉 - 语言模型 | https://github.com/openai/CLIP |
| 40 | `dspy` | 声明式 AI 系统 | https://github.com/stanfordnlp/dspy |
| 41 | `gguf` | GGUF/llama.cpp 量化 | https://github.com/ggerganov/llama.cpp |
| 42 | `grpo-rl-training` | GRPO/RL 微调 | https://github.com/huggingface/trl |
| 43 | `guidance` | 约束 LLM 输出格式 | https://github.com/guidance-ai/guidance |
| 44 | `huggingface-hub` | Hugging Face Hub CLI | https://huggingface.co |
| 45 | `llama-cpp` | CPU/Apple Silicon LLM 推理 | https://github.com/ggerganov/llama.cpp |
| 46 | `lm-evaluation-harness` | 60+ LLM 基准评估 | https://github.com/EleutherAI/lm-evaluation-harness |
| 47 | `modal` | 无服务器 GPU 云 | https://modal.com |
| 48 | `obliteratus` | 移除 LLM 拒绝行为 | https://github.com/gwpl/obliteratus |
| 49 | `outlines` | 结构化 JSON/XML/代码输出 | https://github.com/dottxt-ai/outlines |
| 50 | `peft` | LoRA/QLoRA 高效微调 | https://github.com/huggingface/peft |
| 51 | `pytorch-fsdp` | PyTorch FSDP 训练 | https://pytorch.org/docs/stable/fsdp.html |
| 52 | `segment-anything` | 图像分割基础模型 | https://github.com/facebookresearch/segment-anything |
| 53 | `stable-diffusion` | 文本转图像生成 | https://github.com/huggingface/diffusers |
| 54 | `trl-fine-tuning` | SFT/DPO/PPO 微调 | https://github.com/huggingface/trl |
| 55 | `unsloth` | 快速微调（快 2-5 倍） | https://github.com/unslothai/unsloth |
| 56 | `vllm` | 高性能 LLM 部署 | https://github.com/vllm-project/vllm |
| 57 | `weights-and-biases` | ML 实验追踪 | https://wandb.ai |
| 58 | `whisper` | 语音识别（99 种语言） | https://github.com/openai/whisper |
| 59 | `obsidian` | 读取/创建 Obsidian 笔记 | https://obsidian.md |
| 60 | `feishu-content-extraction` | 飞书博客提取 | https://github.com/NousResearch/hermes-agent |
| 61 | `google-workspace` | Gmail/Drive/Docs 集成 | https://github.com/NousResearch/hermes-agent |
| 62 | `linear` | 管理 Linear issue/项目 | https://linear.app |
| 63 | `nano-pdf` | 自然语言编辑 PDF | https://pypi.org/project/nano-pdf/ |
| 64 | `notion` | Notion 页面/数据库 API | https://developers.notion.com |
| 65 | `ocr-and-documents` | PDF/扫描件文字提取 | https://github.com/pymupdf/PyMuPDF |
| 66 | `powerpoint` | PPTX 创建和处理 | https://python-pptx.readthedocs.io |
| 67 | `godmode` | LLM 越狱（G0DM0D3） | https://github.com/NousResearch/hermes-agent |
| 68 | `arxiv` | 搜索 arXiv 论文 | https://arxiv.org |
| 69 | `blogwatcher` | 监控博客/RSS | https://github.com/JulienTant/blogwatcher-cli |
| 70 | `llm-wiki` | Markdown 知识库 | https://github.com/karpathy/llm-wiki |
| 71 | `polymarket` | 预测市场数据 | https://polymarket.com |
| 72 | `research-paper-writing` | ML/AI 论文写作流程 | https://github.com/NousResearch/hermes-agent |
| 73 | `openhue` | Philips Hue 灯光控制 | https://www.openhue.io/cli |
| 74 | `xitter` | X/Twitter 终端客户端 | https://github.com/Infatoshi/x-cli |
| 75 | `plan` | 计划模式 | https://github.com/NousResearch/hermes-agent |
| 76 | `requesting-code-review` | 提交前安全审查 | https://github.com/NousResearch/hermes-agent |
| 77 | `subagent-driven-development` | 子代理两阶段审查 | https://github.com/NousResearch/hermes-agent |
| 78 | `systematic-debugging` | 4 阶段根因分析 | https://github.com/NousResearch/hermes-agent |
| 79 | `test-driven-development` | TDD 红绿重构 | https://github.com/NousResearch/hermes-agent |
| 80 | `writing-plans` | 多步任务规划 | https://github.com/NousResearch/hermes-agent |

---

## 目录结构

```
hermes-skills/
├── .claude-plugin/       # Claude Code 市场
├── skills/               # Hermes Agent + 通用
├── README.md             # 英文文档
└── README_zh.md          # 中文文档
```

## 许可证

MIT
