# 为 Spec Kit 做贡献

您好！我们很高兴您想为 Spec Kit 做贡献。对此项目的贡献根据[项目的开源许可证](LICENSE)在[项目许可](https://help.github.com/articles/github-terms-of-service/#6-contributions-under-repository-license)下向公众发布。

请注意，本项目附带[贡献者行为准则](CODE_OF_CONDUCT.md)发布。通过参与此项目，您同意遵守其条款。

## 运行和测试代码的先决条件

这些是一次性安装，需要能够本地测试您的更改，作为 pull request (PR) 提交过程的一部分。

1. 安装 [Python 3.11+](https://www.python.org/downloads/)
1. 安装 [uv](https://docs.astral.sh/uv/) 用于包管理
1. 安装 [Git](https://git-scm.com/downloads)
1. 拥有可用的 [AI 编程助手](README.md#-supported-ai-agents)

<details>
<summary><b>💡 如果您使用 <code>VSCode</code> 或 <code>GitHub Codespaces</code> 作为您的 IDE 的提示</b></summary>

<br>

如果您在机器上安装了 [Docker](https://docker.com)，您可以通过此 [VSCode 扩展](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)利用 [Dev Containers](https://containers.dev)，轻松设置您的开发环境，上述工具已经安装和配置，这要归功于 `.devcontainer/devcontainer.json` 文件（位于项目根目录）。

要做到这一点，只需：

- 检出仓库
- 用 VSCode 打开它
- 打开[命令面板](https://code.visualstudio.com/docs/getstarted/userinterface#_command-palette)并选择"Dev Containers: Open Folder in Container..."

在 [GitHub Codespaces](https://github.com/features/codespaces) 上更简单，因为它在打开 codespace 时自动利用 `.devcontainer/devcontainer.json`。

</details>

## 提交 pull request

> [!NOTE]
> 如果您的 pull request 引入了对 CLI 或仓库其余部分的工作产生重大影响的大更改（例如，您正在引入新模板、参数或其他重大更改），请确保它已由项目维护者**讨论并同意**。没有事先对话和同意的大更改的 pull request 将被关闭。

1. Fork 并克隆仓库
1. 配置并安装依赖项：`uv sync`
1. 确保 CLI 在您的机器上工作：`uv run specify --help`
1. 创建新分支：`git checkout -b my-branch-name`
1. 进行更改，添加测试，并确保一切仍然正常工作
1. 如果相关，使用示例项目测试 CLI 功能
1. 推送到您的 fork 并提交 pull request
1. 等待您的 pull request 被审查和合并。

以下是一些可以增加您的 pull request 被接受可能性的做法：

- 遵循项目的编码约定。
- 为新功能编写测试。
- 如果您的更改影响面向用户的功能，请更新文档（`README.md`、`spec-driven.md`）。
- 尽可能保持更改的专注。如果您想进行多个不相互依赖的更改，请考虑将它们作为单独的 pull request 提交。
- 编写[良好的提交消息](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html)。
- 使用规范驱动开发工作流测试您的更改以确保兼容性。

## Development workflow

When working on spec-kit:

1. Test changes with the `specify` CLI commands (`/speckit.specify`, `/speckit.plan`, `/speckit.tasks`) in your coding agent of choice
2. Verify templates are working correctly in `templates/` directory
3. Test script functionality in the `scripts/` directory
4. Ensure memory files (`memory/constitution.md`) are updated if major process changes are made

### Testing template and command changes locally

Running `uv run specify init` pulls released packages, which won’t include your local changes.  
To test your templates, commands, and other changes locally, follow these steps:

1. **Create release packages**

   Run the following command to generate the local packages:

   ```bash
   ./.github/workflows/scripts/create-release-packages.sh v1.0.0
   ```

2. **Copy the relevant package to your test project**

   ```bash
   cp -r .genreleases/sdd-copilot-package-sh/. <path-to-test-project>/
   ```

3. **Open and test the agent**

   Navigate to your test project folder and open the agent to verify your implementation.

## Spec Kit 中的 AI 贡献

> [!IMPORTANT]
>
> 如果您使用**任何类型的 AI 辅助**为 Spec Kit 做贡献，
> 必须在 pull request 或 issue 中披露。

我们欢迎并鼓励使用 AI 工具来帮助改进 Spec Kit！许多有价值的贡献都通过 AI 辅助得到了增强，用于代码生成、问题检测和功能定义。

话虽如此，如果您在为 Spec Kit 做贡献时使用任何类型的 AI 辅助（例如，代理、ChatGPT），
**必须在 pull request 或 issue 中披露**，以及使用 AI 辅助的程度（例如，文档注释与代码生成）。

如果您的 PR 响应或评论是由 AI 生成的，也请披露。

作为例外，琐碎的间距或拼写错误修复不需要披露，只要更改仅限于代码的小部分或短短语。

披露示例：

> 此 PR 主要由 GitHub Copilot 编写。

或更详细的披露：

> 我咨询了 ChatGPT 以理解代码库，但解决方案
> 完全由我自己手动编写。

不披露这一点首先对 pull request 另一端的人类操作者是不礼貌的，但它也使
确定对贡献应用多少审查变得困难。

在理想世界中，AI 辅助会产生与任何人类同等或更高质量的工作。这不是我们今天生活的世界，在大多数情况下
人类监督或专业知识不在循环中，它生成的代码无法合理维护或演进。

### 我们寻找的内容

提交 AI 辅助贡献时，请确保它们包括：

- **明确披露 AI 使用** - 您对 AI 使用以及您将其用于贡献的程度保持透明
- **人类理解和测试** - 您亲自测试了更改并理解它们的作用
- **明确的理由** - 您可以解释为什么需要更改以及它如何符合 Spec Kit 的目标
- **具体证据** - 包括测试用例、场景或示例，展示改进
- **您自己的分析** - 分享您对端到端开发体验的想法

### 我们将关闭的内容

我们保留关闭以下贡献的权利：

- 未经验证提交的未测试更改
- 不解决特定 Spec Kit 需求的通用建议
- 显示没有人类审查或理解的大批量提交

### 成功指南

关键是证明您理解并验证了您提出的更改。如果维护者可以轻易看出贡献完全由 AI 生成而没有人类输入或测试，它可能在提交前需要更多工作。

持续提交低努力 AI 生成更改的贡献者可能会被维护者酌情限制进一步贡献。

请尊重维护者并披露 AI 辅助。

## 资源

- [规范驱动开发方法论](./spec-driven.md)
- [如何为开源做贡献](https://opensource.guide/how-to-contribute/)
- [使用 Pull Requests](https://help.github.com/articles/about-pull-requests/)
- [GitHub 帮助](https://help.github.com)
