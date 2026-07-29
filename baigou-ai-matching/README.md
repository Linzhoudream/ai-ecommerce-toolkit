# 白沟AI匹配台 · Baigou AI Matching Platform

> 白沟箱包产业智能供需撮合平台 — 用 AI 降低传统 BBS 信息门户的使用门槛

## 项目定位

白沟是全球最大的箱包产销基地之一，但现有的本地信息门户（如白沟河网）仍采用传统 BBS 发帖模式——用户需要自己写标题、描述、分类，信息参差不齐，匹配全靠人工浏览。

**白沟AI匹配台** 是一个概念验证 MVP，展示如何用 AI 改造传统垂直信息门户：

- **AI 追问对话**：替代自由发帖，AI 一步步引导用户补齐关键信息
- **产业翻译官**：把普通人的大白话翻译成"卡点+建议+风险"分析
- **智能匹配引擎**：多维度加权撮合，角色互补 + 品类 + 数量 + 交期
- **4 步发布向导**：选角色 → 选品类 → 填详情 → AI 翻译 + 确认发布

## 灵感来源

| 参考 | 借鉴了什么 |
|---|---|
| 白沟河网（baigouhe.com） | 7 大功能板块分类体系 |
| 智联招聘「职悟空」 | AI 长期记忆 + 主动追问引导的产品逻辑 |
| 传统 BBS 信息门户 | 供需信息流的呈现方式 |

## 技术栈

纯前端，零依赖：

- `index.html` — 页面结构（分类面板 + AI 对话 + 信息流 + 弹窗）
- `styles.css` — 紫色品牌主题 + 深色模式 + 全响应式
- `rules.js` — 核心规则引擎（帖子解析 + AI 翻译 + 智能匹配 + 筛选）
- `app.js` — UI 交互层（AI 追问对话流 + 发布向导 + 状态管理）

## 快速开始

```bash
# 直接打开
open index.html

# 或启动本地服务器
python3 -m http.server 8080
# 访问 http://localhost:8080
```

## 体验路径

1. 点击右侧 AI 助手的「我要放加工订单」→ 体验 AI 追问对话
2. 点击顶部「免费发布信息」→ 体验 4 步 AI 发布向导
3. 点击任意帖子的「查看匹配」→ 查看智能匹配结果
4. 使用筛选栏按角色/品类/数量/交期过滤

## 接真实 LLM

当前 `rules.js` 的 `translate()` 函数使用硬编码规则。要接入真实大模型，只需替换为：

```js
async function translate(p) {
  const resp = await fetch('你的 LLM API 地址', {
    method: 'POST',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify({ prompt: `...` })
  });
  const data = await resp.json();
  return data.cards;
}
```

详见 `ARCHITECTURE.md` 第 5 节。

## 项目结构

```
baigou-ai-matching/
├── index.html         # 主页面
├── styles.css         # 样式
├── rules.js           # 规则引擎
├── app.js             # UI 交互
├── ARCHITECTURE.md    # 架构文档
├── README.md          # 本文件
└── LICENSE            # MIT 协议
```

## 状态

🚧 **MVP v1.0** — 概念验证阶段，后续迭代方向：

- [ ] 接入真实 LLM API
- [ ] 用户登录 & 产业记忆系统
- [ ] 真实数据接入
- [ ] 移动端 PWA 支持
- [ ] 交易担保 & 信用体系

## License

MIT © 2026 Linzhoudream
