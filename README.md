<div align="center">

# 网腾无限AI - AIGC多模态创作专家

**基于 Vue 3 + Vite + Vanilla CSS 构建的极简 AIGC 多模态创作与文本降重润色微应用，具备深色玻璃拟态自适应交互与微信端 H5 体验**

Vue 3 · TypeScript · Vite · Vanilla CSS · 开源协议 MIT

[![GitHub stars](https://img.shields.io/github/stars/WT-Agent/ai-aigc?style=social)](https://github.com/WT-Agent/ai-aigc)
[![GitHub license](https://img.shields.io/github/license/WT-Agent/ai-aigc)](https://github.com/WT-Agent/ai-aigc/blob/main/LICENSE)

[在线演示](#在线演示) · [快速启动](#快速启动) · [参与贡献](#参与贡献) · [支持一下](#支持一下)

</div>

## 关于我们

团队成员均来自 C9 等顶尖学府，在字节、腾讯、阿里的工程师组成，全职创业研发开源 AI 应用产品，让所有人感受 AI 的魅力。

本项目是网腾无限 AI 微应用的标准开发模版，内置了毛玻璃深色主题样式系统、移动端与 PC 端自适应响应式框架、API 中转代理配置与流量裂变逻辑。

**我们不搞概念，不卖课，只写能跑起来的代码。**

欢迎 Star、Fork、提 Issue，一起让这个项目变得更好用。

核心特性：
- **极简自适应交互**：提供毛玻璃质感的深色玻璃拟态自适应 Web 界面，高度适配移动端 H5 微信浏览器与 PC 体验。
- **一键零成本部署**：纯静态前端结构，支持零成本部署于 Vercel、GitHub Pages 或 CDN/OSS 静态托管服务。
- **安全开发代理**：本地开发支持使用个人 API 密钥发起代理请求，密钥由 Vite 服务器中转，无需担心前端泄露。
- **裂变解锁与留存**：内置微信朋友圈扫码分享拦截与额度重置机制，提升流量转化与留存。

## 核心功能模块

1. **智能 AI 痕迹诊断**：精准识别文章中的高频 AI 套话与特征句式，输出风险评分与重构建议。
2. **多模态学术润色**：针对工学、理学、医学、社科等不同学科领域，提供顶级学术语重构与语法修饰。
3. **深层降重与查重避坑**：深度重组句式结构与替换专业词汇，有效绕过查重算法的 AI 概率判定。
4. **多模态内容生成与导向**：支持多维度创作模式定制，全流程提升文本质量与可读性。

## AI 评估指标体系

本项目对生成方案采用 5 大核心 AI 共识打分体系（1-5分）：
- **aigcReduction (AIGC 降重率)**：衡量文本去除 AI 痕迹与模式化套话的彻底程度。
- **academicTone (学术语体专业度)**：评估重构后文本的学术规范性与严谨程度。
- **logicCohesion (逻辑衔接流畅度)**：评估段落间与上下文逻辑关联的连贯性。
- **vocabRichness (词汇丰富度)**：衡量学术词汇多样性与专业近义词替换水平。
- **readability (整体可读性)**：综合评定最终生成的语句自然度与可读体验。

## 快速启动

### 1. 克隆项目
```bash
git clone https://github.com/WT-Agent/ai-aigc.git
cd ai-aigc
```

### 2. 安装依赖
项目强制使用 pnpm 作为包管理器：
```bash
pnpm install
```

### 3. 配置本地开发环境变量
复制并修改环境变量配置文件：
```bash
cp .env.example .env
```
根据微应用的功能类型，在 `.env` 中配置您的开发者密钥：
- `DEEPSEEK_API_KEY`: 您的 DeepSeek 开发者 API 密钥（用于文本生成任务）
- `DASHSCOPE_API_KEY`: 您的通义千问/通义万相开发者 API 密钥（用于多模态与生图任务）

### 4. 启动本地开发服务
```bash
pnpm dev
```
启动成功后在浏览器访问控制台输出的地址即可。

### 5. 生产构建打包
```bash
pnpm build
```
打包后生成的 `dist` 目录即为纯静态网页资源，可直接上传部署。

## 脚手架集成说明

本模板由私有总控仓库 `ai-.wuxian.xyz` 中的 `@wuxian/cli` 脚手架统一管理，支持以下批量运维操作：

### 初始化或更新单个子项目

```bash
node bin/cli.js ai-aigc
```

脚手架将自动：
1. 读取子仓库的 `README.md` 首行作为 Prompt 主题。
2. 注入 Vue 3 静态页面结构及标准配置文件。
3. 保留原有的 `.git` 配置与 `README.md`，不覆盖个性化内容。

### 批量同步所有子项目

```bash
node bin/cli.js all
```

将模板的最新变更（如 SSO 逻辑、额度控制）一键同步至全部 31 个子项目。

### Agent 配置维护接口

```bash
# 读取子项目配置
node bin/cli.js get ai-aigc

# 写入/更新配置（支持热更新 prompt、model、title、temperature 等）
node bin/cli.js set ai-aigc prompt "你是一名专业的情绪管理顾问..."
node bin/cli.js set ai-aigc model deepseek-chat
```

## 联系方式

- GitHub Issues: [提交反馈](https://github.com/WT-Agent/ai-aigc/issues)
- 邮箱: us@wuxian.xyz

## 打赏支持

如果本项目对您有帮助，欢迎请作者喝杯咖啡。您的支持是持续维护与更新的动力。

<div align="center">

**微信支付** | **支付宝**
:---:|:---:
<img src="https://ai.wuxian.xyz/assets/tenpay.png" width="200" alt="微信支付"> | <img src="https://ai.wuxian.xyz/assets/alipay.png" width="200" alt="支付宝">

</div>

## 版权与许可

本项目基于 MIT License 开源协议。

Copyright (c) 2026. All rights reserved.
