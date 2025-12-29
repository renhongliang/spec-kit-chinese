<div align="center">
    <img src="./media/logo_large.webp" alt="Spec Kit Logo" width="200" height="200"/>
    <h1>🌱 Spec Kit Chinese</h1>
    <h3><em>更快地构建高质量软件。</em></h3>
</div>

<p align="center">
    <strong>本软件是SPEC KIT的中文版本和更新版本，在SPEC KIT的基础上进行了更新优化，所有提示使用中文，方便中文用户学习</strong>
</p>


---

## 目录

- [🤔 什么是规范驱动开发？](#-what-is-spec-driven-development)
- [⚡ 开始使用](#-get-started)
- [🤖 支持的 AI 助手](#-supported-ai-agents)
- [🔧 Specify CLI 参考](#-specify-cli-reference)
- [📚 核心理念](#-core-philosophy)
- [🌟 开发阶段](#-development-phases)
- [📄 许可证](#-license)

## 🤔 什么是规范驱动开发？

规范驱动开发**颠覆了**传统软件开发。几十年来，代码一直是王者——规范只是我们构建并在编码"真正工作"开始后丢弃的脚手架。规范驱动开发改变了这一点：**规范变得可执行**，直接生成可工作的实现，而不仅仅是指导它们。

## ⚡ 开始使用

### 1. 安装 Specify CLI

选择您首选的安装方法：

#### 选项 1：持久安装（推荐）

安装一次，随处使用：

```bash
uv tool install specify-cli --from git+https://github.com/renhongliang/spec-kit-chinese.git
```

然后直接使用该工具：

```bash
# 创建新项目
specify init <PROJECT_NAME>

# 或在现有项目中初始化
specify init . --ai claude
# 或
specify init --here --ai claude

# 检查已安装的工具
specify check
```

要升级 Specify，请参阅[升级指南](./docs/upgrade.md)了解详细说明。快速升级：

```bash
uv tool install specify-cli --force --from git+https://github.com/renhongliang/spec-kit-chinese.git
```

#### 选项 2：一次性使用

无需安装直接运行：

```bash
uvx --from git+https://github.com/renhongliang/spec-kit-chinese.git specify init <PROJECT_NAME>
```

**持久安装的好处：**

- 工具保持安装并在 PATH 中可用
- 无需创建 shell 别名
- 使用 `uv tool list`、`uv tool upgrade`、`uv tool uninstall` 更好地管理工具
- 更简洁的 shell 配置

### 2. 建立项目原则

在项目目录中启动您的 AI 助手。`/speckit.*` 命令在助手中可用。

使用 **`/speckit.constitution`** 命令创建项目的治理原则和开发指南，这些将指导所有后续开发。

```bash
/speckit.constitution 创建专注于代码质量、测试标准、用户体验一致性和性能要求的原则
```

### 3. 创建规范

使用 **`/speckit.specify`** 命令描述您想要构建的内容。专注于**什么**和**为什么**，而不是技术栈。

```bash
/speckit.specify 构建一个可以帮助我在单独的相册中组织照片的应用程序。相册按日期分组，可以通过在主页上拖放来重新组织。相册永远不会嵌套在其他相册中。在每个相册中，照片以类似图块的界面预览。
```

### 4. 创建技术实施计划

使用 **`/speckit.plan`** 命令提供您的技术栈和架构选择。

```bash
/speckit.plan 应用程序使用 Vite，库数量最少。尽可能使用原生 HTML、CSS 和 JavaScript。图像不上传到任何地方，元数据存储在本地 SQLite 数据库中。
```

### 5. 分解为任务

使用 **`/speckit.tasks`** 从您的实施计划创建可操作的任务列表。

```bash
/speckit.tasks
```

### 6. 执行实施

使用 **`/speckit.implement`** 执行所有任务并根据计划构建您的功能。

```bash
/speckit.implement
```

有关详细的分步说明，请参阅我们的[综合指南](./spec-driven.md)。


## 🤖 Supported AI Agents

| Agent                                                                                | Support | Notes                                                                                                                                     |
| ------------------------------------------------------------------------------------ | ------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| [Qoder CLI](https://qoder.com/cli)                                                   | ✅      |                                                                                                                                           |
| [Amazon Q Developer CLI](https://aws.amazon.com/developer/learning/q-developer-cli/) | ⚠️      | Amazon Q Developer CLI [does not support](https://github.com/aws/amazon-q-developer-cli/issues/3064) custom arguments for slash commands. |
| [Amp](https://ampcode.com/)                                                          | ✅      |                                                                                                                                           |
| [Auggie CLI](https://docs.augmentcode.com/cli/overview)                              | ✅      |                                                                                                                                           |
| [Claude Code](https://www.anthropic.com/claude-code)                                 | ✅      |                                                                                                                                           |
| [CodeBuddy CLI](https://www.codebuddy.ai/cli)                                        | ✅      |                                                                                                                                           |
| [Codex CLI](https://github.com/openai/codex)                                         | ✅      |                                                                                                                                           |
| [Cursor](https://cursor.sh/)                                                         | ✅      |                                                                                                                                           |
| [Gemini CLI](https://github.com/google-gemini/gemini-cli)                            | ✅      |                                                                                                                                           |
| [GitHub Copilot](https://code.visualstudio.com/)                                     | ✅      |                                                                                                                                           |
| [IBM Bob](https://www.ibm.com/products/bob)                                          | ✅      | IDE-based agent with slash command support                                                                                                |
| [Jules](https://jules.google.com/)                                                   | ✅      |                                                                                                                                           |
| [Kilo Code](https://github.com/Kilo-Org/kilocode)                                    | ✅      |                                                                                                                                           |
| [opencode](https://opencode.ai/)                                                     | ✅      |                                                                                                                                           |
| [Qwen Code](https://github.com/QwenLM/qwen-code)                                     | ✅      |                                                                                                                                           |
| [Roo Code](https://roocode.com/)                                                     | ✅      |                                                                                                                                           |
| [SHAI (OVHcloud)](https://github.com/ovh/shai)                                       | ✅      |                                                                                                                                           |
| [Windsurf](https://windsurf.com/)                                                    | ✅      |                                                                                                                                           |

## 🔧 核心变更说明


## 📚 核心理念

规范驱动开发是一个结构化过程，强调：

- **意图驱动开发**，规范在"如何"之前定义"什么"
- **丰富的规范创建**，使用护栏和组织原则
- **多步骤细化**，而不是从提示一次性生成代码
- **严重依赖**高级 AI 模型能力进行规范解释

## 🌟 开发阶段

| 阶段                                    | 重点                    | 关键活动                                                                                                                                                     |
| ---------------------------------------- | ------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **0到1开发**（"绿地"）    | 从零生成    | <ul><li>从高级需求开始</li><li>生成规范</li><li>规划实施步骤</li><li>构建生产就绪的应用程序</li></ul> |
| **创意探索**                 | 并行实施 | <ul><li>探索多样化的解决方案</li><li>支持多种技术栈和架构</li><li>尝试 UX 模式</li></ul>                         |
| **迭代增强**（"棕地"） | 棕地现代化 | <ul><li>迭代添加功能</li><li>现代化遗留系统</li><li>适应流程</li></ul>                                                                |

## 🎯 实验目标

我们的研究和实验重点：

### 技术独立性

- 使用多样化的技术栈创建应用程序
- 验证规范驱动开发是一个不绑定特定技术、编程语言或框架的过程的假设

### 企业约束

- 演示关键任务应用程序开发
- 纳入组织约束（云提供商、技术栈、工程实践）
- 支持企业设计系统和合规要求

### 以用户为中心的开发

- 为不同的用户群体和偏好构建应用程序
- 支持各种开发方法（从 vibe-coding 到 AI 原生开发）

### 创意和迭代流程

- 验证并行实施探索的概念
- 提供强大的迭代功能开发工作流
- 扩展流程以处理升级和现代化任务

## 🔧 先决条件

- **Linux/macOS/Windows**
- [支持的](#-supported-ai-agents) AI 编程助手
- [uv](https://docs.astral.sh/uv/) 用于包管理
- [Python 3.11+](https://www.python.org/downloads/)
- [Git](https://git-scm.com/downloads)

如果您在使用某个助手时遇到问题，请打开一个问题，以便我们改进集成。

## 📄 许可证

本项目仅仅将SPEC KIT 全部汉化，方便大家学习理解
欢迎大家关注我，一起研讨学习SDD
![公众号](./media/qrcode.jpg)
