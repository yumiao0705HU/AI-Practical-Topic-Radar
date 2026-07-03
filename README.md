# AI Practical Topic Radar

一个面向 AI 实践者的通用 Agent 工作流，用来发现“小红书 / B站 / 抖音 / GitHub / 网页搜索”上已经有人做出来的 AI 实操案例，并判断哪些值得尝试、复现、改造成教程或做成 demo。

它不是泛泛的 AI 新闻雷达，也不是“10 个 AI 工具推荐”。它更关注具体玩法，例如：

- `Codex + 营销竞品分析`
- `Coze + 小红书内容工作流`
- `Dify + 企业知识库客服`
- `n8n + 线索收集和跟进`
- `ComfyUI + 电商产品图`
- `AI Agent + 日记复盘`
- `AI Agent + 简历优化`
- `AI Agent + 文件整理`

## 适合谁

- AI 实践者
- 自媒体/内容创作者
- 产品经理
- 运营和增长团队
- 开发者和独立开发者
- 学生和自学者
- 企业内部 AI 推动者

这个工作流是平台无关的，可以复制到 ChatGPT、Claude、Gemini、Cursor、Coze、Dify、自建 Agent 等工具里使用。仓库里也包含一个 Codex skill 适配版。

## 核心逻辑

- 如果用户给了主题，就围绕主题检索平台案例，例如 `Codex + 营销`。
- 如果用户没给主题，就自动组合热点工具、工作流平台和场景。
- 默认来源包括小红书、B站、抖音、GitHub 和网页搜索。
- 默认不使用 YouTube，因为部分国内用户访问不稳定；用户明确要求全球视频教程时才加入。
- 优先找博主、创作者、开发者或项目作者已经发出来的具体操作，而不是基础教程合集。
- 每条推荐都要能回答：它具体做了什么、哪里有趣、能不能复现、适合谁、风险是什么。

## 默认热点组合

工具和 Agent：

- Codex
- Claude Code
- OpenClaw
- WorkBuddy
- Cursor
- Qwen Code
- Kimi
- 豆包

工作流平台：

- Coze
- Dify
- n8n
- 飞书 / Lark
- 剪映
- ComfyUI
- 本地脚本 / MCP 工作流

场景：

- 营销：图片、视频、策略、竞品、账号研究、内容日历、广告文案、落地页、线索收集
- 办公：文件整理、文档总结、会议纪要、邮件草稿、报告、PPT、表格、合同审阅
- 个人规划：简历、求职、面试、日记复盘、周计划、日程、习惯追踪、个人 CRM
- 知识工作：个人知识库、企业知识库、课程笔记、论文阅读、研究表格、搜索助手、简报
- 产品商业：用户反馈分析、PRD、客服、需求澄清、定价研究、销售话术
- 创意生产：产品图、封面图、短视频、分镜、字幕、配音、视觉风格探索

## 文件说明

- [universal-prompt.md](./universal-prompt.md)：通用 Agent prompt，可复制到任何 Agent 中使用。
- [source-guide.md](./source-guide.md)：各平台来源策略和质量判断。
- [scoring-rubric.md](./scoring-rubric.md)：评分和过滤规则。
- [examples/daily-radar-example.md](./examples/daily-radar-example.md)：输出示例。
- [codex-skill/SKILL.md](./codex-skill/SKILL.md)：Codex skill 适配版。

## 快速使用

复制 [universal-prompt.md](./universal-prompt.md) 到任意 Agent，然后输入：

```text
按照这个工作流，帮我跑今天的 AI 实操案例雷达。
```

指定主题：

```text
帮我找 Codex + 营销 的实操案例，重点看小红书、B站、抖音、GitHub 和网页搜索里有没有博主做过有意思的玩法。
```

无主题自动组合：

```text
跑一次今天的 AI Practical Topic Radar。你自己从 Codex、Claude Code、OpenClaw、WorkBuddy、Coze、Dify、n8n、营销、办公、个人规划、知识库、图片、视频、网站、表格这些方向里组合热点主题，然后找 10 个值得尝试或复现的案例。
```

分析用户给的资料：

```text
我发你几个 B站/小红书/抖音/GitHub 链接，请按照这个工作流判断哪些最值得复现，哪些只是噪音。
```

## Codex Skill 使用方式

如果你使用 Codex，可以把 `codex-skill/` 里的内容复制到本地 Codex skills 目录，例如：

```text
.codex/skills/ai-practical-topic-radar/
```

然后可以这样触发：

```text
用 ai-practical-topic-radar 跑一下今天的 AI 实操案例雷达
```

或者：

```text
帮我找 Coze + 小红书运营 的实操案例
```

## 输出重点

每条推荐会尽量包含：

- 自动组合或主题匹配
- 原始内容链接：视频、帖子、仓库、文章或官方页
- 博主/项目名称
- 案例具体做什么
- 最值得借鉴的有趣操作
- 中国可落地性
- 30 / 60 / 90 分钟实操路径
- 可交付物
- 难度、风险和推荐动作

## 注意事项

- 如果当前 Agent 不能联网，请提供链接、笔记、截图、评论或复制的网页内容。
- 如果某个平台不可访问，应说明限制，并用其他来源交叉验证。
- 不要编造链接、日期、播放量、点赞数或评论反馈。
- 不要只按 star、点赞、播放量判断质量。
- 对“自动赚钱”“无人运营”“爆款保证”等内容要降级处理，只保留可复现流程。
