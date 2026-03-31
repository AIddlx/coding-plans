# 讯飞星火 Coding Plan 记录

## 基本信息

**访问时间**: 2026年3月28日
**来源**: [讯飞开放平台官方文档](https://www.xfyun.cn/doc/spark/CodingPlan.html)
**文档版本**: v1.1 (最后更新: 2026年3月12日)

## 产品概述

讯飞星辰 MaaS Astron Coding Plan是讯飞星辰平台面向开发者的AI编码订阅服务，整合星火X2、GLM、Kimi、MiniMax、DeepSeek等旗舰模型。支持通过OpenAI协议与Anthropic协议接入，兼容Claude Code、OpenClaw、Cursor等主流AI编程工具。

### 核心特点

- **Token计费模式**: 首月版采用日tokens限额，次月版将转为请求次数限额
- **双协议支持**: 同时支持OpenAI协议和Anthropic协议
- **灵活价格阶梯**: 入门门槛极低（¥3.9），适合不同使用强度
- **模型快速切换**: 控制台配置后1-3分钟生效
- **专用API Key**: 仅限编程工具使用，防范欠费风险

---

## 套餐详情

### 📊 套餐对比总览（首月版）

| 对比项 | 入门版 | 专业版 | 高效版 |
|-------|--------|--------|--------|
| **价格（首购）** | ¥3.9/月 | ¥7.9/月 | ¥39.9/月 |
| **叠加价格** | ¥19/月 | ¥39/月 | ¥199/月 |
| **日Tokens上限** | 2,000万 | 1,000万 | 5,000万 |
| **QPS** | 20 | 5 | 20 |
| **支持模型** | 3个基础模型 | 6个完整模型 | 6个完整模型 |
| **适用场景** | 极轻度使用 | 轻度到中度 | 高频使用 |
| **性价比** | 极低门槛 | 中等 | 高额度 |

> ⚠️ **重要**: 当前为**首月版**（Token日限额），**次月版将改为5小时/周/月请求次数限额**，具体数值待更新。

### 首月版详细规则（2026年3月9日上线）

| 套餐 | 价格详情 | 额度详情 | QPS | 模型支持 |
|------|----------|----------|-----|----------|
| **入门版** | • 首购: ¥3.9/月<br>• 叠加: ¥19/月 | • 2,000万 tokens/日<br>• 每日00:00重置<br>• 未用不累积 | 20 | Qwen3.5-35B-A3B<br>DeepSeek-V3.2<br>GLM-4.7-Flash |
| **专业版** | • 首购: ¥7.9/月<br>• 叠加: ¥39/月 | • 1,000万 tokens/日<br>• 每日00:00重置<br>• 未用不累积 | 5 | 入门版全部 +<br>GLM-5<br>MiniMax-M2.5<br>Kimi-K2.5 |
| **高效版** | • 首购: ¥39.9/月<br>• 叠加: ¥199/月 | • 5,000万 tokens/日<br>• 每日00:00重置<br>• 未用不累积 | 20 | 专业版全部（同） |

**叠加购买规则**:
- 同一档位可多次购买，每增加一个套餐即增加一份当日Tokens额度
- 每个套餐对应一个独立的API Key
- 首次购买后追加按"叠加"价格计费（非首购价）

### 次月迭代版（计划中）

- 价格保持不变
- 流控方式改为:
  - **5小时流控**: 滑动窗口动态刷新
  - **周流控**: 每周一00:00:00重置
  - **月流控**: 每月订阅日对应时间重置
- 具体请求次数上限待控制台同步更新

---

## 用量限制说明

### 使用范围限制

Coding Plan额度**仅限在编程工具**（Claude Code、OpenClaw、Cursor等）的**交互式编码场景**中使用。

**禁止用途**:
- 自动化脚本、批量任务
- 自建应用后端或服务端
- 任何非交互式、非编程工具场景

**违规后果**: 可能导致限流、订阅停用或账号注销。

### 额度刷新机制

**首月版**:
- 每日00:00:00（UTC+8）重置当日tokens额度
- 未使用额度不累积

**次月版**（计划）:
- 5小时限额: 滚动刷新，自动释放5小时前的额度
- 周限额: 每周一重置
- 月限额: 每月订阅日重置

---

## 支持的模型

### 📋 模型支持矩阵（首月版）

| 模型名称 | 厂商 | 支持套餐 | 特点 |
|---------|------|----------|------|
| **Qwen3.5-35B-A3B** | 阿里云 | 入门版, 专业版, 高效版 | 通义千问模型 |
| **DeepSeek-V3.2** | 深度求索 | 入门版, 专业版, 高效版 | 高效推理 |
| **GLM-4.7-Flash** | 智谱AI | 入门版, 专业版, 高效版 | 快速响应 |
| **GLM-5** | 智谱AI | 专业版, 高效版 | 高阶模型 |
| **MiniMax-M2.5** | MiniMax | 专业版, 高效版 | 多模态支持 |
| **Kimi-K2.5** | 月之暗面 | 专业版, 高效版 | 长上下文处理 |

**切换方式**: 在控制台"套餐订阅"页面点击"配置模型"，修改后约1-3分钟生效。所有请求model固定为 `astron-code-latest`，底层模型由服务端路由。

> **注**: 支持模型以讯飞星辰MaaS平台实际上架为准。次月版模型列表可能调整，以官方更新为准。

---

## 支持的工具

### 📋 协议支持矩阵

| 协议类型 | 工具名称 | 支持档位 | Base URL |
|---------|----------|----------|----------|
| **Anthropic协议** | Claude Code | 入门版, 专业版, 高效版 | `https://maas-coding-api.cn-huabei-1.xf-yun.com/anthropic` |
| **OpenAI协议** | OpenClaw | 入门版, 专业版, 高效版 | `https://maas-coding-api.cn-huabei-1.xf-yun.com/v2` |
| **OpenAI协议** | Cursor | 入门版, 专业版, 高效版 | `https://maas-coding-api.cn-huabei-1.xf-yun.com/v2` |
| **OpenAI协议** | OpenCode | 入门版, 专业版, 高效版 | `https://maas-coding-api.cn-huabei-1.xf-yun.com/v2` |
| **OpenAI协议** | 其他OpenAI协议工具 | 入门版, 专业版, 高效版 | `https://maas-coding-api.cn-huabei-1.xf-yun.com/v2` |

**配置要点**:
- 所有工具需使用专属API Key（每个套餐独立）
- Base URL必须选择正确协议端点
- model固定为 `astron-code-latest`
- 底层模型在控制台配置，1-3分钟后生效

---

## 快速开始

### 1. 订阅套餐
- 访问[讯飞星辰MaaS平台控制台](https://maas.xfyun.cn/packageSubscription)
- 选择入门版/专业版/高效版，完成首购或叠加购买

### 2. 获取API Key
- 在套餐订阅页复制专属API Key
- 每个套餐对应一个独立API Key

### 3. 配置工具

**关键配置**:
- **Base URL**:
  - OpenAI协议: `https://maas-coding-api.cn-huabei-1.xf-yun.com/v2`
  - Anthropic协议: `https://maas-coding-api.cn-huabei-1.xf-yun.com/anthropic`
- **model**: `astron-code-latest`（固定）
- **切换底层模型**: 在控制台"套餐订阅"页面点击"配置模型"，1-3分钟后生效

**Claude Code配置** (`~/.claude/settings.json`):
```json
{
  "env": {
    "ANTHROPIC_AUTH_TOKEN": "你的API Key",
    "ANTHROPIC_BASE_URL": "https://maas-coding-api.cn-huabei-1.xf-yun.com/anthropic",
    "CLAUDE_CODE_DISABLE_NONESSENTIAL_TRAFFIC": 1,
    "API_TIMEOUT_MS": 600000,
    "ANTHROPIC_MODEL": "astron-code-latest",
    "ANTHROPIC_SMALL_FAST_MODEL": "astron-code-latest"
  }
}
```

**OpenClaw配置** (`~/.openclaw/openclaw.json`):
```json
{
  "models": {
    "mode": "merge",
    "providers": {
      "astroncodingplan": {
        "baseUrl": "https://maas-coding-api.cn-huabei-1.xf-yun.com/v2",
        "apiKey": "你的API Key",
        "api": "openai-completions",
        "models": [
          {
            "id": "astron-code-latest",
            "name": "astron-code-latest",
            "reasoning": false,
            "input": ["text"],
            "contextWindow": 92160,
            "maxTokens": 32768
          }
        ]
      }
    }
  }
}
```

### 4. 开始使用
- 启动Claude Code或OpenClaw
- 开始编码对话

---

## 对比分析

### 独特优势

1. **Token计费模式**: 与腾讯云Token Plan类似，适合token消耗大的场景（如长上下文、复杂任务）
2. **极低入门门槛**: 入门版首月仅¥3.9，叠加¥19，是所有Coding Plan中最低的
3. **双协议兼容**: 同时支持OpenAI和Anthropic生态，工具选择更灵活
4. **QPS保障**: 入门版和高效版QPS达20，专业版5

### 与竞品对比

| 维度 | 讯飞星火 | 阿里云 | 腾讯云 | 智谱AI |
|------|----------|--------|--------|--------|
| 计费模式 | Tokens（日限额） → 将转请求 | API请求 | Tokens | Prompts |
| 最低门槛 | ¥3.9 | ¥7.9（已停） | ¥39 | ¥20 |
| QPS | 5-20 | 未公开 | 未公开 | 未公开 |
| 后续模式 | 将转请求次数 | 请求次数 | Tokens | Prompts |

### 注意事项

- **过渡期不确定性**: 当前为"首月版"，次月将改为请求次数模式，具体限额待定
- **QPS差异**: 专业版仅5 QPS，可能限制高并发场景
- **新服务风险**: 作为新上线的服务（2026年3月9日），稳定性和功能完善度有待验证
- **模型切换**: 所有请求model固定为`astron-code-latest`，切换底层模型需在控制台配置

---

## 注意事项

- ✅ 支持升级（入门→专业→高效），不支持降级（需到期后重购）
- ✅ 叠加购买可增加当日额度
- ❌ 几乎不退订（仅平台原因或法律规定可退）
- ⚠️ 模型切换需1-3分钟生效
- ✅ 每个套餐独立API Key，便于额度管理
- ⚠️ 仅限个人开发，禁止滥用

---

## 参考资源

- 官方使用文档: https://www.xfyun.cn/doc/spark/CodingPlan.html
- 控制台: https://maas.xfyun.cn/packageSubscription
- 计费说明: https://www.xfyun.cn/doc/spark/BillingDescription.html
- 推理服务HTTP协议: https://www.xfyun.cn/doc/spark/推理服务-http.html
- 活动说明: https://www.xfyun.cn/doc/spark/CodingPlanEvent.html

---

## 更新记录

| 日期 | 说明 |
|------|------|
| 2026-03-12 | 官方文档v1.1，优化配置信息，增加错误码排查指南 |
| 2026-03-09 | Astron Coding Plan首月版上线（入门/专业/高效三档，日tokens限额） |
| 计划次月 | 改为请求次数限额（5小时/周/月） |

---

**总结**: 讯飞星辰Astron Coding Plan以极低门槛（¥3.9）和Token计费模式切入市场，适合想低成本试水的开发者。但其处于服务早期，额度模式和具体配额仍在迭代中，建议关注官方更新。Token计费对长上下文场景有利，但QPS限制（专业版仅5）可能影响高频使用体验。

