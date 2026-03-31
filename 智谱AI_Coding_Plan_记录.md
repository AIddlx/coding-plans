# 智谱AI GLM Coding Plan 记录

## 基本信息

**访问时间**: 2026年3月28日
**来源**:
- [套餐概览](https://docs.bigmodel.cn/cn/coding-plan/overview)
- [GLM Coding官网](https://www.bigmodel.cn/glm-coding)
- [快速开始](https://docs.bigmodel.cn/cn/coding-plan/quick-start)
- [使用须知](https://docs.bigmodel.cn/cn/coding-plan/usage-notes)

## 产品概述

GLM Coding Plan是智谱AI专为AI编码打造的订阅套餐，仅需少量投入，即可在主流AI编码工具中畅享智谱高智能模型。支持Claude Code、Kilo Code、OpenClaw、OpenCode、TRAE、CodeBuddy等20+编程工具。

### 核心特点

- **Prompt-based计费**: 独特采用"prompt"作为计费单位（非API请求次数，非Token）
- **双维度限额**: 5小时限额 + **周限额**，平衡使用与成本
- ⚠️ **周限额重要提示**: 新套餐（2月12日起）有周限额，老套餐（2月12日前订阅+续订）**无周限额**且额度更高（1.5倍）
- **独家MCP生态**: 提供视觉理解、联网搜索、网页读取、开源仓库MCP工具
- **专属扩展**: GLM in Excel (Beta) - 直接在Excel中使用GLM
- **高速响应**: 55+ Tokens/秒生成速度
- **旗舰模型**: 支持GLM-5.1、GLM-5等最新模型

---

### 📊 套餐对比总览（新老套餐）

| 对比项 | Lite 套餐 | Pro 套餐 | Max 套餐 |
|-------|-----------|----------|----------|
| **新套餐原价** | ¥49/月 | ¥149/月 | ¥469/月 |
| **老套餐原价** | ¥40/月 | ¥200/月 | ¥400/月 |
| **新套餐连续包年** | ¥39.2/月（8折） | ¥119.2/月（8折） | ¥375.2/月（8折） |
| **5小时额度（新）** | ~80 prompts | ~400 prompts | ~1,600 prompts |
| **5小时额度（老）** | ~120 prompts（1.5倍） | ~600 prompts（1.5倍） | ~2,400 prompts（1.5倍） |
| **周限额（新）** | ~400 prompts | ~2,000 prompts | ~8,000 prompts |
| **周限额（老）** | ❌ 无 | ❌ 无 | ❌ 无 |
| **月总额度（新）** | ⚠️ ~1,600 prompts<br>（推算值，受周限额约束） | ⚠️ ~8,000 prompts<br>（推算值，受周限额约束） | ⚠️ ~32,000 prompts<br>（推算值，受周限额约束） |
| **月总额度（推算，×15）** | ⚠️ ~24,000次<br>（周×4推算，非官方确认） | ⚠️ ~120,000次<br>（周×4推算，非官方确认） | ⚠️ ~480,000次<br>（周×4推算，非官方确认） |
| **MCP额度（新）** | 100次/月 | 1,000次/月 | 4,000次/月 |
| **适用场景** | 轻度使用 | 中度到重度 | 重度/企业级 |
| **关键提示** | 老用户**无周限额**且额度1.5倍 | 老用户**无周限额**且额度1.5倍 | 老用户**无周限额**且额度1.5倍 |

**老用户锁定权益**: 2026年2月12日前订阅且开启续费的用户，价格和额度保持不变，不受新规则影响。

### 新老套餐核心差异总结

| 维度 | 老套餐（已停止） | 新套餐（当前） |
|------|------------------|----------------|
| **价格** | ¥40/200/400 | ¥49/149/469（涨价30%+） |
| **5小时额度** | 更高（1.5倍） | 较低 |
| **周限额** | 无 | 有（约13-23倍月费） |
| **折扣** | 首购5折 | 连续包季9折/包年8折 |
| **功能** | 完全相同 | 完全相同 |
| **新用户** | 无法购买 | 只能购买新套餐 |

**关键结论**:
- ✅ **老套餐性价比更高**: 1.5倍额度 + 无周限额
- ✅ **老用户锁定权益**: 2026-02-12前订阅且开启续订的用户，价格和额度保持不变
- ⚠️ **新用户适用新套餐**: 价格更低（Pro从¥200→¥149）但额度减少且有周限额

---

### ⚠️ 重要说明：月额度推算与周限额约束

**关于月总额度的特别提示**：

官方仅明确公布**5小时额度**和**周限额**，**未直接公布月总额度**。文档中出现的"月额度"数值为基于周额度按4周推算的理论值：

- **推算公式**: 月额度 ≈ 周额度 × 4
- **⚠️ 关键限制**: 由于新套餐存在**周限额**，实际月可用量受周额度约束：
  - **均匀使用模式**: 月可用量 ≈ 周额度 × 4（可接近推算值）
  - **不均匀使用模式**: 周额度可能先达到上限，实际月可用量**低于**推算值
- **老用户例外**: 2026年2月12日前订阅且开启续费的用户**不受周限额限制**，额度为1.5倍，实际可用量更高

**购买建议**：
- 新用户需评估自身使用模式：如果某几天集中高强度使用，周限额可能成为瓶颈
- 重度用户建议考虑老用户权益或选择无周限额的厂商（如阶跃星辰）

---

- **1 prompt ≈ 15-20次标准请求**
- 实际可用量受项目复杂度、代码库大小、是否启用自动接受等因素影响
- 每月可用额度相当于月订阅费的**15-30倍**（已计入周限额影响）
- ⚠️ **高峰期消耗加倍**: GLM-5.1、GLM-5、GLM-5-Turbo作为高阶模型：
  - 高峰期（14:00-18:00 UTC+8）消耗为**3倍**
  - 非高峰期消耗为**2倍**
  - **限时福利（至4月底）**: 非高峰期仅**1倍**消耗

### 📈 周限额详解

新套餐执行每周使用额度限制：
- **周额度计算**: 约为套餐月订阅费用的 **13-23倍**（按API定价）
- **刷新规则**: 以7天为周期，额度在周期开始时刷新重置
- **监控方式**: 可在[用量统计](https://www.bigmodel.cn/usercenter/glm-coding/usage)中查看周额度消耗进度

**老套餐用户特权**:
> ✅ 2026年2月12日之前订阅且开启自动续费的用户，**不受周限额限制**，额度保持不变。

### 💡 额度优化建议

**模型选择策略**:
- **GLM-4.7** (对标 Claude Sonnet): 日常开发、常规任务 → **1倍消耗**
- **GLM-5** (对标 Claude Opus): 复杂推理、大型工程任务 → **2-3倍消耗**

**时间选择策略**:
- 非高峰期使用 GLM-5.1/5-Turbo 可节省额度（限时福利至4月底仅1倍）
- 高峰期（14:00-18:00）避免使用高阶模型

---

> 2026年2月12日之前订阅且开启自动续费的用户，在订阅有效期内**不受周限额限制**，额度保持不变，续费价格及用量也不变。

---

## MCP工具附加额度

智谱AI Coding Plan独家提供4种MCP工具，各套餐额度不同：

| 套餐 | 联网搜索MCP<br>+ 网页读取MCP<br>+ 开源仓库MCP | 视觉理解MCP |
|------|-----------------------------------------------|-------------|
| Lite | 100次/月（合计） | 与模型共享5小时prompt池 |
| Pro | 1,000次/月（合计） | 与模型共享5小时prompt池 |
| Max | 4,000次/月（合计） | 与模型共享5小时prompt池 |

 达到上限后，相关MCP当月无法继续调用。

---

## 使用条件与限制

### ✅ 允许的使用场景
- 仅在支持的编程工具中使用（Claude Code、Cursor、Kilo Code等）
- 正常的编码辅助任务（代码生成、补全、解释、重构等）

### ❌ 禁止的使用场景
- 批量自动化脚本
- 自建后端服务
- 非编程相关的通用对话
- 违反公平使用条款的行为

### 并发与速率限制
- 套餐用户的并发限制与套餐等级相关: **Max > Pro > Lite**
- 高峰期（14:00-18:00 UTC+8）集群流量过大时，可能触发动态限流策略
- 仍遵循并发数 Max > Pro > Lite 的基本原则
- 命中风控规则可能导致高强度限流、冻结或封禁（3次以上违反将封号）
- 可在[套餐总览](https://www.bigmodel.cn/usercenter/glm-coding/subscribe)页面查看风控提示并申请解除

### 购买限制（限售）
- 因用户量激增，短期限售处理
- **限售时间**: 每日 10:00 释放新库存
- Lite、Pro、Max 每日可售数量相同
- **不受限售影响**: 开启续订或在订阅有效期内升级套餐的用户

---

## 常见问题与故障排除

## 支持的模型

### 所有套餐通用
- GLM-5.1
- GLM-5-Turbo
- GLM-4.7
- GLM-4.6
- GLM-4.5
- GLM-4.5-Air

### Pro/Max专享
- **GLM-5**（更高智能等级，对标 Claude Opus）

### 📅 GLM-5 支持计划
- ✅ **Max & Pro 套餐**: 当前已支持 GLM-5
- 🔄 **Lite 套餐**: 待新老模型资源迭代完成后支持（敬请期待）
- ℹ️ 所有套餐现阶段均支持 GLM-4.7 及历史模型

> **注意**: 调用 GLM-5 将占用更多额度（高峰期3倍，非高峰期2倍，限时福利至4月底非高峰1倍）。建议复杂任务使用GLM-5，日常任务使用GLM-4.7以节省额度。

### 模型消耗系数
| 模型 | 高峰期系数 | 非高峰期系数 | 限时福利（至4月底） |
|------|------------|--------------|---------------------|
| GLM-4.7系列 | 1x | 1x | 1x |
| GLM-5.1 / GLM-5-Turbo | 3x | 2x | **1x** |
| GLM-5 | 未明确 | 未明确 | 未明确 |

---

## 快速开始

### 步骤1: 订阅套餐
- 访问[智谱AI GLM Coding页面](https://www.bigmodel.cn/glm-coding)
- 选择 Lite / Pro / Max 套餐（注意每日10:00限售，新库存释放）
- 选择付费方式：连续包季（9折）或连续包年（8折）更划算
- 完成支付

### 步骤2: 获取API Key
- 访问[控制台用量页面](https://www.bigmodel.cn/usercenter/glm-coding/usage)
- 复制专属API Key（仅显示一次，请妥善保存）

### 步骤3: 配置Coding Agent

**Base URL配置** (必须正确选择):
| 工具 | Base URL |
|------|----------|
| Claude Code | `https://open.bigmodel.cn/api/anthropic` |
| Cherry Studio | `https://open.bigmodel.cn/api/coding/paas/v4/` |
| 其他工具 (Open Code, Cline, Kilo Code等) | `https://open.bigmodel.cn/api/coding/paas/v4` |

**Claude Code配置示例** (`~/.claude/settings.json`):

根据官方套餐变更指南，推荐配置如下：

```json
{
  "env": {
    "ANTHROPIC_AUTH_TOKEN": "your_zhipu_api_key",
    "ANTHROPIC_BASE_URL": "https://open.bigmodel.cn/api/anthropic",
    "API_TIMEOUT_MS": "3000000",
    "CLAUDE_CODE_DISABLE_NONESSENTIAL_TRAFFIC": 1,
    "ANTHROPIC_DEFAULT_OPUS_MODEL": "glm-5",
    "ANTHROPIC_DEFAULT_SONNET_MODEL": "glm-4.7",
    "ANTHROPIC_DEFAULT_HAIKU_MODEL": "glm-4.5-air"
  }
}
```

**字段说明**:
- `ANTHROPIC_AUTH_TOKEN`: 智谱AI Coding Plan的API Key
- `ANTHROPIC_BASE_URL`: 必须为智谱AI的Claude协议地址
- `API_TIMEOUT_MS`: 超时设置为3000秒（50分钟）
- `CLAUDE_CODE_DISABLE_NONESSENTIAL_TRAFFIC`: 禁用非必要流量以节省额度
- `ANTHROPIC_DEFAULT_OPUS_MODEL`: 复杂任务使用 **GLM-5** (对标Opus)
- `ANTHROPIC_DEFAULT_SONNET_MODEL`: 普通任务使用 **GLM-4.7** (对标Sonnet)
- `ANTHROPIC_DEFAULT_HAIKU_MODEL`: 简单任务使用 **GLM-4.5-Air** (对标Haiku)

**模型映射策略**:
- 通过设置不同层级的默认模型，可自动根据任务复杂度选择合适模型
- 手动修改这三个字段即可在GLM-5/4.7/4.5-Air间切换
- 无需在控制台单独配置模型（使用套餐默认模型即可）

---

**切换特定模型** (如GLM-5.1):
- 在[控制台套餐订阅页](https://www.bigmodel.cn/usercenter/glm-coding/subscribe)配置
- 修改后约2-3分钟生效
- 在工具中设置模型名为 `GLM-5.1`、`GLM-5-Turbo` 或 `GLM-5`

### 步骤4: 开始使用并监控
- 启动Coding Agent开始编码
- 查看[用量统计](https://www.bigmodel.cn/usercenter/glm-coding/usage)监控prompt消耗
- 查看[套餐总览](https://www.bigmodel.cn/usercenter/glm-coding/subscribe)管理订阅和风控状态

### 步骤5: 管理订阅
- **取消自动续费**: [我的编程套餐](https://www.bigmodel.cn/usercenter/glm-coding/subscribe) → 取消订阅（需在扣费日前至少3天）
- **升级套餐**: 在有效期内升级不受限售影响
- **查看费用明细**: [费用明细](https://www.bigmodel.cn/usercenter/glm-coding/billing) 查看资源包抵扣

---

## 支持的工具

### 📋 工具兼容性矩阵（20+ 工具）

| 工具名称 | 类型 | 支持协议 | 支持套餐 | 备注 |
|---------|------|----------|----------|------|
| **Claude Code** | Anthropic官方 | Anthropic | Lite, Pro, Max | 官方推荐 |
| **Open Code** | 开源 | OpenAI | Lite, Pro, Max | - |
| **Cline** | VS Code插件 | OpenAI | Lite, Pro, Max | - |
| **Factory Droid** | 开源 | OpenAI | Lite, Pro, Max | - |
| **Kilo Code** | 轻量级 | OpenAI | Lite, Pro, Max | - |
| **Roo Code** | VS Code插件 | OpenAI | Lite, Pro, Max | - |
| **Crush** | 开源 | OpenAI | Lite, Pro, Max | - |
| **Goose** | 开源 | OpenAI | Lite, Pro, Max | - |
| **Cursor** | AI原生编辑器 | OpenAI | Lite, Pro, Max | - |
| **Gemini CLI** | Google | OpenAI | Lite, Pro, Max | - |
| **Grok CLI** | xAI | OpenAI | Lite, Pro, Max | - |
| **Cherry Studio** | 桌面应用 | OpenAI | Lite, Pro, Max | - |

**总计**: 20+ 工具持续扩展中

### MCP工具支持（独家优势）

| MCP工具 | 功能 | Lite | Pro | Max |
|---------|------|------|-----|-----|
| **联网搜索MCP** | 网络搜索能力 | 100次/月 | 1,000次/月 | 4,000次/月 |
| **网页读取MCP** | 网页内容提取 | 与搜索MCP共享额度 | 与搜索MCP共享额度 | 与搜索MCP共享额度 |
| **开源仓库MCP** | GitHub等仓库读取 | 与搜索MCP共享额度 | 与搜索MCP共享额度 | 与搜索MCP共享额度 |
| **视觉理解MCP** | 图片分析 | ✅ | ✅ | ✅ |
| **GLM in Excel** | Excel插件 | Beta | Beta | Beta |

> **⚠️ 重要使用条件**: 
> - 只能在上述指定工具中使用
> - 必须配置正确的 Base URL（见下文）
> - 违规使用（如批量任务、自建后端）将触发风控

---

根据官方文档，支持的编程工具包括：

**Coding Agents**:
- Claude Code
- Open Code
- Cline
- Factory Droid
- Kilo Code
- Roo Code
- Crush
- Goose
- Cursor
- Gemini CLI
- Grok CLI
- Cherry Studio

**总计**: 20+ 工具持续扩展中

> **⚠️ 重要使用条件**: 
> - 只能在上述指定工具中使用
> - 必须配置正确的 Base URL（见下文）
> - 违规使用（如批量任务、自建后端）将触发风控

---

## 常见问题与故障排除

### Q1: 购买了编码套餐为什么还报错"1113余额不足"？为什么扣账号余额？

**原因**: 未满足GLM Coding Plan的使用条件，系统自动从账号余额扣费。

**排查要点**:
1. ✅ 必须在**支持的工具**中使用（Claude Code、Open Code、Cline、Factory Droid、Kilo Code、Roo Code、Crush、Goose、Cursor、Gemini CLI、Grok CLI、Cherry Studio）
2. ✅ 必须配置**正确的Base URL**：
   - Claude Code: `https://open.bigmodel.cn/api/anthropic`
   - Cherry Studio: `https://open.bigmodel.cn/api/coding/paas/v4/`
   - 其他工具: `https://open.bigmodel.cn/api/coding/paas/v4`
3. ✅ 套餐在有效期内且未用完额度

**如何查看是否使用了编码套餐抵扣？**
- 访问[费用明细](https://www.bigmodel.cn/usercenter/glm-coding/billing)页面
- 查看"资源包抵扣"列

### Q2: 套餐支持哪些模型？如何切换？

**所有套餐通用**: GLM-5.1、GLM-5-Turbo、GLM-4.7、GLM-4.6、GLM-4.5-Air
**Pro/Max专享**: GLM-5

**切换方法**: 在Coding Agent的自定义配置中（如Claude Code的 `~/.claude/settings.json`），手动修改模型为 `GLM-5.1`、`GLM-5-Turbo` 或 `GLM-5`。

### Q3: 高阶模型（GLM-5.1）消耗额度规则？

- **高峰期** (14:00-18:00 UTC+8): **3倍** 消耗
- **非高峰期**: **2倍** 消耗
- **限时福利（至4月底）**: GLM-5.1/GLM-5-Turbo在非高峰期仅**1倍**消耗
- **建议**: 复杂任务用GLM-5系列，普通任务用GLM-4.7以节省额度

### Q4: 如何取消自动续费？

- 访问[我的编程套餐](https://www.bigmodel.cn/usercenter/glm-coding/subscribe)页面
- 取消订阅自动续费
- ⚠️ 务必在**下一个扣费日至少3天前**取消，以避免自动续费
- 取消后，当前周期继续有效，到期后不再续费

### Q5: 为什么感觉并发只有1？

- 套餐并发限制: **Max > Pro > Lite**
- 高峰期集群流量大时，可能动态限流
- 如命中风控规则，可能被限流/冻结/封禁
- 可在[套餐总览](https://www.bigmodel.cn/usercenter/glm-coding/subscribe)查看风控提示

---

1. **订阅套餐**
   - 访问[智谱AI GLM Coding页面](https://www.bigmodel.cn/glm-coding)
   - 选择Lite/Pro/Max套餐并完成支付
   - 在控制台管理订阅

2. **获取API Key**
   - 进入[控制台用量页面](https://www.bigmodel.cn/usercenter/glm-coding/usage)
   - 获取专属API Key

 3. **配置工具**
    - 在支持的Coding Agent中配置API Key和Base URL
    - **Base URL** (根据工具选择):
      - Claude Code: `https://open.bigmodel.cn/api/anthropic`
      - Cherry Studio: `https://open.bigmodel.cn/api/coding/paas/v4/`
      - 其他工具 (Open Code, Cline, Kilo Code等): `https://open.bigmodel.cn/api/coding/paas/v4`
    - 默认模型: `astron-code-latest`
    - 如需使用特定GLM版本，在控制台套餐订阅页配置，修改后约2-3分钟生效

4. **切换模型**（可选）
   - 如需使用特定GLM版本，在[控制台套餐订阅页](https://www.bigmodel.cn/usercenter/glm-coding/subscribe)配置
   - 修改后预计2-3分钟生效

5. **开始编码**
   - 在工具中发起对话，自动消耗prompt额度
   - 查看[用量统计](https://www.bigmodel.cn/usercenter/glm-coding/usage)监控消耗

---

## 对比分析

### 价格竞争力

| 套餐 | 智谱AI | 百度千帆 | 阿里云 | 讯飞星火 |
|------|--------|----------|--------|----------|
| Lite/入门 | ¥49 | ¥40 | ¥40 | ¥3.9 |
| Pro/标准 | ¥149 | ¥200 | ¥200 | ¥7.9 |
| Max/旗舰 | ? | - | - | ¥39.9 |

✅ **智谱Pro档（¥149）** 在主流厂商中性价比极高，与百度千帆Pro（¥200）相比月费更低且支持GLM-5，但百度Pro含2,000次/月联网搜索权益。

### 独特优势

1. **MCP工具生态**: 独家提供4种MCP（视觉理解、联网搜索、网页读取、开源仓库），扩展能力远超纯代码生成
2. **GLM in Excel**: Beta版Excel插件，支持数据解释、公式生成、图表可视化等，场景独特
3. **Prompt透明计费**: 1 prompt ≈ 15-20次请求，成本可预测性强
4. **高速响应**: 55+ Tokens/秒，实际体验流畅
5. **限时福利**: 非高峰期GLM-5.1/5-Turbo仅1倍消耗，性价比突显

### 注意事项

- ⚠️ **30%+涨价已生效**: 2026年1月调整后价格大幅上涨，首月优惠已取消
- ⚠️ **周限额限制**: 2026年2月12日起新订阅用户受周限额约束，可能影响高频使用（老用户不受影响）
- ⚠️ **高峰期消耗加倍**: GLM-5.1等模型在高/非高峰期消耗系数不同，需合理规划使用时间
- ⚠️ **限售**: 短期每日限量，需10:00抢购

### 与竞品差异

- **vs 智谱API**: Coding Plan是专属套餐，与常规GLM API独立，不支持多账号共享
- **vs 讯飞星火**: 都采用非传统计费（prompt vs tokens），但智谱的MCP生态更丰富
- **vs 阶跃星辰**: 两者都用prompt计费，但阶跃Step Plan强调Agent性能，智谱强调工具生态

---

## 注意事项

- ✅ 2月12日前订阅用户**不受周限额**影响（重要！）
- ⚠️ GLM-5.1/GLM-5-Turbo消耗系数需特别关注，避免额度快速耗尽
- ⚠️ 高峰期（14:00-18:00 UTC+8）使用高阶模型消耗3倍
- ✅ 额度用完需等待5小时周期恢复，**不会**自动扣其他资源包/余额
- ✅ 仅限编程工具使用，禁止滥用（批量任务、后端服务等）
- ❌ 不支持退订（仅平台原因或法律规定）
- ✅ 可升级套餐，不支持降级（需到期后重购）

---

## 参考资源

- 套餐概览: https://docs.bigmodel.cn/cn/coding-plan/overview
- 快速开始: https://docs.bigmodel.cn/cn/coding-plan/quick-start
- 使用须知: https://docs.bigmodel.cn/cn/coding-plan/usage-notes
- 常见问题: https://docs.bigmodel.cn/cn/coding-plan/faq
- MCP工具:
  - 视觉理解MCP: https://docs.bigmodel.cn/cn/coding-plan/mcp/vision-mcp-server
  - 联网搜索MCP: https://docs.bigmodel.cn/cn/coding-plan/mcp/search-mcp-server
  - 网页读取MCP: https://docs.bigmodel.cn/cn/coding-plan/mcp/reader-mcp-server
  - 开源仓库MCP: https://docs.bigmodel.cn/cn/coding-plan/mcp/zread-mcp-server
- GLM in Excel: https://docs.bigmodel.cn/cn/coding-plan/extension/glm-in-excel
- 开发者社区: https://zhipu-ai.feishu.cn/wiki/TrlMwahsfihLrKkZsy0cpuTenCz

---

## 更新记录

| 日期 | 说明 |
|------|------|
| 2026年1月 | 价格结构性调整，整体涨幅30%+，取消首购优惠 |
| 2026年2月12日 | 周限额规则生效（新订阅用户；老用户不受影响） |
| 2026年3月持续 | MCP工具陆续上线（视觉、搜索、阅读、开源仓库） |
| 持续更新 | GLM in Excel Beta等新权益加入 |

---

**总结**: 智谱AI GLM Coding Plan是当前功能最丰富的Coding Plan之一，独特的MCP工具生态和Excel插件拓展了AI编码的边界。Pro档¥49的性价比极高（支持GLM-5），但需注意30%+的涨价已生效且周限额可能影响高频使用。适合需要联网搜索、视觉理解等高级能力的开发者。建议2月12日前订阅以规避周限额限制。
