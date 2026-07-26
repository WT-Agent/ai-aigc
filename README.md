<div align="center">

# 网腾无限 AI - 网腾无限AI - AIGC多模态创作专家

**[基于 Vue 3 + Vite + Vanilla CSS 构建的 网腾无限AI - AIGC多模态创作专家 智能实战微应用，具备深色玻璃拟态自适应交互与微信端 H5 体验]**

[Vue 3] · [TypeScript] · [Vite] · [Vanilla CSS] · [开源协议 MIT]

[![GitHub stars](https://img.shields.io/github/stars/WT-Agent/ai-aigc?style=social)](https://github.com/WT-Agent/ai-aigc)
[![GitHub license](https://img.shields.io/github/license/WT-Agent/ai-aigc)](https://github.com/WT-Agent/ai-aigc/blob/main/LICENSE)
[![Online Demo](https://img.shields.io/badge/Online_Demo-aigc.wuxian.xyz-indigo?style=flat-square)](https://aigc.wuxian.xyz)

[在线演示](https://aigc.wuxian.xyz) · [快速启动](#快速启动) · [核心特性](#核心特性) · [脚手架集成](#脚手架集成说明) · [支持一下](#打赏支持)

</div>

---

## 团队与产品简介

团队成员均来自 C9 等顶尖学府，由字节、腾讯、阿里的资深工程师组成，全职创业研发开源 AI 微应用矩阵产品，旨在让所有人都能零门槛感受 AIGC 的生产力魅力。

**网腾无限AI - AIGC多模态创作专家** 专注于“**你是一位顶尖高校学术委员会专家、国际顶级期刊审稿人兼 AIGC 学术生成特征分析导师。你需要针对用户提供的论文段落/摘要/全文大纲，以及用户选择的“润色模式（如：重度降重去AI痕迹、顶刊学术语体润色、逻辑衔接与结构强化、查重报告针对性改写）”、“目标学科（工学技术/理学基础/医学医药/人文社科/经济管理）”、“降重强度（极致去AI化/中度自然润色/轻度语法修饰）”，为用户生成一份极具学术严谨度与可读性的【AIGC 论文降重与重构润色对比报告】。内容必须包含以下 4 个标准模块：
1. 【AIGC 痕迹诊断与风险分析】：指出原句中过于平庸或典型的 AI 逻辑连词（如“此外”、“总而言之”、“不可否认”）及固定特征套话。
2. 【重构后学术正文 (去AI化/强逻辑)】：提供高度学术化、避开 AI 查重算法检测的高质量重写段落。
3. 【修改对照与核心替换词库】：列出关键专业词汇与句式重组的前后对比。
4. 【学术投稿与查重避坑建议】：针对该学科提供 2-3 条防止 AI 判定度超标的学术写作建议。

请在回复的最后，根据你的学术评估给出该重构方案的【AI共识打分】（1-5分），格式必须严格如下（换行写入且不能有任何多余字符，以便前端自动解析）：
[AIGC_SCORES]aigcReduction:数字,academicTone:数字,logicCohesion:数字,vocabRichness:数字,readability:数字[/AIGC_SCORES]
注意：[AIGC_SCORES]...[/AIGC_SCORES] 必须是回复的最后一小行，里面的“数字”只能是1到5之间的正整数。**”。我们剔除了冗余概念，不搞虚假宣传，只提供极致优雅、即调即用的高完成度微应用前端与边缘网关接口。

**我们不搞概念，不卖课，只写能跑起来的代码。**

欢迎 Star、Fork、提 Issue，一起让这个开源 AI 工具生态变得更好用。

---

## 核心特性

- **极简自适应交互**：采用极具现代感与科幻氛围的深色玻璃拟态 (Glassmorphic Dark UI) 设计，全量兼容移动端微信 H5 与 PC 响应式体验。
- **纯静态零成本部署**：架构保持 100% 静态化，无额外 Server 依赖，支持一键托管至 Cloudflare Pages、Vercel、GitHub Pages 或 CDN/OSS 静态存储。
- **安全代理与双模型网关**：内置安全开发代理中转层，支持无缝接入 DeepSeek-V3/R1 文本大模型及通义千问/通义万相多模态生图 API。
- **多维度评分与案例展示**：集成 AI 共识多指标看板、动态用户活跃跑马灯 ticker、精彩场景 Preset 案例以及生成卡片截图分享功能。
- **微信/钉钉双通道联系**：全量内置微信交流与钉钉联系双二维码组件，支持灵活的裂变锁屏与额度留存管理。

---

## 核心功能与使用场景

1. **智能 Prompt 场景引擎**：针对 **你是一位顶尖高校学术委员会专家、国际顶级期刊审稿人兼 AIGC 学术生成特征分析导师。你需要针对用户提供的论文段落/摘要/全文大纲，以及用户选择的“润色模式（如：重度降重去AI痕迹、顶刊学术语体润色、逻辑衔接与结构强化、查重报告针对性改写）”、“目标学科（工学技术/理学基础/医学医药/人文社科/经济管理）”、“降重强度（极致去AI化/中度自然润色/轻度语法修饰）”，为用户生成一份极具学术严谨度与可读性的【AIGC 论文降重与重构润色对比报告】。内容必须包含以下 4 个标准模块：
1. 【AIGC 痕迹诊断与风险分析】：指出原句中过于平庸或典型的 AI 逻辑连词（如“此外”、“总而言之”、“不可否认”）及固定特征套话。
2. 【重构后学术正文 (去AI化/强逻辑)】：提供高度学术化、避开 AI 查重算法检测的高质量重写段落。
3. 【修改对照与核心替换词库】：列出关键专业词汇与句式重组的前后对比。
4. 【学术投稿与查重避坑建议】：针对该学科提供 2-3 条防止 AI 判定度超标的学术写作建议。

请在回复的最后，根据你的学术评估给出该重构方案的【AI共识打分】（1-5分），格式必须严格如下（换行写入且不能有任何多余字符，以便前端自动解析）：
[AIGC_SCORES]aigcReduction:数字,academicTone:数字,logicCohesion:数字,vocabRichness:数字,readability:数字[/AIGC_SCORES]
注意：[AIGC_SCORES]...[/AIGC_SCORES] 必须是回复的最后一小行，里面的“数字”只能是1到5之间的正整数。** 领域进行了深度提示词工程优化与共识打分约束。
2. **多风格预设切换**：提供专业干练、高情商说辞、幽默风趣、严谨学术（或写真照片、卡通动漫等多模态）风格的一键切换。
3. **一键复制与卡片分享**：支持生成内容的快速复制，以及渲染结果的截图分享导出。
4. **统一 SSO 额度管理**：接入 wuxian.xyz 共享登录凭证，支持每日免费额度计数与登录解锁。

---

## 快速启动

### 1. 克隆项目
```bash
git clone https://github.com/WT-Agent/ai-aigc.git
cd ai-aigc
```

### 2. 安装依赖
项目推荐使用 `pnpm` 作为包管理器：
```bash
pnpm install
```

### 3. 配置环境变量
复制并配置本地开发环境变量：
```bash
cp .env.example .env
```
在 `.env` 中填入您的 API Key：
- `DEEPSEEK_API_KEY`: 您的 DeepSeek 开发者 API Key（用于文本类微应用）
- `DASHSCOPE_API_KEY`: 阿里 DashScope API Key（用于多模态生图微应用）

### 4. 启动本地开发
```bash
pnpm dev
```
启动后在浏览器打开控制台提示的本地开发地址即可进行调试。

---

## 脚手架集成说明

本微应用由私有总控仓库 `ai.wuxian.xyz` 中的运维脚手架统一管理，支持通过 CLI 进行批量更新与配置维护：

```bash
# 自动化发版与发布
node bin/cli.js publish ai-aigc

# 查看当前微应用配置
node bin/cli.js get ai-aigc

# 动态热更新提示词或模型映射
node bin/cli.js set ai-aigc prompt "你是一位顶尖高校学术委员会专家、国际顶级期刊审稿人兼 AIGC 学术生成特征分析导师。你需要针对用户提供的论文段落/摘要/全文大纲，以及用户选择的“润色模式（如：重度降重去AI痕迹、顶刊学术语体润色、逻辑衔接与结构强化、查重报告针对性改写）”、“目标学科（工学技术/理学基础/医学医药/人文社科/经济管理）”、“降重强度（极致去AI化/中度自然润色/轻度语法修饰）”，为用户生成一份极具学术严谨度与可读性的【AIGC 论文降重与重构润色对比报告】。内容必须包含以下 4 个标准模块：
1. 【AIGC 痕迹诊断与风险分析】：指出原句中过于平庸或典型的 AI 逻辑连词（如“此外”、“总而言之”、“不可否认”）及固定特征套话。
2. 【重构后学术正文 (去AI化/强逻辑)】：提供高度学术化、避开 AI 查重算法检测的高质量重写段落。
3. 【修改对照与核心替换词库】：列出关键专业词汇与句式重组的前后对比。
4. 【学术投稿与查重避坑建议】：针对该学科提供 2-3 条防止 AI 判定度超标的学术写作建议。

请在回复的最后，根据你的学术评估给出该重构方案的【AI共识打分】（1-5分），格式必须严格如下（换行写入且不能有任何多余字符，以便前端自动解析）：
[AIGC_SCORES]aigcReduction:数字,academicTone:数字,logicCohesion:数字,vocabRichness:数字,readability:数字[/AIGC_SCORES]
注意：[AIGC_SCORES]...[/AIGC_SCORES] 必须是回复的最后一小行，里面的“数字”只能是1到5之间的正整数。"
node bin/cli.js set ai-aigc model deepseek-chat
```

---

## 联系我们

- **官方网站**: [https://aigc.wuxian.xyz](https://aigc.wuxian.xyz)
- **GitHub Issues**: [提交反馈](https://github.com/WT-Agent/ai-aigc/issues)
- **反馈邮箱**: us@wuxian.xyz
- **官方主页**: [ai.wuxian.xyz](https://ai.wuxian.xyz)

---

## 打赏支持

如果本项目对您的工作或学习有所帮助，欢迎请团队喝杯咖啡支持我们的开源维护！

<div align="center">

**微信支付** | **钉钉交流**
:---:|:---:
<img src="https://ai.wuxian.xyz/assets/weixin.png" width="200" alt="微信交流"> | <img src="https://ai.wuxian.xyz/assets/dingtalk.png" width="200" alt="钉钉联系">

</div>

---

## 版权与许可

本项目基于 **MIT License** 开源协议。

Copyright (c) 2026 [WangTeng.Tech](https://ai.wuxian.xyz). All rights reserved.
