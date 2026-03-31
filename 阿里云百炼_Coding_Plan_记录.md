# 阿里云百炼 Coding Plan 记录

## 基本信息

**访问时间**: 2026年3月28日
**来源**: [阿里云百炼控制台](https://bailian.console.aliyun.com/)

## 产品概述

Coding Plan 是阿里云百炼推出的AI编码订阅套餐，专为编程场景设计。

### 核心特点
- **模型整合**: 整合千问(Qwen)、GLM、Kimi、MiniMax等顶级模型
- **兼容性**: 兼容主流AI编程工具和API协议
- **成本优势**: 折算成本远低于常规API调用
- **风险控制**: 固定月费模式，有效防范欠费风险
- **使用限制**: 仅限在编程工具中使用，禁止API批量调用

---

## 套餐详情

### 📊 套餐对比总览

| 对比项 | Lite 基础套餐 | Pro 高级套餐 |
|-------|---------------|--------------|
| **价格（原价）** | ¥40/月<br>（首月¥7.9，次月¥20） | ¥200/月 |
| **5小时额度** | 1,200次 | 6,000次 |
| **每周额度** | 9,000次 | 45,000次 |
| **每月额度** | 18,000次 | 90,000次 |
| **额度比例** | Pro是Lite的**5倍** | - |
| **价格比例** | - | 价格是Lite的**5倍** |
| **功能差异** | 与Pro完全一致 | 与Lite完全一致 |
| **适用场景** | 新手尝鲜、轻度使用 | 高频开发、重度用户 |
| **状态** | ❌ 已停止新购（2026-03-20起） | ✅ 当前主推 |

### Pro 高级套餐（当前主推）

| 项目 | 详情 |
|------|------|
| **价格** | ¥200/月 |
| **支持模型** | **推荐模型**:<br>• qwen3.5-plus (支持图片理解)<br>• kimi-k2.5 (支持图片理解)<br>• glm-5<br>• MiniMax-M2.5<br><br>**更多模型**:<br>• qwen3-max-2026-01-23<br>• qwen3-coder-next<br>• qwen3-coder-plus<br>• glm-4.7 |
| **用量限制** | • 每5小时: **6,000**次请求<br>• 每周: **45,000**次请求<br>• 每月: **90,000**次请求 |
| **额度恢复** | • **5小时额度**: 滚动恢复，每分钟自动释放5小时前的额度<br>• **每周额度**: 每周一 00:00:00 (UTC+8) 重置<br>• **每月额度**: 下月订阅日 00:00:00 (UTC+8) 重置 |
| **消耗说明** | • 简单任务: 约5-10次/次提问<br>• 复杂任务: 约10-30+次/次提问<br>• 实际消耗受任务难度、上下文及工具使用影响 |

### Lite 基础套餐（已停止新购）

> ⚠️ **重要通知**: 自2026年3月20日00:00:00（UTC+8）起，Lite基础套餐停止接受新购订单。已购买用户的使用、续费及套餐升级权益保持不变。

| 项目 | 详情 |
|------|------|
| **价格** | 首月¥7.9，次月¥20，第三个月起¥40/月 |
| **用量限制** | • 每5小时: **1,200**次请求<br>• 每周: **9,000**次请求<br>• 每月: **18,000**次请求 |
| **额度恢复** | 同Pro套餐（滚动恢复、周重置、月重置） |

---

## 价格历史

### Pro 高级套餐
- **首月**: ¥39.9（限时优惠价，活动已结束）
- **次月续费**: ¥100（5折）
- **第三个月起**: ¥200/月

### Lite 基础套餐（历史价格）
- **首月**: ¥7.9
- **次月续费**: ¥20（5折）
- **第三个月起**: ¥40/月

> **说明**: 当前价格以下单页为准。限时优惠活动已结束。

---

## 支持的模型

### 📋 模型支持矩阵

| 模型名称 | 厂商 | 支持档位 | 特点 | 多模态 |
|---------|------|----------|------|--------|
| **qwen3.5-plus** | 阿里云 | Lite, Pro | 推荐模型，代码生成能力强 | ✅ 图片理解 |
| **kimi-k2.5** | 月之暗面 | Lite, Pro | 长上下文处理 | ✅ 图片理解 |
| **glm-5** | 智谱AI | Lite, Pro | 代码优化 | ❌ |
| **MiniMax-M2.5** | MiniMax | Lite, Pro | 综合能力强 | ❌ |
| **qwen3-max-2026-01-23** | 阿里云 | Pro | 旗舰模型 | ❌ |
| **qwen3-coder-next** | 阿里云 | Pro | 编码专用 | ❌ |
| **qwen3-coder-plus** | 阿里云 | Pro | 编码专用 | ❌ |
| **glm-4.7** | 智谱AI | Lite, Pro | 基础模型 | ❌ |

**注意**: 具体可用模型以控制台实时显示为准，官方会持续更新。切换模型可在控制台内一键完成，无需修改本地配置。

---

## 支持的工具

### 📋 工具兼容性矩阵

| 工具名称 | 类型 | 支持协议 | 支持档位 | 备注 |
|---------|------|----------|----------|------|
| **Qwen Code** | 阿里云官方 | OpenAI | Lite, Pro | 官方推荐工具 |
| **Claude Code** | Anthropic | Anthropic | Lite, Pro | 需配置Anthropic Base URL |
| **Cline** | 开源 | OpenAI | Lite, Pro | VS Code插件 |
| **OpenClaw** | 开源 | OpenAI | Lite, Pro | 原Moltbot/Clawdbot |
| **CoPaw** | 开源 | OpenAI | Lite, Pro | - |
| **Kilo Code** | 轻量级 | OpenAI | Lite, Pro | - |
| **Cursor** | AI原生编辑器 | OpenAI | Lite, Pro | 需通过IDE插件配置 |
| **JetBrains IDE系列** | 商业IDE | OpenAI | Lite, Pro | IDEA、PyCharm等通过插件 |

**配置说明**: 所有工具共享套餐额度，可在不同工具间灵活切换使用。

---

## 快速开始指南

### 步骤1: 订阅 Coding Plan

1. 访问 [Coding Plan页面](https://bailian.console.aliyun.com/)
2. 根据需求选择并购买套餐
3. **RAM子账号**需要完成授权:
   - 主账号在权限管理页面添加用户
   - 授予管理员权限

### 步骤2: 获取API Key和Base URL

#### API Key
- 在Coding Plan页面获取专属API Key
- 格式: `sk-sp-xxxxx`
- ⚠️ **注意**: 与百炼按量计费的API Key（`sk-xxxxx`）不互通

#### Base URL（二选一）

| 协议类型 | Base URL |
|----------|----------|
| OpenAI兼容协议 | `https://coding.dashscope.aliyuncs.com/v1` |
| Anthropic兼容协议 | `https://coding.dashscope.aliyuncs.com/apps/anthropic` |

### 步骤3: 接入AI工具

#### 支持的编程工具
- **Qwen Code**（阿里云官方）
- **Claude Code**
- **Cline**
- **OpenClaw**（原Moltbot/Clawdbot）
- **CoPaw**
- **Kilo Code**
- **Cursor**（通过IDE插件）
- **JetBrains IDE系列**（IDEA、PyCharm等通过插件）

#### 配置方式

**以Qwen Code为例**:

1. **安装Qwen Code**:
   ```bash
   # macOS/Linux
   curl -fsSL https://qwen-code-assets.oss-cn-hangzhou.aliyuncs.com/installation/install-qwen.sh | bash -s -- --source bailian

   # Windows
   curl -fsSL -o %TEMP%\install-qwen.bat https://qwen-code-assets.oss-cn-hangzhou.aliyuncs.com/installation/install-qwen.bat && %TEMP%\install-qwen.bat --source bailian
   ```

2. **认证配置**:
   - 启动Qwen Code
   - 运行 `/auth` 命令
   - 选择 `api-key` 方式
   - 选择 `Coding-plan`
   - 填写API Key

3. **切换模型**:
   - 运行 `/model` 命令
   - 选择Coding Plan支持的任意模型

---

## 使用限制与规范

### ✅ 允许使用场景
- AI编程工具（如Claude Code、Qwen Code、Cline等）
- IDE插件（Claude Code IDE插件、Kilo Code、Qwen Code IDE插件）
- OpenClaw类型的Agent

### ❌ 禁止使用场景
- **工作流/自动化平台**: Dify、n8n、Coze等
- **API测试工具**: Postman、Insomnia等
- **自定义应用程序**: 自动化脚本、应用后端代码直接调用API
- **任何非交互式批量调用场景**

### ⚠️ 违规后果
将套餐API Key用于禁止范围之外的调用将被视为**违规或滥用**，可能导致:
- 订阅被暂停
- API Key被封禁

---

## 重要注意事项

### 1. 不支持退款
Coding Plan服务**不支持退款**，订阅前请仔细评估需求。

### 2. 数据使用授权
- 使用期间，模型输入和生成内容将用于**服务改进与模型优化**
- 停止使用可终止后续数据授权
- 已授权使用的数据不涵盖在终止范围内
- 详细条款: 阿里云百炼服务协议第5.2条

### 3. 账号使用规范
- 套餐为**订阅人专享使用**，禁止共享
- 账号共享可能导致订阅权益受限

### 4. API Key安全
- Coding Plan专属API Key（`sk-sp-xxxxx`）与百炼通用API Key（`sk-xxxxx`）**不互通**
- 误用通用API Key会导致额外按量计费

---

## 常见问题

### Q1: 已购买Coding Plan但仍显示欠费/被扣费？

**原因**: 误用了百炼通用API Key和Base URL，系统识别为按量付费。

**解决方案**:
1. 改用Coding Plan专属API Key（以`sk-sp-`开头）
2. 使用专属Base URL（含`coding.dashscope.aliyuncs.com`）
3. 检查配置方法: 参考"获取套餐专属API Key和Base URL"

### Q2: 额度消耗速度差异？

**影响因素**:
- 任务复杂度
- 上下文长度
- 工具使用情况
- 简单任务: 5-10次/次
- 复杂任务: 10-30+次/次

### Q3: 额度恢复机制？

**三种额度独立恢复**:
1. **5小时额度**: 滚动恢复，每分钟释放5小时前的额度
2. **每周额度**: 每周一00:00:00重置
3. **每月额度**: 下月订阅日00:00:00重置

---

## 参考资源

### 官方文档
- [Coding Plan概述](https://help.aliyun.com/zh/model-studio/coding-plan)
- [其他工具接入指南](https://help.aliyun.com/zh/model-studio/other-tools-coding-plan)
- [Coding Plan用户指南](https://www.alibabacloud.com/help/zh/model-studio/coding-plan-guide/)

### 外部资源
- [2026最新！阿里云百炼Coding Plan详解（知乎）](https://zhuanlan.zhihu.com/p/2010486807704409374)
- [阿里云百炼产品页](https://www.aliyun.com/product/bailian)

### 相关链接
- [百炼控制台](https://bailian.console.aliyun.com/)
- [Qwen Code下载页](https://www.aliyun.com/benefit/scene/codingplan)

---

## 更新记录

| 日期 | 更新内容 | 备注 |
|------|----------|------|
| 2026-03-28 | 初始记录 | 基于官方文档和第三方资料整理 |
| 2026-03-20 | Lite套餐停止新购 | 官方通知 |
| 2026-01-12 | 文档首次发布 | - |

---

## 备注

1. **订阅前须知**: 请务必阅读"订阅前须知"部分，了解使用限制和风险
2. **额度监控**: 建议在Coding Plan页面定期查看用量，避免额度超限
3. **工具兼容性**: 部分编程工具（如通义灵码个人版、Cursor免费版、Trae）不支持自定义服务端点，无法直接使用Coding Plan
4. **限时优惠**: 当前价格以下单页为准，原限时优惠活动已结束

---

**记录人**: Sisyphus (AI Agent)
**记录方式**: 自动抓取并整理官方文档及第三方资料
**验证状态**: ✅ 信息已交叉验证（官方文档 + 第三方解读）
