<div align="center">

<img src="./assets/logo-apiplus.svg" width="120" alt="API Plus Gateway logo" />

# API Plus Gateway

**基于 new-api 二次开发的大模型网关与 AI 资产管理系统展示页**

把多家模型供应商、用户额度、订阅充值、渠道路由、模型可用性和运营后台统一到一个可运营的 AI API 网关里。

[功能矩阵](./docs/feature-matrix.md) · [部署概览](./docs/deployment-overview.md) · [路线图](./docs/roadmap.md) · [上游项目](https://github.com/QuantumNous/new-api)

</div>

---

## 这是什么

API Plus Gateway 是一个面向 AI API 运营场景的网关方案展示仓库。项目基于 new-api 生态二次开发，目标不是只做“接口转发”，而是把模型接入、计费、用户资产、渠道稳定性和管理后台放在同一套系统里。

这个仓库是公开展示页，不包含完整业务源码、数据库、运行配置或私有部署资产。如果你想了解源码、部署、合作或二开交付，可以通过 GitHub Issues 发起沟通。

## 适合谁

| 场景 | API Plus Gateway 解决的问题 |
| --- | --- |
| AI API 分发平台 | 统一 OpenAI-compatible、Claude、Gemini、Rerank、图像、音频等模型接口 |
| 企业内部模型网关 | 将多供应商、多账号、多渠道收敛为统一入口，并保留后台治理能力 |
| AI 产品商业化 | 支持用户额度、充值、订阅套餐、返佣和账单查询等运营能力 |
| 多渠道容灾 | 通过渠道权重、失败重试、可用性监控和亲和缓存提升可用性 |
| 快速二开 | 在 new-api 基础上继续扩展支付、登录、渠道、计费和管理能力 |

## 核心亮点

### 多模型统一网关

支持 OpenAI-compatible、OpenAI Responses、Claude Messages、Google Gemini、Rerank、图像、音频、Realtime、Midjourney/Suno 类任务接口等多类型接入。上层业务只需要对接统一 API，底层可继续扩展不同供应商和协议转换。

### 可运营的用户资产系统

围绕真实运营补齐用户额度、充值记录、订阅套餐、余额事件、账单查询、返佣统计和后台筛选能力。相比单纯代理项目，更适合做可收费、可对账、可持续运营的 AI API 服务。

### 智能路由与稳定性治理

内置渠道权重、失败重试、模型可用性探测、渠道亲和缓存和异常日志能力，用于减少单一供应商波动对用户体验的影响。管理员可以围绕模型、分组、渠道和日志做持续优化。

### Playground 真实协议体验

支持 Playground 场景下的真实协议直连与用户令牌接管，方便用户在网页侧测试模型能力，也方便平台侧观察实际调用、计费和错误反馈。

### 多登录与安全扩展

支持 GitHub、Discord、LinuxDO、OIDC、Telegram 等登录/绑定能力，并保留 Passkey、二次验证、权限分组、令牌限制等安全治理方向。

## 能力总览

| 模块 | 能力 |
| --- | --- |
| 网关协议 | OpenAI-compatible、Responses、Claude Messages、Gemini、Rerank、Realtime、图像、音频 |
| 渠道治理 | 加权路由、失败重试、渠道测试、模型可用性、亲和缓存、日志追踪 |
| 商业化 | 充值、订阅、套餐绑定、余额事件、账单、返佣、后台统计 |
| 用户系统 | 注册登录、OAuth、Telegram、令牌管理、分组权限、额度限制 |
| 管理后台 | 渠道、模型、用户、计费、日志、订阅、充值、佣金、配置项 |
| 部署形态 | Docker Compose、MySQL/PostgreSQL/SQLite、Redis 缓存、多机部署配置 |

## 项目边界

这个仓库不是完整源码仓库，也不是可直接 `docker compose up` 的交付包。它用于公开介绍 API Plus Gateway 的定位、功能、部署形态和二开方向。

如果你需要完整部署，请重点确认：

1. 支付渠道是否完成真实商户配置和回调验证。
2. 模型供应商账号、渠道权重和价格倍率是否符合你的业务。
3. Redis、数据库、会话密钥和加密密钥是否按生产要求配置。
4. AGPLv3 与上游项目许可证是否符合你的组织合规要求。

## 与 new-api 的关系

API Plus Gateway 基于 new-api 生态进行二次开发，继承其多模型网关、管理后台和 API 转发基础，并围绕商业化、订阅、充值、返佣、模型可用性监控、渠道治理和用户侧体验继续增强。

感谢以下上游项目：

| 项目 | 说明 |
| --- | --- |
| [new-api](https://github.com/QuantumNous/new-api) | 主要上游项目和多模型网关基础 |
| [One API](https://github.com/songquanpeng/one-api) | 更早期的 API 管理与转发基础 |

## 快速了解

建议从这些文档开始：

| 文档 | 内容 |
| --- | --- |
| [功能矩阵](./docs/feature-matrix.md) | 按模块查看当前展示能力 |
| [部署概览](./docs/deployment-overview.md) | 了解生产部署需要准备什么 |
| [路线图](./docs/roadmap.md) | 查看后续适合继续打磨的方向 |

## 联系

如果你想了解源码、部署、二开、私有化或合作方式，请在本仓库提交 Issue，并说明你的使用场景、预计用户规模、需要接入的模型供应商和支付方式。

---

<div align="center">

**API Plus Gateway** · 让 AI API 网关从“能转发”走向“能运营”

</div>
