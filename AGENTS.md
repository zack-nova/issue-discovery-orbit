# Issue Discovery Workflow

Issue Discovery Workflow 用于在需要时把想法、PRD 或计划切成 issue tracker 中可追踪的工作。

## 按需读取

- 生成 PRD、把计划切成 issues、或准备发布 issue candidates 时，先读 `docs/issue-discovery-orbit/discovery-rules.md`。
- 使用 `to-prd` 或 `to-issues` skill 时，由 skill 承担具体流程，并按 discovery rules 处理发布条件。
- 发布 PRD 或 issues 前，读取目标仓库的 Repository Publishing Rules；规则缺失或冲突时，只输出 candidates，不发布。

## 常驻边界

- 不要假设 issue tracker、模板、labels、状态入口或权限已经明确。
- 不要把未确认的候选 PRD 或 issue 当作已经发布的 tracker truth。
