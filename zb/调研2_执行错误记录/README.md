# 调研 2 执行错误记录 · 总入口

> **创建时间**：调研 2 补充轮
> **目的**：记录 Phase 2 调研中所有**真实**的调用错误、工具限制、缺失数据，便于团队成员亲自验证和补做
> **配合文档**：`调研2.md`（主调研报告）
> **诚实原则**：本文件夹**所有记录都是真实失败**，不掩盖、不夸大、不编造

---

## 文件结构

| 文件 | 内容 | 何时用 |
|---|---|---|
| [`错误清单_网络和工具.md`](./错误清单_网络和工具.md) | 所有网络连接错误、工具能力限制、subagent 失败、paywall 阻挡 | 想了解"为什么没拿到某些数据" |
| [`数据缺口清单.md`](./数据缺口清单.md) | Phase 2 没拿到的关键数据 + 可直接复制的补做命令 | 准备补做时 |
| [`补充调研发现_v0.2.md`](./补充调研发现_v0.2.md) | 本轮补充搜索的新发现 + 9 假设矩阵更新 + 比赛调整 | 想看新内容时 |

---

## 关键结论（TL;DR）

### 调研 2 在当前环境无法获得 30 段可引用的 Reddit 直接原话

**4 类失败**：

1. ❌ 当前会话**完全没有 outbound 网络访问**（已实际测试 reddit.com / guardian.com / arxiv.org / duckduckgo.com 全部失败）
2. ❌ `web_search` **只能返回 URL + 标题 + snippet**，**不能抓取页面正文**
3. ❌ Subagent **同样无网络访问权限**（自报"curl 报 SEC_E_NO_CREDENTIALS"）
4. ❌ 部分关键文章被 paywall 阻挡（Atlantic / 部分 Chalkbeat 内容）

### 但调研 2 仍有价值

虽然无法获得直接原话，本次调研**仍然采集到**：

- ✅ 多个独立 aggregator 文章信号（30+ 个 URL）
- ✅ 反向证据信号（出乎意料地强）
- ✅ 学术研究入口（arxiv 2406.10461 + 2510.24070）
- ✅ 实际存在的 homeschool + AI 播客
- ✅ 第一人称 homeschool 妈妈正面案例（Ivana Greco）
- ✅ 中国 AI 玩具的负面事件报道（Today.com）

**关键意外发现**：**反向证据信号比支持信号强得多**——这改变了整个产品定位的风险评估。

---

## 团队必须补做的（按优先级）

### P0（立即）：抓真实原话

```bash
# 用能访问外网的机器执行
curl -A "research-bot/1.0" "https://www.reddit.com/r/homeschool/search.json?q=finished+curriculum&restrict_sr=on&limit=25&sort=relevance" > r_homeschool_finished.json
curl -A "research-bot/1.0" "https://www.reddit.com/r/Gifted/search.json?q=bored+school&restrict_sr=on&limit=25&sort=relevance" > r_gifted_bored.json
curl -A "research-bot/1.0" "https://www.reddit.com/r/Parenting/search.json?q=AI+kids+concerned&limit=25&sort=relevance" > r_parenting_ai.json
curl -A "research-bot/1.0" "https://www.reddit.com/r/2e_school/search.json?q=struggle&restrict_sr=on&limit=25&sort=relevance" > r_2e_school.json
```

### P1（24 小时内）：下载 PDF + 读 aggregator 文章正文

- 下载 NCES 2024-113 PDF：https://archive.org/details/ERIC_ED659476
- 浏览器读 arxiv 2510.24070（含家长直接引用）
- 浏览器读 Today.com AI 玩具报道（中国团队出海关键风险）
- 浏览器读 Ivana Greco "AI is a Homeschooling Tool"（正面案例）

### P2（Phase 3 设计时）：调整访谈问题

新增关于"中国团队 AI 信任度"问题、关于"AI 玩具事件认知"问题。

---

## 维护原则

1. **不掩盖失败**：任何工具调用失败都要如实记录
2. **不编造数据**：宁可标"未找到"也不用估算
3. **团队可复现**：所有命令、URL、错误信息都完整保留
4. **诚实优先**：调研推翻叙事 > 调研支持叙事

---

> **本文件夹状态**：v0.2 补充调研时建立
> **维护**：每次新调研轮次后更新
