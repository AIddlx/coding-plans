# 无问芯穹 (Infini-AI) Coding Plan 记录

## 基本信息

- **记录时间**: 2026年3月28日
- **产品名称**: GenStudio Infini 编码套餐 (Coding Plan)
- **厂商**: 无问芯穹 (Infini-AI)
- **官方网站**: https://cloud.infini-ai.com/platform/ai
- **控制台**: https://cloud.infini-ai.com/
- **文档来源**: 官方平台页面及用户提供的文本资料

---

## 产品概述

Infini Coding Plan 是无问芯穹（Infini-AI）推出的 AI 编程订阅服务，通过单一订阅即可在熟悉的开发工具中使用 DeepSeek、MiniMax、Kimi、GLM 等多家顶尖厂商的主流编程模型。采用"请求次数"计费而非 Token，提供更可预测的成本控制。

### 核心特点

- **多模型聚合**: 集成 DeepSeek、MiniMax、Kimi、GLM 等主流编码模型，一键切换
- **请求次数计费**: 消除 Token 计费的不确定性，成本更可控
- **双协议支持**: 同时兼容 OpenAI 和 Anthropic 协议，工具覆盖全面
- **无速率限制**: 不设置 RPM/TPM/TPD 限制（不同于其通用 LLM API）
- **统一 API 端点**: 一次配置即可在所有主流开发工具中使用
- **多密钥管理**: 支持创建最多 5 个独立 API Key，便于分流统计和安全管理

---

## 套餐详情

### Infini Coding Lite（轻量日常）

| 项目 | 详情 |
|------|------|
| **价格** | ¥40/月（刊例价） |
| **适用场景** | 改 Bug、写脚本、补单测、文档生成等轻量日常开发 |
| **5小时配额** | 1,000 次请求（滑动窗口） |
| **7天配额** | 6,000 次请求（每周一 00:00:00 重置） |
| **30天配额** | 12,000 次请求（每订阅周期第一日 00:00:00 重置） |
| **模型支持** | 所有支持的模型（与 Pro 相同） |
| **目标用户** | 中等强度日常开发者，大多数个人开发者 |

### Infini Coding Pro（高频生产力）

| 项目 | 详情 |
|------|------|
| **价格** | ¥200/月（刊例价） |
| **适用场景** | 复杂排障、架构重构、连续迭代、多人协作等高频生产场景 |
| **5小时配额** | 5,000 次请求（滑动窗口） |
| **7天配额** | 30,000 次请求（每周一 00:00:00 重置） |
| **30天配额** | 60,000 次请求（每订阅周期第一日 00:00:00 重置） |
| **模型支持** | 所有支持的模型（与 Lite 相同） |
| **目标用户** | 高强度工作的专业开发者，复杂项目开发 |

> **额度对比**: Pro 套餐的 5小时额度是 Lite 的 5 倍（5,000 vs 1,000），价格也是 5 倍（¥200 vs ¥40），形成清晰的线性梯度。

---

## 额度刷新机制

Infini Coding Plan 采用 **三重独立额度系统**，各周期互不影响：

| 额度类型 | 刷新机制 | 说明 |
|---------|---------|------|
| **5小时配额** | 滑动窗口 | 统计任意连续5小时内的请求总数，动态刷新。例如10:00使用的额度，15:00释放。 |
| **7天配额（周）** | 固定周期重置 | 每周一 00:00:00 重置，连续统计累计7天内的请求总数。 |
| **30天配额（月）** | 固定周期重置 | 每订阅周期第一日 00:00:00 重置，连续统计累计30天内的请求总数。 |

**重要说明**:
- 三个维度的限额独立计算，任意一个达到上限后，新的请求会被拒绝（HTTP 429）
- 不会自动扣费或转按量计费，需等待对应周期额度恢复
- 滑动窗口机制避免了固定时间点重置的并发拥堵，保障全天候平滑使用

---

## 支持的模型

Infini Coding Plan 集成了多家主流厂商的编码模型，列表随平台更新动态扩展。当前支持的模型包括：

### 文本模型

| 模型 ID | 厂商 | 特点 |
|---------|------|------|
| `deepseek-v3.2` | DeepSeek | 高效推理，通用编码能力 |
| `deepseek-v3.2-thinking` | DeepSeek | 深度思考模式（默认启用 Thinking） |
| `kimi-k2.5` | Moonshot (月之暗面) | 长上下文处理，多模态支持 |
| `minimax-m2.1` | MiniMax | 综合能力强 |
| `minimax-m2.5` | MiniMax | 高速推理 |
| `minimax-m2.7` | MiniMax | 最新主力模型 |
| `glm-4.7` | 智谱AI | 代码生成优化 |
| `glm-5` | 智谱AI | 最新 GLM-5 系列 |

**模型选择**: 可在 Claude Code 中使用 `/model` 命令切换，或在其他工具中直接指定模型 ID。

**注意**: OpenAI 协议与 Anthropic 协议支持的模型可能存在差异，请以控制台"接入信息"栏实时展示的兼容模型列表为准。

---

## 支持的工具与协议

### 协议支持

- **OpenAI 兼容协议**: `https://cloud.infini-ai.com/maas/coding/v1`
  - 支持: `/chat/completions`, `/models`
  - 不支持: `/responses/`
- **Anthropic 兼容协议**: `https://cloud.infini-ai.com/maas/coding`
  - 支持: `/v1/messages`, `/v1/models`

### 📋 已验证工具兼容性矩阵

| 工具名称 | 类型 | 支持协议 | 支持档位 | 备注 |
|---------|------|----------|----------|------|
| **Claude Code** | Anthropic官方 | Anthropic | Lite, Pro | 使用 `/model` 切换 |
| **Cursor** | AI原生编辑器 | OpenAI | Lite, Pro | 需手动添加模型ID |
| **Roo Code / Cline** | VS Code插件 | OpenAI | Lite, Pro | - |
| **Kilo Code** | 轻量级 | OpenAI | Lite, Pro | - |
| **OpenCode** | 开源 | OpenAI | Lite, Pro | - |
| **其他OpenAI/Anthropic协议工具** | - | 双协议 | Lite, Pro | 理论上全部支持 |

**多工具共享额度**: 所有工具共用您订阅套餐的总请求额度。可创建最多 **5 个独立 API Key**，分别配置在不同设备或工具上。

---

## 快速开始指南

---

## 快速开始指南

### 步骤1: 订阅 Coding Plan

1. 访问 [Infini 控制台](https://cloud.infini-ai.com/)
2. 注册/登录账号并完成实名认证
3. 进入 Coding Plan 页面，选择 Lite 或 Pro 套餐
4. 完成支付（刊例价: Lite ¥40/月, Pro ¥200/月）

### 步骤2: 获取专属凭证

1. 前往 **Coding Plan 管理页面**（控制台内）
2. **获取 API Key**:
   - Coding Plan 使用独立密钥体系，以 `sk-cp-` 开头
   - ⚠️ 与 GenStudio 通用 LLM API Key (`sk-` 开头) **不互通**
   - 支持创建最多 5 个独立密钥，建议为不同工具分别配置
3. **获取 API 端点**:
   - OpenAI 兼容: `https://cloud.infini-ai.com/maas/coding/v1`
   - Anthropic 兼容: `https://cloud.infini-ai.com/maas/coding`

### 步骤3: 配置开发工具

#### Claude Code (Anthropic 协议)

**MacOS / Linux**:
编辑 `~/.claude/settings.json`:
```json
{
    "env": {
        "ANTHROPIC_AUTH_TOKEN": "sk-cp-xxxxx",
        "ANTHROPIC_BASE_URL": "https://cloud.infini-ai.com/maas/coding",
        "ANTHROPIC_DEFAULT_HAIKU_MODEL": "minimax-m2.5",
        "ANTHROPIC_DEFAULT_SONNET_MODEL": "minimax-m2.5",
        "ANTHROPIC_DEFAULT_OPUS_MODEL": "minimax-m2.5"
    }
}
```

**Windows (CMD)**:
```cmd
setx ANTHROPIC_AUTH_TOKEN "sk-cp-xxxxx"
setx ANTHROPIC_BASE_URL "https://cloud.infini-ai.com/maas/coding"
setx CLAUDE_CODE_DISABLE_NONESSENTIAL_TRAFFIC 1
setx ANTHROPIC_DEFAULT_HAIKU_MODEL "minimax-m2.5"
setx ANTHROPIC_DEFAULT_SONNET_MODEL "minimax-m2.5"
setx ANTHROPIC_DEFAULT_OPUS_MODEL "minimax-m2.5"
```

#### Cursor / Roo Code / Cline (OpenAI 协议)

- **Base URL**: `https://cloud.infini-ai.com/maas/coding/v1`
- **API Key**: 您的 Coding Plan Key (`sk-cp-xxxxx`)
- **Model ID**: 输入模型名称，如 `deepseek-v3.2`, `minimax-m2.5`, `glm-5`

**注意**: Cursor 预置下拉列表不会自动包含 Infini 支持的第三方模型，需在"Add new model"中手动输入模型 ID。

### 步骤4: 验证与使用

1. 启动配置好的工具（Claude Code / Cursor 等）
2. 执行简单测试，确认连接正常
3. 使用 `/model` 命令（Claude Code）或在界面中选择模型
4. 开始 AI 编程辅助

---

## 使用限制与规范

### ✅ 允许使用场景

- ✅ AI 编程工具（Claude Code、Cursor、Roo Code、OpenCode 等）
- ✅ IDE 插件（通过上述工具集成）
- ✅ 本地开发环境中的编码辅助
- ✅ 多设备使用（最多 5 个独立 API Key）

### ❌ 禁止使用场景

- ❌ **自动化脚本**: 脚本批量调用、定时任务
- ❌ **自建后端服务**: Web API、微服务、后端应用
- ❌ **爬虫**: 数据采集、自动化请求
- ❌ **非交互式调用**: 任何无人值守的 API 调用
- ❌ **团队共享**: Coding Plan 仅限订阅者本人使用，不支持多人共享

### ⚠️ 违规后果

- 检测到异常多用户并发、异地高频调用或非 IDE 场景使用
- 可能触发风控限制，严重时导致订阅停用或账号封禁
- **不予退款**

---

## 重要注意事项

### 1. 额度耗尽处理

当任意维度额度达到上限时：
- 新请求会被拒绝（HTTP 429）
- **不会自动扣费**或转按量计费
- 需等待对应周期额度恢复：
  - 5小时额度: 滑动窗口自动释放
  - 7天额度: 周一 00:00:00 重置
  - 30天额度: 下个订阅周期首日重置
- 如急需使用，可考虑升级套餐或等待恢复

### 2. 账号与密钥管理

- **专享使用**: 仅限订阅者本人，不支持团队共享
- **多密钥**: 最多创建 5 个独立 API Key，便于不同设备/工具配置
- **安全**: 妥善保管 Key，避免泄露；支持紧急吊销
- **风险**: 虽然允许多 Key，但若检测到多用户共享或滥用行为，仍可能触发风控

### 3. 与 GenStudio 通用 API 的区别

| 项目 | Coding Plan | GenStudio 通用 LLM API |
|------|-------------|------------------------|
| **计费单位** | 请求次数 | Token 数量 |
| **适用场景** | IDE 编码工具 | 应用开发、API 集成 |
| **速率限制** | 无 RPM/TPM/TPD | 有速率限制 |
| **API Key 格式** | `sk-cp-...` | `sk-...` |
| **Base URL** | 专用端点 | 通用端点 |
| **互操作性** | ❌ 不互通 | ❌ 不互通 |

⚠️ **重要**: 在 IDE 中必须使用 Coding Plan 专属 Key 和 Base URL，否则将无法使用套餐额度或产生额外按量计费。

### 4. 模型切换与 Thinking 模式

- **Claude Code**: 对话期间执行 `/model` 命令切换
- **Cursor**: 在聊天窗口模型下拉菜单选择（需先手动添加模型 ID）
- **Thinking 模式**:
  - DeepSeek v3.2-thinking 模型默认启用 Thinking
  - 其他模型需通过工具配置（如 Claude Code 的 `/config` 设置 `Thinking mode: true`）

### 5. 多模态支持

- `kimi-k2.5` 支持多模态（图片输入，Base64 编码）
- `minimax-m2.1/m2.5/m2.7`, `glm-4.7/glm-5` 为纯文本模型，不支持图片

### 6. 常见错误排查

| 错误 | 可能原因 | 解决方案 |
|------|---------|---------|
| 401 / 404 | API Key 或 Base URL 错误 | 确认使用 `sk-cp-` 开头的 Key 和专用端点 |
| 405 | 协议不支持该模型 | 检查工具使用的协议（OpenAI/Anthropic）与模型兼容性 |
| 429 | 额度已达上限 | 等待额度恢复或升级套餐 |
| 500 | 服务端错误 | 稍后重试或联系客服 |
| "invalid value: developer" | 工具使用了新版 developer 角色 | 在工具设置中将 `supportsDeveloperRole` 设为 `false` |
| Claude Code "AuthenticationError" | 本地已有其他 Anthropic 配置 | 先 `/logout`，确保 `ANTHROPIC_API_KEY` 为空 |

---

## 额度查询与用量监控

### 控制台查看

访问 [Coding Plan 管理页面](https://cloud.infini-ai.com/)，实时查看：
- 5小时用量与剩余
- 7天用量与剩余
- 30天用量与剩余
- 套餐有效期

### API 查询

```bash
curl -X GET --location 'https://cloud.infini-ai.com/maas/coding/usage' \
  --header 'Authorization: Bearer sk-cp-xxxxx'
```

响应示例:
```json
{
  "5_hour": {"quota": 5000, "used": 0, "remain": 5000},
  "7_day": {"quota": 6000, "used": 0, "remain": 6000},
  "30_day": {"quota": 12000, "used": 0, "remain": 12000}
}
```

### 用量统计页面

- 登录控制台，进入"用量统计"页面
- 切换到大语言模型标签页
- 按用户与 API Key 筛选查看调用数据
- ⚠️ 非实时数据，整点后 5 分钟更新（如 10:00 的数据在 11:05 更新）

---

## 订阅管理

### 升级套餐

- 支持从 Lite 升级到 Pro
- Lite 套餐有效期不足 7 天时，不支持直接升级，需先续费再升级
- 升级后：
  - 订阅周期不变（起止日不变）
  - 退还剩余天数 Lite 费用（按 Lite 日均价）
  - 补收 Pro 差价（按 Pro 日均价）
  - 所有额度（5h/7d/30d）立即切换为 Pro 额度
  - 已用额度继续累计
- Pro 有效期内不支持降级

### 续费与自动续费

- 支持自动续费（防止断线）
- 支持手动续费，优先消耗手动续费时长
- 可随时在"订阅管理"页面取消自动续费（需在下一个扣费日前至少 72 小时操作）

### 退款政策

- **不支持退款**
- 订阅服务属于数字化商品，一经购买（或自动续费）即视为服务已交付
- 即使未使用完，费用也无法退回
- 建议首次使用选择 Lite 月付体验，满意后再选更高档位或长期订阅

---

## 常见问题摘要

### 计费相关

- **Q**: 额度是按请求次数还是 Token 计算？
  - **A**: 按**请求次数 (Requests)** 计算，而非 Token。一次 IDE 操作可能触发多次请求，但成本更可控。

- **Q**: 有 RPM/TPM/TPD 限制吗？
  - **A**: **没有**。Coding Plan 不同于 GenStudio 通用 LLM API，不设置速率限制。

- **Q**: 达到配额后会怎样？
  - **A**: 请求被拒绝（429），**不会自动扣费**。需等待额度恢复或升级套餐。

- **Q**: 额度用完了怎么办？
  - **A**: 等待刷新，或创建新租户/用户购买新套餐（不支持在同一账号下叠加）。

### 使用相关

- **Q**: 可以在多台设备或多个工具中同时使用吗？
  - **A**: 可以。最多创建 5 个独立 API Key，但**所有工具共享总额度**。

- **Q**: 可以供团队多人共享吗？
  - **A**: **不可以**。仅限订阅者本人使用。检测到多用户并发或异地高频调用可能触发风控。

- **Q**: 可以用在自建应用或后端服务吗？
  - **A**: **不可以**。仅限 IDE 编码工具中的交互式使用。非 IDE 场景可能导致订阅停用。

- **Q**: Coding Plan Key 和 GenStudio 通用 Key 通用吗？
  - **A**: **不通用**。必须使用 `sk-cp-` 开头的 Coding Plan 专属 Key 和专用 Base URL。

### 模型与工具

- **Q**: 支持哪些模型？
  - **A**: DeepSeek (v3.2/v3.2-thinking), Kimi (k2.5), MiniMax (m2.1/m2.5/m2.7), GLM (4.7/5)。列表动态更新，以控制台为准。

- **Q**: 支持哪些编程工具？
  - **A**: 理论上支持所有 OpenAI/Anthropic 兼容工具。已验证: Claude Code, Cursor, Roo Code/Cline, Kilo Code, OpenCode。

- **Q**: 如何切换模型？
  - **A**: Claude Code 用 `/model` 命令；Cursor 在聊天窗口选择（需手动添加模型 ID）。

- **Q**: 支持 Thinking 模式吗？
  - **A**: 支持。DeepSeek v3.2-thinking 默认启用；其他模型需通过工具配置。

---

## 参考资源

### 官方文档与入口

- [Infini 控制台](https://cloud.infini-ai.com/)
- [Coding Plan 管理页面](https://cloud.infini-ai.com/platform/ai)
- [使用文档](https://cloud.infini-ai.com/docs/getting-started)

### 相关链接

- GenStudio 平台首页: https://cloud.infini-ai.com/
- 飞书交流群: 见控制台公告

---

## 更新记录

| 日期 | 说明 |
|------|------|
| 2026-03-28 | 初始记录，基于官方页面信息整理 |

---

## 备注

1. **信息完整性**: 本记录基于用户提供的官方页面文本整理，部分细节（如具体 API 端点路径、模型列表）建议以控制台实时显示为准
2. **价格确认**: Lite ¥40/月, Pro ¥200/月 为刊例价，实际购买时请确认是否有活动优惠
3. **额度机制**: 三重独立额度（5h/7d/30d）是独特设计，需注意任一维度超限都会导致请求拒绝
4. **无速率限制**: Coding Plan 不设 RPM/TPM/TPD，相比其他厂商可能有优势
5. **多模型聚合**: 支持 DeepSeek、MiniMax、Kimi、GLM 等主流模型，切换灵活
6. **使用限制**: 仅限个人 IDE 编码场景，严禁自动化或团队共享，违规可能导致封号
7. **与竞品对比**: 定价（¥40/¥200）和额度（12k/60k 月额度）与主流厂商 Lite/Pro 档接近，但采用请求次数而非 Token 或 Prompt 计费

---

**记录人**: Sisyphus (AI Agent)
**记录方式**: 基于官方页面信息整理
**验证状态**: ⚠️ 建议购买前到官网控制台核实最新信息
