# Claude Toolkit

> Claude Code 通用工具集 —— 跨项目复用的 skills、agents、rules 及辅助配置。

## 📁 目录结构

```
claude-toolkit/
├── .claude/
│   ├── agents/          # 自定义 Agent 定义
│   ├── skills/          # 自定义 Skills
│   ├── rules/           # 通用 Rules（跨项目共享规则）
│   └── settings.json    # 共享配置（不含敏感信息）
├── .gitignore
└── README.md
```

## 🚀 使用方式

### 方式一：符号链接（推荐）

将本仓库克隆到固定位置，在其它项目中通过符号链接引用：

```bash
git clone https://github.com/a60717937/claude-toolkit.git ~/claude-toolkit

# 在目标项目中链接所需文件
ln -s ~/claude-toolkit/.claude/skills/my-skill.md .claude/skills/my-skill.md
```

### 方式二：Git Submodule

```bash
cd your-project
git submodule add https://github.com/a60717937/claude-toolkit.git .claude/shared
```

## 📦 内容规划

| 目录 | 用途 | 示例 |
|------|------|------|
| `agents/` | 自定义 Agent 类型定义 | 代码审查专用 agent、自动化测试 agent |
| `skills/` | 可复用的技能脚本 | 项目初始化、部署流程、代码生成 |
| `rules/` | 通用开发规范 | 代码风格、命名规范、Git 提交规范 |

## 🛠️ 技术说明

- 基于 [Claude Code](https://claude.ai/code) 的扩展机制
- 使用 MCP（Model Context Protocol）集成外部工具
- 遵循约定式配置，零运行依赖

## 📄 License

MIT
