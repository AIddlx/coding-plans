# 快手 KwaiKAT Coding Plan 记录

## 基本信息

**记录时间**: 2026年3月30日
**来源**: [快手StreamLake Coding Plan](https://www.streamlake.com/marketing/coding-plan)
**所属公司**: 快手（StreamLake/万擎）
**模型**: KAT-Coder-Pro V2

---

## 产品概述

KwaiKAT Coding Plan 是快手旗下 StreamLake 平台推出的 AI 编程订阅服务，采用 Prompt 计费模式，针对 Agentic Coding 场景深度优化。

### 核心特点

- **Prompt计费**: 1 prompt ≈ 15-20次模型调用，复合处理机制归一化计费
- **单一模型**: KAT-Coder-Pro V2（快手自研旗舰编码模型）
- **Agentic优化**: 针对 OpenClaw 专项训练与深度优化
- **工具兼容**: Claude Code、Cline、Kilo、OpenCode 等 10+ 工具
- **双协议**: 支持 OpenAI 协议和 Claude 协议

---

## 套餐详情

### 订阅套餐

| 套餐 | 月费 | 5小时额度 | 换算后（×15） | 每元额度 | RPM/TPM |
|------|------|-----------|-------------|---------|---------|
| **Star** | ¥29 | 40 Prompts | ~600次 | 20.7 | 60 RPM / 200万 TPM |
| **Starter** | ¥70 | 100 Prompts | ~1,500次 | 21.4 | 60 RPM / 200万 TPM |
| **Pro** | ¥140 | 300 Prompts | ~4,500次 | 32.1 | 60 RPM / 200万 TPM |
| **Max** | ¥350 | 1,000 Prompts | ~15,000次 | 42.9 | 60 RPM / 200万 TPM |

**额度说明**:
- **5小时窗口**: 固定时段（如 00:00-05:00），超过限制后等待下一个5小时时段自动重置
- **周/月额度**: 官方未明确公布，仅公布5小时限额
- **额度换算**: 1 prompt ≈ 15-20次模型调用，表中按15倍计算

### 按量付费

| 项目 | 价格 |
|------|------|
| 输入 | ¥2.1 / MTok |
| 输出 | ¥8.4 / MTok |
| 缓存写入 | 免费 |
| 缓存读取 | ¥0.42 / MTok |

### API 接口

**订阅用户（Coding Plan）**:
- OpenAI 协议: `https://wanqing.streamlakeapi.com/api/gateway/coding/v1`
- Claude 协议: `https://wanqing.streamlakeapi.com/api/gateway/coding/kat-coder-pro-v2/claude-code-proxy`

**按量付费用户**:
- OpenAI 协议: `https://wanqing.streamlakeapi.com/api/gateway/v1/endpoints`
- Claude 协议: `https://wanqing.streamlakeapi.com/api/gateway/v1/endpoints/kat-coder-pro-v2/claude-code-proxy`

---

## 支持的工具

Claude Code、OpenClaw、Cursor、Cline、Kilo Code、OpenCode 等 10+ 主流 AI 编码工具。

---

## FAQ 摘要

**Prompt 计算**: 单次前台操作驱动后台约 15-20 次精密运算（上下文检索、代码生成与自我修正），标准化为一个 Prompt 单位。

**套餐升级**: 支持"立即生效"（补差价）和"下月生效"两种方式。

**V1 先锋卡**: 可在控制台「卡券管理」兑换，仅限 V1 模型，V1 下线后权益同步停止。

**V2 兼容**: 原有 Coding Plan 订阅可直接切换模型名为 KAT-Coder-Pro V2 使用。

---

**记录人**: AI Agent
**验证状态**: 基于官方页面信息整理
