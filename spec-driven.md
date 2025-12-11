# 规范驱动开发 (SDD)

## 权力反转

几十年来，代码一直是王者。规范服务于代码——它们是我们构建的脚手架，一旦编码的"真正工作"开始就被丢弃了。我们编写 PRD 来指导开发，创建设计文档来告知实施，绘制图表来可视化架构。但这些总是从属于代码本身。代码就是真理。其他一切充其量只是良好的意图。代码是真理的源泉，随着它向前推进，规范很少能跟上步伐。由于资产（代码）和实施是一体的，如果不从代码构建，就很难有并行实施。

规范驱动开发 (SDD) 反转了这种权力结构。规范不服务于代码——代码服务于规范。产品需求文档 (PRD) 不是实施的指南；它是生成实施的源泉。技术计划不是告知编码的文档；它们是产生代码的精确定义。这不是对我们如何构建软件的渐进式改进。这是对驱动开发的根本性重新思考。

规范与实施之间的差距自软件开发诞生以来就一直困扰着它。我们试图用更好的文档、更详细的需求、更严格的流程来弥合它。这些方法失败了，因为它们接受差距是不可避免的。它们试图缩小差距但从未消除它。SDD 通过使规范及其从规范产生的具体实施计划可执行来消除差距。当规范和实施计划生成代码时，没有差距——只有转换。

这种转换现在成为可能，因为 AI 可以理解和实施复杂的规范，并创建详细的实施计划。但没有结构的原始 AI 生成会产生混乱。SDD 通过精确、完整且足够明确的规范和后续实施计划来生成可工作的系统，从而提供这种结构。规范成为主要工件。代码成为它在特定语言和框架中的表达（作为来自实施计划的实施）。

在这个新世界中，维护软件意味着演进规范。开发团队的意图用自然语言（"**意图驱动开发**"）、设计资产、核心原则和其他指南来表达。开发的**通用语言**提升到更高层次，代码是最后一英里的方法。

调试意味着修复生成错误代码的规范及其实施计划。重构意味着为了清晰而重新构建。整个开发工作流围绕规范作为中央真理源重新组织，实施计划和代码作为持续再生的输出。用新功能更新应用程序或创建新的并行实施，因为我们是有创造力的存在，意味着重新审视规范并创建新的实施计划。因此，这个过程是 0 -> 1, (1', ..), 2, 3, N。

开发团队专注于他们的创造力、实验和批判性思维。

## SDD 工作流实践

工作流从一个想法开始——通常是模糊和不完整的。通过与 AI 的迭代对话，这个想法变成了一个全面的 PRD。AI 提出澄清问题，识别边界情况，并帮助定义精确的验收标准。在传统开发中可能需要数天会议和文档的工作，在专注的规范工作中只需数小时就能完成。这改变了传统的 SDLC——需求和设计成为持续活动而不是离散阶段。这支持**团队流程**，其中团队审查的规范被表达和版本化，在分支中创建并合并。

当产品经理更新验收标准时，实施计划会自动标记受影响的技术决策。当架构师发现更好的模式时，PRD 会更新以反映新的可能性。

在整个规范过程中，研究代理收集关键上下文。它们调查库兼容性、性能基准和安全影响。组织约束被自动发现和应用——您公司的数据库标准、身份验证要求和部署策略无缝集成到每个规范中。

从 PRD，AI 生成将需求映射到技术决策的实施计划。每个技术选择都有文档化的理由。每个架构决策都追溯到特定需求。在整个过程中，一致性验证持续提高质量。AI 分析规范的歧义、矛盾和差距——不是作为一次性门控，而是作为持续细化。

一旦规范及其实施计划足够稳定，代码生成就开始了，但它们不必"完整"。早期生成可能是探索性的——测试规范在实践中是否有意义。领域概念变成数据模型。用户故事变成 API 端点。验收场景变成测试。这通过规范合并开发和测试——测试场景不是在代码之后编写的，它们是生成实施和测试的规范的一部分。

反馈循环延伸到初始开发之外。生产指标和事件不仅触发热修复——它们更新规范以进行下一次再生。性能瓶颈成为新的非功能需求。安全漏洞成为影响所有未来生成的约束。规范、实施和运营现实之间的这种迭代舞蹈是真正理解出现的地方，也是传统 SDLC 转变为持续演进的地方。

## 为什么 SDD 现在很重要

三个趋势使 SDD 不仅可能而且必要：

首先，AI 能力已经达到一个阈值，自然语言规范可以可靠地生成可工作的代码。这不是要取代开发人员——而是通过自动化从规范到实施的机械转换来放大他们的有效性。它可以放大探索和创造力，轻松支持"重新开始"，并支持加法、减法和批判性思维。

其次，软件复杂性继续呈指数级增长。现代系统集成了数十个服务、框架和依赖项。通过手动流程保持所有这些部分与原始意图对齐变得越来越困难。SDD 通过规范驱动的生成提供系统对齐。框架可能演变为提供 AI 优先支持，而不是人类优先支持，或围绕可重用组件进行架构。

第三，变化速度加快。需求变化比以往任何时候都快得多。转向不再是例外——它是预期的。现代产品开发需要基于用户反馈、市场条件和竞争压力的快速迭代。传统开发将这些变化视为干扰。每次转向都需要手动通过文档、设计和代码传播变化。结果要么是限制速度的缓慢、谨慎的更新，要么是积累技术债务的快速、鲁莽的变化。

SDD 可以支持假设/模拟实验："如果我们需要重新实施或更改应用程序以促进销售更多 T 恤的业务需求，我们将如何实施和实验？"

SDD 将需求变化从障碍转变为正常工作流。当规范驱动实施时，转向成为系统化再生而不是手动重写。更改 PRD 中的核心需求，受影响实施计划会自动更新。修改用户故事，相应的 API 端点会重新生成。这不仅仅是关于初始开发——它是关于通过不可避免的变化保持工程速度。

## 核心原则

**规范作为通用语言**：规范成为主要工件。代码成为它在特定语言和框架中的表达。维护软件意味着演进规范。

**可执行规范**：规范必须精确、完整且足够明确，以生成可工作的系统。这消除了意图和实施之间的差距。

**持续细化**：一致性验证持续进行，而不是作为一次性门控。AI 将规范分析歧义、矛盾和差距作为持续过程。

**研究驱动的上下文**：研究代理在整个规范过程中收集关键上下文，调查技术选项、性能影响和组织约束。

**双向反馈**：生产现实告知规范演进。指标、事件和运营学习成为规范细化的输入。

**分支探索**：从同一规范生成多种实施方法，以探索不同的优化目标——性能、可维护性、用户体验、成本。

## 实施方法

今天，实践 SDD 需要组装现有工具并在整个过程中保持纪律。该方法可以通过以下方式实践：

- 用于迭代规范开发的 AI 助手
- 用于收集技术上下文的研究代理
- 用于将规范转换为实施的代码生成工具
- 适应规范优先工作流的版本控制系统
- 通过 AI 分析规范文档进行一致性检查

关键是将规范视为真理源，代码作为服务于规范而非相反方向的生成输出。

## 使用命令简化 SDD

SDD 方法论通过三个强大的命令得到显著增强，这些命令自动化了规范 → 规划 → 任务分配工作流：

### `/speckit.specify` 命令

此命令将简单的功能描述（用户提示）转换为完整的结构化规范，并自动进行仓库管理：

1. **自动功能编号**：扫描现有规范以确定下一个功能编号（例如，001、002、003）
2. **分支创建**：从您的描述生成语义分支名称并自动创建
3. **基于模板的生成**：使用您的需求复制和自定义功能规范模板
4. **目录结构**：为所有相关文档创建适当的 `specs/[branch-name]/` 结构

### `/speckit.plan` 命令

一旦功能规范存在，此命令创建全面的实施计划：

1. **规范分析**：读取并理解功能需求、用户故事和验收标准
2. **宪法合规**：确保与项目宪法和架构原则对齐
3. **技术转换**：将业务需求转换为技术架构和实施细节
4. **详细文档**：为数据模型、API 合约和测试场景生成支持文档
5. **快速开始验证**：生成捕获关键验证场景的快速开始指南

### `/speckit.tasks` 命令

创建计划后，此命令分析计划和相关设计文档以生成可执行任务列表：

1. **输入**：读取 `plan.md`（必需）以及如果存在的 `data-model.md`、`contracts/` 和 `research.md`
2. **任务派生**：将合约、实体和场景转换为特定任务
3. **并行化**：标记独立任务 `[P]` 并概述安全的并行组
4. **输出**：在功能目录中写入 `tasks.md`，准备由任务代理执行

### Example: Building a Chat Feature

Here's how these commands transform the traditional development workflow:

**Traditional Approach:**

```text
1. Write a PRD in a document (2-3 hours)
2. Create design documents (2-3 hours)
3. Set up project structure manually (30 minutes)
4. Write technical specifications (3-4 hours)
5. Create test plans (2 hours)
Total: ~12 hours of documentation work
```

**SDD with Commands Approach:**

```bash
# Step 1: Create the feature specification (5 minutes)
/speckit.specify Real-time chat system with message history and user presence

# This automatically:
# - Creates branch "003-chat-system"
# - Generates specs/003-chat-system/spec.md
# - Populates it with structured requirements

# Step 2: Generate implementation plan (5 minutes)
/speckit.plan WebSocket for real-time messaging, PostgreSQL for history, Redis for presence

# Step 3: Generate executable tasks (5 minutes)
/speckit.tasks

# This automatically creates:
# - specs/003-chat-system/plan.md
# - specs/003-chat-system/research.md (WebSocket library comparisons)
# - specs/003-chat-system/data-model.md (Message and User schemas)
# - specs/003-chat-system/contracts/ (WebSocket events, REST endpoints)
# - specs/003-chat-system/quickstart.md (Key validation scenarios)
# - specs/003-chat-system/tasks.md (Task list derived from the plan)
```

In 15 minutes, you have:

- A complete feature specification with user stories and acceptance criteria
- A detailed implementation plan with technology choices and rationale
- API contracts and data models ready for code generation
- Comprehensive test scenarios for both automated and manual testing
- All documents properly versioned in a feature branch

### 结构化自动化的力量

这些命令不仅节省时间——它们强制执行一致性和完整性：

1. **不遗漏细节**：模板确保考虑每个方面，从非功能需求到错误处理
2. **可追溯的决策**：每个技术选择都链接回特定需求
3. **活文档**：规范与代码保持同步，因为它们生成代码
4. **快速迭代**：更改需求并在几分钟内重新生成计划，而不是数天

这些命令通过将规范视为可执行工件而不是静态文档来体现 SDD 原则。它们将规范过程从必要的邪恶转变为开发的驱动力。

### Template-Driven Quality: How Structure Constrains LLMs for Better Outcomes

The true power of these commands lies not just in automation, but in how the templates guide LLM behavior toward higher-quality specifications. The templates act as sophisticated prompts that constrain the LLM's output in productive ways:

#### 1. **Preventing Premature Implementation Details**

The feature specification template explicitly instructs:

```text
- ✅ Focus on WHAT users need and WHY
- ❌ Avoid HOW to implement (no tech stack, APIs, code structure)
```

This constraint forces the LLM to maintain proper abstraction levels. When an LLM might naturally jump to "implement using React with Redux," the template keeps it focused on "users need real-time updates of their data." This separation ensures specifications remain stable even as implementation technologies change.

#### 2. **Forcing Explicit Uncertainty Markers**

Both templates mandate the use of `[NEEDS CLARIFICATION]` markers:

```text
When creating this spec from a user prompt:
1. **Mark all ambiguities**: Use [NEEDS CLARIFICATION: specific question]
2. **Don't guess**: If the prompt doesn't specify something, mark it
```

This prevents the common LLM behavior of making plausible but potentially incorrect assumptions. Instead of guessing that a "login system" uses email/password authentication, the LLM must mark it as `[NEEDS CLARIFICATION: auth method not specified - email/password, SSO, OAuth?]`.

#### 3. **Structured Thinking Through Checklists**

The templates include comprehensive checklists that act as "unit tests" for the specification:

```markdown
### Requirement Completeness

- [ ] No [NEEDS CLARIFICATION] markers remain
- [ ] Requirements are testable and unambiguous
- [ ] Success criteria are measurable
```

These checklists force the LLM to self-review its output systematically, catching gaps that might otherwise slip through. It's like giving the LLM a quality assurance framework.

#### 4. **Constitutional Compliance Through Gates**

The implementation plan template enforces architectural principles through phase gates:

```markdown
### Phase -1: Pre-Implementation Gates

#### Simplicity Gate (Article VII)

- [ ] Using ≤3 projects?
- [ ] No future-proofing?

#### Anti-Abstraction Gate (Article VIII)

- [ ] Using framework directly?
- [ ] Single model representation?
```

These gates prevent over-engineering by making the LLM explicitly justify any complexity. If a gate fails, the LLM must document why in the "Complexity Tracking" section, creating accountability for architectural decisions.

#### 5. **Hierarchical Detail Management**

The templates enforce proper information architecture:

```text
**IMPORTANT**: This implementation plan should remain high-level and readable.
Any code samples, detailed algorithms, or extensive technical specifications
must be placed in the appropriate `implementation-details/` file
```

This prevents the common problem of specifications becoming unreadable code dumps. The LLM learns to maintain appropriate detail levels, extracting complexity to separate files while keeping the main document navigable.

#### 6. **Test-First Thinking**

The implementation template enforces test-first development:

```text
### File Creation Order
1. Create `contracts/` with API specifications
2. Create test files in order: contract → integration → e2e → unit
3. Create source files to make tests pass
```

This ordering constraint ensures the LLM thinks about testability and contracts before implementation, leading to more robust and verifiable specifications.

#### 7. **Preventing Speculative Features**

Templates explicitly discourage speculation:

```text
- [ ] No speculative or "might need" features
- [ ] All phases have clear prerequisites and deliverables
```

This stops the LLM from adding "nice to have" features that complicate implementation. Every feature must trace back to a concrete user story with clear acceptance criteria.

### 复合效应

这些约束共同产生以下规范：

- **完整**：检查清单确保不遗漏任何内容
- **明确**：强制澄清标记突出不确定性
- **可测试**：测试优先思维融入过程
- **可维护**：适当的抽象层次和信息层次结构
- **可实施**：具有具体可交付成果的清晰阶段

模板将 LLM 从创意作家转变为纪律严明的规范工程师，引导其能力产生始终如一的高质量、可执行规范，真正驱动开发。

## 宪法基础：执行架构纪律

SDD 的核心是宪法——一套管理规范如何变成代码的不可变原则。宪法（`memory/constitution.md`）充当系统的架构 DNA，确保每个生成的实施保持一致性、简单性和质量。

### 开发的九条条款

宪法定义了塑造开发过程每个方面的九条条款：

#### 条款 I：库优先原则

每个功能必须作为独立库开始——没有例外。这从一开始就强制模块化设计：

```text
Specify 中的每个功能必须作为独立库开始其存在。
任何功能不得在首先抽象为可重用库组件之前
直接在应用程序代码中实施。
```

此原则确保规范生成模块化、可重用的代码，而不是单体应用程序。当 LLM 生成实施计划时，它必须将功能构建为具有清晰边界和最少依赖项的库。

#### 条款 II：CLI 接口要求

每个库必须通过命令行接口公开其功能：

```text
所有 CLI 接口必须：
- 接受文本作为输入（通过 stdin、参数或文件）
- 产生文本作为输出（通过 stdout）
- 支持 JSON 格式用于结构化数据交换
```

这强制执行可观测性和可测试性。LLM 不能将功能隐藏在 opaque 类中——一切都必须通过基于文本的接口访问和验证。

#### 条款 III：测试优先要求

最具变革性的条款——测试之前没有代码：

```text
这是不可协商的：所有实施必须遵循严格的测试驱动开发。
在以下情况之前不得编写任何实施代码：
1. 编写单元测试
2. 测试经过验证并获得用户批准
3. 确认测试失败（红色阶段）
```

这完全反转了传统的 AI 代码生成。不是生成代码并希望它工作，LLM 必须首先生成定义行为的全面测试，获得批准，然后才生成实施。

#### 条款 VII 和 VIII：简单性和反抽象

这些配对条款对抗过度工程：

```text
第 7.3 节：最小项目结构
- 初始实施最多 3 个项目
- 其他项目需要文档化的理由

第 8.1 节：框架信任
- 直接使用框架功能而不是包装它们
```

当 LLM 可能自然创建精心设计的抽象时，这些条款强制它证明每一层复杂性的合理性。实施计划模板的"阶段 -1 门控"直接强制执行这些原则。

#### 条款 IX：集成优先测试

优先考虑真实世界测试而不是隔离的单元测试：

```text
测试必须使用真实环境：
- 优先使用真实数据库而不是模拟
- 使用实际服务实例而不是存根
- 实施前必须进行合约测试
```

这确保生成的代码在实践中工作，而不仅仅是在理论上。

### Constitutional Enforcement Through Templates

The implementation plan template operationalizes these articles through concrete checkpoints:

```markdown
### Phase -1: Pre-Implementation Gates

#### Simplicity Gate (Article VII)

- [ ] Using ≤3 projects?
- [ ] No future-proofing?

#### Anti-Abstraction Gate (Article VIII)

- [ ] Using framework directly?
- [ ] Single model representation?

#### Integration-First Gate (Article IX)

- [ ] Contracts defined?
- [ ] Contract tests written?
```

These gates act as compile-time checks for architectural principles. The LLM cannot proceed without either passing the gates or documenting justified exceptions in the "Complexity Tracking" section.

### 不可变原则的力量

宪法的力量在于其不可变性。虽然实施细节可以演进，但核心原则保持不变。这提供了：

1. **跨时间一致性**：今天生成的代码遵循与明年生成的代码相同的原则
2. **跨 LLM 一致性**：不同的 AI 模型产生架构兼容的代码
3. **架构完整性**：每个功能都加强而不是削弱系统设计
4. **质量保证**：测试优先、库优先和简单性原则确保可维护代码

### 宪法演进

虽然原则是不可变的，但它们的应用可以演进：

```text
第 4.2 节：修正程序
对此宪法的修改需要：
- 明确记录变更理由
- 项目维护者审查和批准
- 向后兼容性评估
```

这允许方法论在保持稳定性的同时学习和改进。宪法通过带日期的修正案显示其自身演进，展示如何根据真实世界经验细化原则。

### 超越规则：开发哲学

宪法不仅仅是规则手册——它是塑造 LLM 如何思考代码生成的哲学：

- **可观测性优于不透明性**：一切都必须通过 CLI 接口可检查
- **简单性优于巧妙性**：从简单开始，仅在证明必要时添加复杂性
- **集成优于隔离**：在真实环境中测试，而不是人工环境
- **模块化优于单体**：每个功能都是具有清晰边界的库

通过将这些原则嵌入规范和规划过程，SDD 确保生成的代码不仅仅是功能性的——它是可维护的、可测试的和架构健全的。宪法将 AI 从代码生成器转变为尊重和加强系统设计原则的架构合作伙伴。

## 转变

这不是要取代开发人员或自动化创造力。它是通过自动化机械转换来放大人类能力。它是关于创建一个紧密的反馈循环，其中规范、研究和代码一起演进，每次迭代都带来更深入的理解以及意图和实施之间更好的对齐。

软件开发需要更好的工具来保持意图和实施之间的对齐。SDD 提供了通过生成代码而不仅仅是指导代码的可执行规范来实现这种对齐的方法论。
