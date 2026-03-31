# 月之暗面 Kimi Code 会员权益记录

## 基本信息

- **访问时间**: 2026年3月28日
- **产品名称**: Kimi Code（Kimi会员权益）
- **来源**:
  - [会员权益说明](https://www.kimi.com/user/agreement/zh/membershipBenefits)
  - [Kimi Code文档](https://www.kimi.com/code/docs/benefits.html)
  - [API价格说明](https://platform.moonshot.cn/docs/pricing/chat)
  - [权益详细对比](https://www.kimi.com/user/agreement/zh/membershipBenefits)
- **控制台**: https://www.kimi.com/code/console
- **版本生效**: 2026年2月28日

---

## ⚠️ 核心认知：会员权益模式 + 复合限额

**Kimi Code 不是独立订阅产品，而是 Kimi 会员的组成部分**。这意味着：
- ✅ 购买 Kimi 会员即获得编码能力，无需额外付费
- ✅ 会员其他权益（Agent、深度研究、PPT）可与 Code 额度共享
- ❌ 无法单独购买更高 Code 额度，必须升级整个会员档位
- ❌ Code 额度成本远高于独立 Coding Plan（约 ¥4.9-7.0/次 vs ¥0.02-0.05/次）

### 🔢 计费模式详解

Kimi Code 采用 **Token-based internal billing**（内部Token计费），但对外呈现为**多层请求限额**：

| 维度 | 说明 |
|------|------|
| **计费基础** | 内部按Token消耗计算 |
| **用户视角** | 按**API请求次数**限制（每月固定次数） |
| **限额维度** | **5小时滚动限额** + **周限额** + 月总额度 |
| **模型倍率** | K2.5模型使用有倍数系数（1x/2x/4x/10x）影响实际消耗 |

**简化理解**: 用户每月有固定 Code 请求次数（10/20/40/100），但每次请求实际消耗的 Token 数量受模型选择影响（K2.5 倍率越高，单次消耗越大）。

---

## 会员档位与价格

### 档位对比总表

| 档位 | 包月价格 | **连续包年（8折）** | Kimi Code 额度/月 | Agent 额度/月 | K2.5 模型额度 | 年付节省 |
|------|----------|---------------------|-------------------|---------------|---------------|----------|
| **免费版 (Adagio)** | 免费 | - | 3次 | 3次 | 基础模型 | - |
| **Andante (入门)** | ¥49/月 | **¥39/月**<br>（年付¥468） | 10次 | 10次 | 1x | ¥120 |
| **Moderato (基础)** | ¥99/月 | **¥79/月**<br>（年付¥948） | 20次 | 20次 | **2x** | ¥240 |
| **Allegretto (高级)** | ¥199/月 | **¥159/月**<br>（年付¥1,908） | 40次 | 40次 | **4x** | ¥480 |
| **Allegro (旗舰)** | ¥699/月 | **¥559/月**<br>（年付¥6,708） | **100次** | **100次** | **10x** | ¥1,680 |

**关键洞察**:
- 年付优惠约 **20%**（8折），长期使用推荐年付
- Allegro 档位是唯一提供 **100次/月 Kimi Code 额度**的选项
- K2.5 模型使用额度随档位倍增：1x → 2x → 4x → **10x**

---

## 详细权益对比

### 完整权益矩阵

| 权益项目 | Andante | Moderato | Allegretto | Allegro |
|---------|---------|----------|------------|---------|
| **Kimi Code 月额度** | 10次 | **20次** (4x) | **40次** (20x) | **100次** (60x) |
| **Agent 月额度** | 10次 | **20次** (2x) | **40次** (4x) | **100次** (10x) |
| **深度研究月额度** | 10次 | **20次** (2x) | **40次** (4x) | **100次** (10x) |
| **PPT 助手月额度** | 10次 | **20次** (2x) | **40次** (4x) | **100次** (10x) |
| **K2.5 模型倍数** | 1x | **2x** | **4x** | **10x** |
| **Kimi Code 相对倍数** | 1x | **4x** | **20x** | **60x** |
| **高速模型 Kimi Turbo** | ✅ | ✅ | ✅ | ✅ |
| **高峰时段 PPT 4倍速** | ✅ | ✅ | ✅ | ✅ |
| **同时运行 2 个 Agent 任务** | ❌ | ✅ | ✅ | ✅ |
| **同时运行 2 个深度研究** | ❌ | ✅ | ✅ | ✅ |
| **同时运行 2 个 PPT 任务** | ❌ | ✅ | ✅ | ✅ |
| **Agent Swarm 支持** | ❌ | ❌ | ✅ | ✅ |
| **Kimi Claw 一键部署** | ❌ | ❌ | ✅ | ✅ |
| **专属助理** | ❌ | ❌ | ✅ | ✅ |

**额度说明**:
- **Kimi Code 额度**: 专用于编程场景的 API 请求次数（括号内为相对于 Andante 的倍数）
- **Agent/深度研究/PPT 额度**: 独立于 Code，各功能间共享（除 Code 外），括号内为相对于 Andante 的倍数
- **K2.5 模型倍数**: 影响单次 Code 请求的 Token 消耗倍数（1x=基准，10x=高消耗高回报）
- **Kimi Code 相对倍数**: 展示各档位相对于 Andante 的 Code 额度增长（注意：这不是 K2.5 倍数，是独立的额度倍增）
- **所有月额度按周刷新**，未使用不累积、不退款

---

## 额度刷新逻辑（多层结构）

Kimi Code 采用**多层刷新机制**，这是其核心特点：

### 三层限额结构

1. **5小时滚动限额**（动态刷新）
   - 每5小时刷新一次可用额度
   - 这是**最严格的限制**，用完后需等待5小时
   - 参考：每5小时Token总量支持约300-1200次API请求（因档位和模型而异）

2. **周限额**（7天周期）
   - 官方明确描述：以订阅日期 D1 为起点
   - D1-D7: 首周额度
   - D8-D14: 第二周额度刷新
   - 以此类推，每7天刷新一次
   - 作为5小时限额的上层总约束

3. **月总额度**（月度上限）
   - 各档位有固定的月 Code 额度（10/20/40/100次）
   - 周限额和5小时限额都在此月总额度内循环
   - 月额度用尽后需等待下月重置

### 刷新优先级

```
月总额度 (10-100次/月)
    ├── 周限额 (D1-D7, D8-D14...)
    │     └── 5小时滚动限额 (每5小时刷新)
    └── 最严格限制：5小时额度用尽即阻塞，即使周/月有剩余
```

**重要**:
- ⚠️ **5小时限额最严格**: 即使周/月额度有剩余，5小时内用尽也会阻塞
- ✅ 月会员权益按月发放，未使用部分自动失效，不退款
- 🔄 额度类型（Agent/深度研究/PPT/Kimi Code）**独立计算**，互不影响
- ⚠️ 会员过期后，Kimi Claw 云资源保留 **7天**，之后永久关停并清空数据

---

## 支持的模型

### 模型性能分级

| 模型 | 性能 | 说明 |
|------|------|------|
| **Kimi Turbo** | 高速 | 所有会员档位可用 |
| **K2.5 系列** | 旗舰 | 根据档位获得不同使用倍数（1x/2x/4x/10x） |

**K2.5 多模式**:
- **快速模式** (Fast): 响应速度快
- **思考模式** (Thinking): 深度推理
- **Agent 模式**: 智能体调用
- **Agent 集群**: 多 Agent 并行（Allegretto+）

### 模型选择建议

- **Andante**: 日常任务，Kimi Turbo 足够
- **Moderato**: 复杂任务，可使用 2x K2.5
- **Allegretto**: 重度开发，推荐 4x K2.5 + Agent Swarm
- **Allegro**: 生产环境，10x K2.5 最高性能

---

## 支持的工具

### 官方工具
- **Kimi CLI** - 命令行智能体工具
- **Kimi Code for VS Code** - 官方 VS Code 插件

### 第三方 Coding Agent（通过 API Key）
- **Claude Code** (Anthropic 协议)
- **Roo Code** (支持 Kimi API)

### 配置方式

#### 1. Kimi CLI（推荐）
```bash
npm install -g @moonshotai/kimi-cli
kimi login  # 使用 Kimi 账号登录
kimi  # 启动交互
```

#### 2. VS Code 插件
- 安装 "Kimi Code for VS Code"
- 在插件设置中登录 Kimi 账号
- 侧边栏打开 Kimi Code 面板

#### 3. Claude Code 配置
```json
{
  "env": {
    "ANTHROPIC_AUTH_TOKEN": "你的Kimi API Key",
    "ANTHROPIC_BASE_URL": "https://api.moonshot.cn/v1",
    "ANTHROPIC_MODEL": "kimi-k2.5"
  }
}
```

---

## 快速开始

### 新用户：7天试用

**苹果端**: 免费试用
**非苹果端**: ¥4.99/7天

试用额度（7天）:
- Agent: 3次（苹果）/ 5次（非苹果）
- 深度研究: 3次 / 5次
- PPT: 3次 / 5次
- 不支持同时运行多个任务

⚠️ 试用期结束后自动转正式订阅（可随时取消）

### 正式订阅

1. **选择档位**: 根据需求选择 Andante/Moderato/Allegretto/Allegro
2. **选择周期**: 包月或包年（年付省20%）
3. **支付**: 完成订阅
4. **获取 API Key**: 访问 [Kimi Code 控制台](https://www.kimi.com/code/console)
5. **配置工具**: 在 Kimi CLI、Claude Code 或 Roo Code 中使用

### 设备管理

- 可在控制台查看已授权设备列表
- 设备超过 30 天未活跃，登录态自动失效
- 支持多种设备登录，Moderato+ 可分享额度

---

## 使用限制与注意事项

### ✅ 允许场景
- 个人开发使用
- 在指定工具中使用（Kimi CLI、Claude Code、Roo Code）
- 编程相关任务（代码生成、调试、重构等）

### ❌ 禁止场景
- 企业开发（需使用开放平台 API，按 token 付费）
- 在非指定产品中使用 base_url 和 API Key（视为滥用）
- API Key 共享给他人使用
- 非编程场景使用

### 额度管理
- **不累积**: 未使用额度到期自动失效
- **不退款**: 已付费不退还
- **独立**: 套餐额度与账户余额独立，不互通
- **超限**: 超出额度后无法继续使用，需等待刷新

### 订阅与取消
- ✅ 支持随时取消订阅
- ✅ 已付费服务持续到周期结束
- ✅ 包年比包月省20%（8折）
- ⚠️ 试用期结束后自动转正式订阅（可取消）

### 地区限制
- ⚠️ **首月优惠砍价活动仅限中国大陆以外地区**
- 中国大陆用户无法参与砍价，需按原价订阅

---

## 技术规格

### API 价格（企业参考）

| 模型 | 输入价格 | 输出价格 | 上下文长度 |
|------|----------|----------|------------|
| kimi-k2.5 (多模态) | 缓存命中: ¥0.70/1M<br>缓存未命中: ¥4.00/1M | ¥21.00/1M | 262,144 tokens |
| kimi-k2-0905-preview | ¥1.00/1M | ¥16.00/1M | 262,144 |
| kimi-k2-turbo-preview | ¥1.00/1M | ¥58.00/1M | 262,144 |
| kimi-k2-thinking | ¥1.00/1M | ¥16.00/1M | 262,144 |
| moonshot-v1-8k | ¥2.00/1M | ¥10.00/1M | 8,192 |
| moonshot-v1-128k | ¥10.00/1M | ¥30.00/1M | 131,072 |

**联网搜索**: ¥0.03/次

### 速率限制（用户等级）

| 等级 | 累计充值 | 并发 | RPM | TPM | TPD |
|------|----------|------|-----|-----|-----|
| Tier0 | ¥0 | 1 | 3 | 500K | 1.5M |
| Tier1 | ¥50 | 50 | 200 | 2M | Unlimited |
| Tier2 | ¥100 | 100 | 500 | 3M | Unlimited |
| Tier3 | ¥500 | 200 | 5,000 | 3M | Unlimited |
| Tier4 | ¥5,000 | 400 | 5,000 | 4M | Unlimited |
| Tier5 | ¥20,000 | 1,000 | 10,000 | 5M | Unlimited |

---

## 参考资源

- [会员权益说明](https://www.kimi.com/user/agreement/zh/membershipBenefits)
- [Kimi Code 文档](https://www.kimi.com/code/docs/benefits.html)
- [Kimi Code CLI 指南](https://www.kimi.com/code/docs/kimi-cli/guides/getting-started.html)
- [VS Code 插件指南](https://www.kimi.com/code/docs/kimi-code-for-vscode/guides/getting-started.html)
- [第三方工具接入](https://www.kimi.com/code/docs/more/third-party-agents.html)
- [开放平台 API 价格](https://platform.moonshot.cn/docs/pricing/chat)
- [联网搜索定价](https://platform.moonshot.cn/docs/pricing/tools)
- [充值与限速](https://platform.moonshot.cn/docs/pricing/limits)
- [促销活动](https://platform.moonshot.cn/docs/promotion)
- [企业咨询](mailto:sales@kimi.com)

---

## 更新记录

| 日期 | 说明 |
|------|------|
| 2026-02-28 | K2.5 发布，会员权益更新，Allegro 档位新增 |
| 2026-03-28 | 补充完整权益矩阵和档位对比 |
| 2026-03-28 | 更新年付价格和折扣信息 |

---

**中国大陆用户注意**: 无法享受首月砍价活动，需按原价订阅。
