# ESA 浅查结果 · v0.1

> **调研时间**：本会话（约 30 分钟）
> **调研方式**：web_search（环境无 outbound 网络，仅返回 snippet + URL）
> **调研深度**：浅（C 选项）
> **配套文档**：`zb/ESA知识库.md`

---

## 一、调研方法

### 1.1 搜索词（4 组）
- `Arizona Empowerment Scholarship Account ESA approved vendors list 2024 2025`
- `Arizona ESA AI education software subscription approved eligible`
- `Arizona ESA application process become vendor education provider`
- `Empowerment Scholarship Account other states Florida Tennessee West Virginia list`

### 1.2 找到的关键 URL（5 个核心）

| # | URL | 内容 |
|---|---|---|
| 1 | https://www.schoolchoiceusa.org/esa-vendors/arizona | **Arizona ESA Approved Vendors 列表** |
| 2 | https://homeschoolstartguide.com/blog/arizona-esa-vendor-registration | **如何成为 Arizona ESA vendor** |
| 3 | https://homeschoolstartguide.com/blog/arizona-esa-approved-expenses | **Arizona ESA Approved Expenses** |
| 4 | https://app.smartsheet.com/b/form/f0dea2798798406fbe43c835cf38fbb3 | **Arizona Dept of Education Service Provider Registration** |
| 5 | https://www.esatrackerbystate.com/compare | **State ESA Tracker**（可对比 50 州） |

### 1.3 辅助 URL
- https://www.lumosarts.com/esa（Lumos Arts Academy 被批为 vendor 案例）
- https://www.cavecreekmusicacademy.com/arizona-esa-music-lessons（音乐课被批案例）
- https://grandcanyontimes.com/foia-request-sent-to-state-of-arizona-department-of-education-regarding-esa-program-records-on-july-11-2025（FOIA 申请案例）
- https://www.prodigygame.com/main-en/blog/arizona-esa-homeschool-chandler（Chandler homeschool ESA 全额资助）

---

## 二、关键发现

### 2.1 ✅ Arizona ESA 流程清晰、可成为 vendor

**注册路径**：
1. 提交 **Service Provider Registration** 表单（smart sheet form）
2. 通过审批
3. 加入 approved vendors 列表
4. 家庭通过 ESA 资金直接支付 vendor

**关键文档**：`Arizona ESA Service Provider Registration Form`

### 2.2 ⚠️ AI 软件订阅类是否在批准清单：未明

**已知被批准的类别**（从公开文章看到）：
- 私立学校学费
- 音乐课 / 艺术课程
- homeschool 教材
- 辅导服务
- 特殊教育服务
- 评估测试

**未知**：
- AI 对话 / 订阅类是否在标准批准清单
- 是否需要走特殊申请流程
- 是否有 AI 类 vendor 案例

### 2.3 ✅ 多州 ESA 对比工具有

**State ESA Tracker** (https://www.esatrackerbystate.com/compare)：
- 50 州 ESA 对比
- 各州资金规模 / 适用人群 / 合规要求
- 可作为 Q1 50 州调研的起点

### 2.4 ⚠️ 凤凰城 Chandler ESA 普及度

`prodigygame.com` 文章提到 Chandler homeschool 可获 ESA 全额资助——这意味着凤凰城东谷确实是 ESA 高密度区。

但**具体数据**（参与率、ESA 家庭总数、收入区间）仍需深查。

---

## 三、对商业模型的影响

### 3.1 MVP 阶段 ESA 不可行的判断（仍然成立）

**理由**：
- 浅查 1 小时**未发现** AI 软件订阅类被批准的公开案例
- Service Provider Registration 表单可能要求"教学目标 + 学习成果"
- AI 对话产品的"学习成果"难量化（`zb/ESA知识库.md` §3.1 已分析）

**建议维持原判断**：MVP 跑通直订阅，6-12 个月后再申请 ESA vendor。

### 3.2 但 ESA 仍是远景优势

**理由**：
- 流程清晰可走（不是黑箱）
- 多州可扩展（State ESA Tracker 提供对比工具）
- ESA 家庭的"已付费"特征不变（即使不走 ESA 通道，他们仍有付费习惯）

**建议**：保留 ESA 作为远景支付通道，不作为 MVP 障碍。

---

## 四、待深查项（如果未来要做 ESA）

| 任务 | 时间 | 优先级 |
|---|---|---|
| 完整浏览 schoolchoiceusa.org/esa-vendors/arizona | 1 小时 | P0（需确认 AI 类） |
| 联系 1-2 个已批准的 AI / 软件类 vendor 询问经验 | 2-3 天 | P1 |
| 完整阅读 Arizona ESA Approved Expenses 列表 | 1 小时 | P0 |
| 下载并阅读 Service Provider Registration 表单全文 | 1 小时 | P1 |
| 用 State ESA Tracker 对比 AZ / FL / WV / TN / MS / NC | 2 小时 | P2 |
| 联系 Arizona ESA 管理办公室确认 AI 类申请可行性 | 1-2 周 | P2 |

---

## 五、对决策的影响

### 5.1 不影响现有决策
- 决策 4（付费模型 = A 双轨）保持不变
- MVP 走直订阅 / 远景走 ESA 的策略不变

### 5.2 但增强了对 ESA 远景的信心
- 流程明确
- 多州可扩展
- 浅查未发现"绝对不可行"的硬证据

### 5.3 需要更新 ESA 知识库
- 添加 5 个核心 URL
- 更新 §2.2 未知部分（流程已部分明确）

---

> **本文件状态**：v0.1 ESA 浅查结果
> **下次深查建议**：当团队决定 6-12 个月后启动 ESA 申请时使用
