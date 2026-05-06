# Discovery Rules

Issue Discovery Orbit 把讨论、PRD、计划或仓库理解整理成 issue tracker 工作项。

## Purpose

- `to-prd`: 从当前上下文和仓库理解生成 PRD。
- `to-issues`: 把计划或 PRD 拆成 vertical slice issues。
- 发布规则明确时可发布；规则缺失或冲突时只输出 candidates。

## Outputs

**PRD**:
可作为 tracker Issue 发布的产品需求文档。

**Slice plan**:
发布 issues 前的人类确认计划。

**Issue candidate**:
尚未发布到 issue tracker 的工作项候选；不是 Issue，不是事实源。

**Issue**:
tracker 返回的工作项；这是 issue tracker 事实。

## Before Publishing

按兼容性读取目标仓库可用的 Repository Publishing Rules；来源是候选来源，不是必备目录结构：

- 通用 agent 入口或仓库规则文档，例如 `AGENTS.md`。
- tracker contract 文档，例如 Issue Tracker Contract 约定或仓库自定义等价文件。
- issue 模板配置，例如 GitHub `.github/ISSUE_TEMPLATE/` 或其他 tracker 模板。
- 其他明确说明 issue tracker、模板、labels、状态入口或发布权限的文档。

同时按兼容性读取可用的项目记忆；它不是发布规则，也不是必备目录结构：

- Design Memory 约定，例如 `CONTEXT.md`、`CONTEXT-MAP.md` 或 `docs/adr/`。
- 仓库声明的领域语言、context map 或设计决策记录。
- 对话、issue body 或任务描述中已有的相关背景。

发布时只使用仓库定义的 issue templates、状态、labels、assignee、milestone 和项目字段。

## Candidate Fallback

以下情况只输出 candidates，并列出缺失或冲突的规则：

- 找不到 issue tracker。
- 找不到应使用的模板或 label 规则。
- 仓库文档之间互相冲突。
- tracker 权限不可用。
- 用户要求的发布方式与仓库规则冲突。
