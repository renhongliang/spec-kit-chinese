# 快速开始指南

本指南将帮助您开始使用 Spec Kit 进行规范驱动开发。

> [!NOTE]
> 所有自动化脚本现在都提供 Bash (`.sh`) 和 PowerShell (`.ps1`) 两种变体。`specify` CLI 会根据操作系统自动选择，除非您传递 `--script sh|ps`。

## 6 步流程

> [!TIP]
> **上下文感知**：Spec Kit 命令会根据您当前的 Git 分支（例如，`001-feature-name`）自动检测活动功能。要在不同规范之间切换，只需切换 Git 分支。

### 步骤 1：安装 Specify

**在终端中**，运行 `specify` CLI 命令来初始化您的项目：

```bash
# 创建新项目目录
uvx --from git+https://github.com/github/spec-kit.git specify init <PROJECT_NAME>

# 或在当前目录中初始化
uvx --from git+https://github.com/github/spec-kit.git specify init .
```

明确选择脚本类型（可选）：

```bash
uvx --from git+https://github.com/github/spec-kit.git specify init <PROJECT_NAME> --script ps  # 强制 PowerShell
uvx --from git+https://github.com/github/spec-kit.git specify init <PROJECT_NAME> --script sh  # 强制 POSIX shell
```

### 步骤 2：定义您的宪法

**在 AI 助手的聊天界面中**，使用 `/speckit.constitution` 斜杠命令来建立项目的核心规则和原则。您应该将项目的特定原则作为参数提供。

```markdown
/speckit.constitution 此项目遵循"库优先"方法。所有功能必须首先作为独立库实现。我们严格使用 TDD。我们更喜欢函数式编程模式。
```

### 步骤 3：创建规范

**在聊天中**，使用 `/speckit.specify` 斜杠命令来描述您想要构建的内容。专注于**什么**和**为什么**，而不是技术栈。

```markdown
/speckit.specify 构建一个可以帮助我在单独的相册中组织照片的应用程序。相册按日期分组，可以通过在主页上拖放来重新组织。相册永远不会嵌套在其他相册中。在每个相册中，照片以类似图块的界面预览。
```

### 步骤 4：细化规范

**在聊天中**，使用 `/speckit.clarify` 斜杠命令来识别和解决规范中的歧义。您可以将特定的重点领域作为参数提供。

```bash
/speckit.clarify 专注于安全和性能要求。
```

### 步骤 5：创建技术实施计划

**在聊天中**，使用 `/speckit.plan` 斜杠命令来提供您的技术栈和架构选择。

```markdown
/speckit.plan 应用程序使用 Vite，库数量最少。尽可能使用原生 HTML、CSS 和 JavaScript。图像不上传到任何地方，元数据存储在本地 SQLite 数据库中。
```

### 步骤 6：分解和实施

**在聊天中**，使用 `/speckit.tasks` 斜杠命令创建可操作的任务列表。

```markdown
/speckit.tasks
```

可选地，使用 `/speckit.analyze` 验证计划：

```markdown
/speckit.analyze
```

然后，使用 `/speckit.implement` 斜杠命令执行计划。

```markdown
/speckit.implement
```

## 详细示例：构建 Taskify

这是一个构建团队生产力平台的完整示例：

### 步骤 1：定义宪法

初始化项目的宪法以设定基本规则：

```markdown
/speckit.constitution Taskify 是一个"安全优先"的应用程序。必须验证所有用户输入。我们使用微服务架构。代码必须完全文档化。
```

### 步骤 2：使用 `/speckit.specify` 定义需求

```text
开发 Taskify，一个团队生产力平台。它应该允许用户创建项目、添加团队成员、
分配任务、评论并在看板样式的板之间移动任务。在这个功能的初始阶段，
让我们称之为"创建 Taskify"，让我们有多个用户，但用户将提前声明，预定义。
我想要五个用户，分为两个不同的类别，一个产品经理和四个工程师。让我们创建三个
不同的示例项目。让我们为每个任务的状态设置标准看板列，例如"待办"、
"进行中"、"审查中"和"完成"。此应用程序将没有登录，因为这只是
第一个测试，以确保我们的基本功能已设置。
```

### 步骤 3：细化规范

使用 `/speckit.clarify` 命令交互式地解决规范中的任何歧义。您还可以提供要确保包含的特定详细信息。

```bash
/speckit.clarify 我想澄清任务卡详细信息。对于任务卡 UI 中的每个任务，您应该能够
在看板工作板的不同列之间更改任务的当前状态。您应该能够为特定卡片留下无限数量的评论。
您应该能够从该任务卡分配一个有效用户。
```

您可以使用 `/speckit.clarify` 继续用更多细节细化规范：

```bash
/speckit.clarify 当您首次启动 Taskify 时，它将为您提供五个用户的列表供您选择。
不需要密码。当您点击用户时，您进入主视图，显示项目列表。当您点击项目时，
您打开该项目的看板。您将看到列。您将能够在不同列之间拖放卡片。
您将看到分配给您的任何卡片，当前登录的用户，颜色与其他所有卡片不同，
因此您可以快速看到您的。您可以编辑您所做的任何评论，但不能编辑其他人所做的评论。
您可以删除您所做的任何评论，但不能删除其他人所做的评论。
```

### 步骤 4：验证规范

使用 `/speckit.checklist` 命令验证规范检查清单：

```bash
/speckit.checklist
```

### 步骤 5：使用 `/speckit.plan` 生成技术计划

具体说明您的技术栈和技术要求：

```bash
/speckit.plan 我们将使用 .NET Aspire 生成此项目，使用 Postgres 作为数据库。
前端应该使用 Blazor server，具有拖放任务板和实时更新。应该创建一个 REST API，
包含项目 API、任务 API 和通知 API。
```

### 步骤 6：验证和实施

让您的 AI 助手使用 `/speckit.analyze` 审核实施计划：

```bash
/speckit.analyze
```

最后，实施解决方案：

```bash
/speckit.implement
```

## 关键原则

- **明确**说明您正在构建什么以及为什么
- **不要专注于技术栈**在规范阶段
- **迭代和细化**您的规范，然后再实施
- **验证**计划，然后再开始编码
- **让 AI 助手处理**实施细节

## 下一步

- 阅读[完整方法论](../spec-driven.md)以获取深入指导
- 查看仓库中的[更多示例](../templates)
- 探索 [GitHub 上的源代码](https://github.com/github/spec-kit)
