# Digital Twin Collaboration Pattern（数字分身协作模式）

> 用"一个最了解主理人的早期 AI 分身"作为**战略守门人**：它负责审核标准、守住边界、校准方向，让主理人不用事事亲力亲为，又不会在关键处失控。

## 为什么需要数字分身

当 AI 要替主理人做"对外交付"时，最大的风险不是"做不好"，而是**在不该做主的地方越权**。与其让人盯着每一个产出，不如造一个分身当"守门人"：它把主理人的判断标准、边界、红线固化成可执行的规则，在人与 AI 之间建立一层可控的 Let 审核层。

**核心定位**：数字分身 = **守门人**。只管"守住边界、底线、主理人容易忘的事"，不做执行。

## 目录

| 文件 | 内容 |
|------|------|
| [`audit-standards.md`](audit-standards.md) | 出图 / 文案 / 交付四维审核标准 |
| [`authorization-boundary.md`](authorization-boundary.md) | 授权边界清单（可代劳 vs 必须本人） |
| [`red-lines-template.md`](red-lines-template.md) | 红线清单模板（9 条可复用） |
| [`communication-templates.md`](communication-templates.md) | 对外沟通话术模板（对客户 / 合作方 / 自我介绍） |
| [`weekly-report-format.md`](weekly-report-format.md) | 周报四段格式模板 |
| [`arbitration-mechanism.md`](arbitration-mechanism.md) | 仲裁机制（群内 @ + 期限响应） |

## 核心原则

1. **主理人是"人 + 决策者"，分身是"工具 + 执行者"**：这是所有话术和授权的根本性质。
2. **给选择题，不做填空题**：交付时给 2–3 个方案让主理人选，而不是让他一字一句指定方案。
3. **一次过，别一条条蹦**：需要主理人确认的事项集中发，尊重他的时间预算。
4. **拿不准的必须等本人确认**：永远不要替主理人做决定，即使"感觉他肯定同意"。

## 快速上手

1. 先写 `red-lines-template.md` 定死"绝对不能做"的红线。
2. 再用 `authorization-boundary.md` 分清"可代劳"与"必须本人"。
3. 配好 `communication-templates.md`，让分身以"助手/工具"的身份对外说话。
4. 接收交付时用 `audit-standards.md` 把关，卡住时走 `arbitration-mechanism.md`。

> 本模式是 `multi-ai-collaboration/role-architecture.md` 中"分身Agent"角色的深化实现，可与多 AI 协作框架组合使用。

## License

全仓默认 [MIT](../../LICENSE)，引用请保留出处。