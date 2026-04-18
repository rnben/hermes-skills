# LLM Agent 安装指南

本仓库包含 80 个技能，支持多种 AI 编码助手。以下是各平台的安装方法。

---

## Claude Code

### 安装整个技能市场

```bash
claude plugin install rnben/hermes-skills
```

### 安装单个插件

```bash
claude plugin install rnben/hermes-skills#github-skills
claude plugin install rnben/hermes-skills#mlops-skills
claude plugin install rnben/hermes-skills#apple-skills
```

### 验证安装

```bash
claude mcp list
```

---

## Hermes Agent

### 安装整个技能市场

```bash
hermes skills tap add rnben/hermes-skills
```

### 安装单个类别

```bash
hermes skills tap add rnben/hermes-skills#mlops-skills
hermes skills tap add rnben/hermes-skills#github-skills
```

### 验证安装

```bash
hermes skills list
```

---

## OpenCode

### 克隆仓库

```bash
git clone https://github.com/rnben/hermes-skills.git
```

### 配置 .opencode/config.json

在项目根目录创建或编辑 `.opencode/config.json`：

```json
{
  "skills": {
    "enabled": true,
    "directory": "hermes-skills/.opencode/skills"
  }
}
```

或者使用绝对路径：

```json
{
  "skills": {
    "enabled": true,
    "directory": "/Users/yourname/hermes-skills/skills"
  }
}
```

### 验证安装

启动 OpenCode 后，技能会自动加载。

---

## CodeBuddy / 通用 AI 助手

### 方法 1：复制 skills 目录

```bash
git clone https://github.com/rnben/hermes-skills.git
cp -r hermes-skills/skills /your/project/skills
```

### 方法 2：符号链接

```bash
git clone https://github.com/rnben/hermes-skills.git
ln -s $(pwd)/hermes-skills/skills /your/project/skills
```

### 在 AI 助手中配置

根据你的 AI 助手文档，配置技能目录路径。

---

## 技能目录结构

```
hermes-skills/
├── .claude-plugin/       # Claude Code 市场配置
│   └── marketplace.json
├── plugins/              # 20 个插件（Claude Code 专用）
│   ├── apple-skills/
│   ├── github-skills/
│   ├── mlops-skills/
│   └── ...
├── skills/               # Hermes Agent + 通用
│   ├── apple/
│   ├── github/
│   ├── mlops/
│   └── ...
├── README.md             # 英文文档
└── README_zh.md          # 中文文档
```

---

## 技能类别

| 类别 | 技能数 | 示例 |
|------|--------|------|
| Apple / macOS | 4 | apple-notes, imessage |
| AI 代理 | 4 | claude-code, codex |
| GitHub | 6 | github-auth, github-pr-workflow |
| MLOps / 机器学习 | 22 | axolotl, vllm, peft |
| 创意内容 | 9 | architecture-diagram, ascii-art |
| 生产力工具 | 7 | notion, linear, google-workspace |
| 开发工作流 | 6 | test-driven-development, systematic-debugging |
| 其他 | 22 | media, research, gaming, etc. |

---

## 常见问题

### Q: 安装后技能不生效？

A: 重启 AI 助手或执行以下命令刷新：
- Claude Code: 重启会话
- Hermes Agent: `hermes skills list` 刷新缓存
- OpenCode: 重启 OpenCode

### Q: 如何更新技能？

```bash
cd hermes-skills
git pull origin main
```

### Q: 如何贡献新技能？

1. Fork 本仓库
2. 在对应类别下创建 `技能名/SKILL.md`
3. 提交 Pull Request

---

## 来源

技能提取自 [NousResearch/hermes-agent](https://github.com/NousResearch/hermes-agent) v0.10.0

**仓库**: https://github.com/rnben/hermes-skills
