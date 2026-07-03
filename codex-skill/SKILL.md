---
name: ai-practical-topic-radar
description: Find China-landable creator/platform AI practice cases around a user's seed topic, such as Codex + marketing, Coze + Xiaohongshu operations, Dify + knowledge base, AI Agent + diary/video/image/website/spreadsheet workflows, or practical AI demos. Use this skill whenever the user asks for practical AI cases, interesting creator operations, Xiaohongshu/Bilibili/Douyin AI trends, GitHub AI projects tied to a case, AI workflow ideas, daily AI practice radar, demo ideas, or actionable AI learning/share topics. Prioritize concrete posted cases over generic AI news, broad tool lists, or basic tutorials.
---

# AI Practical Topic Radar

Use this skill to find concrete creator/platform AI practice cases, tutorials, GitHub projects, tools, and workflows that AI practitioners can try, teach, share, or turn into demos.

This is the Codex adapter for the platform-neutral workflow in `AI-Practical-Topic-Radar/universal-prompt.md`. Follow the universal workflow behavior, but do not require the user to know or mention that file.

## Default Behavior

- Output in Chinese unless the user asks otherwise.
- Default to 10 concrete cases for a daily radar.
- Prioritize China-landable sources and workflows.
- Use Xiaohongshu, Bilibili, Douyin, GitHub, and general web search as default source families.
- Do not use YouTube as a default source. Add it only when the user explicitly asks for global video tutorial discovery.
- Reduce industry analysis to background context. Recommend industry information only when it becomes a concrete case, tutorial, workflow, demo, comparison, or adoption opportunity.
- Use Chinese field names in the final output.
- Prefer cases such as AI Agent + knowledge base, diary, video, image, website, spreadsheet, research, automation, coding, or personal assistant workflows.
- If the user gives a seed topic, stay close to that topic and search for creator/platform cases around it instead of searching broadly.
- If the user does not give a seed topic, generate timely combinations from hot AI agent tools, workflow platforms, and scenario families.
- Prefer interesting operations posted by creators or practitioners over basic beginner tutorials.

## Topic-Seeded Discovery

This skill is topic-seeded by default.

On first use or when the user gives no preference, proactively run the default hot-combination radar. Do not block on clarification. After the output, invite the user to steer the next run by providing interests, platforms, creators, links, screenshots, notes, or files.

If the user provides a current interest, search around that topic. Examples:

- Codex + marketing
- Coze + Xiaohongshu operations
- Dify + knowledge base
- AI Agent + diary
- ComfyUI + product image
- Jianying + AI video
- Qwen Code + website

For a seed topic, prioritize:

- Which creators posted an interesting operation
- What video, post, repo, or article can be inspected
- What the creator actually did
- What part is worth copying, adapting, or testing
- What is hype, title bait, or too basic

If the user does not provide a topic, generate seed topics automatically from the Hot Combination Matrix below. Pick 6-10 combinations that look timely and practical, then search for creator/platform cases around those combinations. Do not fall back to broad beginner tutorials.

For follow-up runs, prefer user-provided context over the default matrix:

- Interest keywords: e.g. `Codex + marketing`, `AI video`, `Dify + customer service`, `resume agent`.
- Platform preference: Xiaohongshu, Bilibili, Douyin, GitHub, blogs, official docs.
- Specific creators or accounts to track.
- Links to videos, posts, repos, articles, or product pages.
- Screenshots, copied comments, saved notes, browser bookmarks, or exported reading lists.
- Local files or notes, if the current agent can access them.

When the user provides source material, evaluate it directly and use web search only to verify freshness, alternatives, and reproducibility.

## Hot Combination Matrix

When no seed topic is provided, combine tools, workflow platforms, and scenarios.

Hot AI agent tools:

- Codex
- Claude Code
- OpenClaw
- WorkBuddy
- Cursor
- Qwen Code
- Kimi
- Doubao
- Gemini CLI or similar coding/agent tools when relevant

Workflow and automation platforms:

- Coze
- Dify
- n8n
- Feishu/Lark
- Jianying
- ComfyUI
- Make/Zapier only when China landing is realistic
- Local scripts or MCP workflows

Scenario families:

- Marketing: image generation, video generation, campaign strategy, competitor research, account research, content calendar, Xiaohongshu/Douyin/Bilibili operations, ad copy, landing page, lead list.
- Office work: file organization, document summarization, meeting notes, email drafts, report generation, PPT outline, spreadsheet cleanup, contract review.
- Personal planning: resume, job search, interview prep, diary review, weekly planning, schedule assistant, habit tracker, personal CRM.
- Knowledge work: personal knowledge base, company knowledge base, course notes, paper reading, research table, search assistant, briefing.
- Product and business: user feedback analysis, PRD draft, support bot, requirement clarification, pricing research, sales script.
- Creative production: product image, cover image, short video, storyboard, subtitle, voiceover, design style exploration.

Example auto-generated seed topics:

- Codex + marketing competitor research
- Claude Code + landing page generation
- OpenClaw + browser-based marketing automation
- WorkBuddy + office file organization
- Coze + Xiaohongshu image/content workflow
- Dify + company knowledge base
- n8n + lead collection and follow-up
- ComfyUI + product image batch workflow
- Jianying + AI short video production
- Feishu + meeting notes and task follow-up
- AI Agent + resume optimization
- AI Agent + diary review and weekly planning

## Default Daily Mix

For a daily radar without a seed topic, produce 10 concrete cases from auto-generated combinations:

- 6 creator/platform cases from Xiaohongshu, Bilibili, Douyin, blogs, or community posts
- 2 GitHub or open-source projects that make a case reproducible
- 1 tool/product case with a clear workflow
- 1 industry signal translated into a concrete case

## Selection Rules

Recommend an item only when it has at least two:

- Concrete use case or workflow
- Reachable video, post, repo, tutorial, or official page
- Specific creator/platform operation worth inspecting
- Evidence of demand or repeated user pain
- Visible output a user can reproduce
- China-landable path or realistic local alternative
- Clear value for learning, productivity, content, product, operation, or business

Downgrade or skip:

- Generic AI news
- Title bait
- Pure marketing
- Stale tutorials
- Abandoned repos with no usable instructions
- Basic introductions with no interesting operation
- Tools that cannot be accessed or replaced from China
- Items with no 30/60/90 minute practical path

## Output Format

Start with one short Chinese sentence summarizing today's practical theme.

For each of the 10 items, include:

- 名称
- 自动组合：如果是自动生成的主题，写出工具 + 场景组合
- 主题匹配：它和用户给的主题有什么关系
- 案例类型：知识库 / 日记 / 视频 / 图片 / 网站 / 表格 / 研究 / 自动化 / 编程 / 其他
- 来源：小红书 / B站 / 抖音 / GitHub / 官方文档 / 网页搜索 / 社区
- 原始内容：视频 / 帖子 / 仓库 / 文章 / 官方页，附链接和日期，能给就给
- 博主/项目：作者、账号或项目名，能确认就写
- 适合谁：开发者 / 产品 / 运营 / 创作者 / 设计师 / 学生 / 独立开发者 / 企业团队
- 这个案例具体做什么
- 有趣操作：它最值得借鉴的操作是什么
- 中国可落地性：访问、成本、中文资料、国内替代、部署、合规
- 实操路径：30 / 60 / 90 分钟能做什么
- 可交付物：demo / 模板 / 清单 / SOP / 对比表 / 教程 / 内部分享 / 小工具
- 难度：低 / 中 / 高
- 风险：过期、收费、访问限制、部署复杂、效果不稳定、合规
- 推荐动作：收藏 / 试用 / 对比 / 做教程 / 做 demo / 搭工作流 / 暂不推荐

End with `已过滤噪音` only when there are obvious noisy items worth warning about. Do not add a separate weekly checklist unless the user asks.

When useful, add a short `下次可以这样定制` section with 2-4 concrete prompts the user can give next time. Keep it brief and practical. Examples:

- `下次可以指定：Codex + 营销竞品分析`
- `也可以发 3 个 B站/小红书链接，我只判断哪些值得复现`
- `可以指定平台：只看小红书和 GitHub`
- `可以上传截图/笔记，我会从里面筛案例`

## Source Quality Checks

- GitHub: check README, setup steps, recent commits/releases, issues, license, demo, and whether setup is safe.
- Xiaohongshu: look for concrete workflow, comments asking how to reproduce, result screenshots, and tool accessibility.
- Bilibili: prefer complete walkthroughs, visible steps, current links, dependency versions, and comment feedback.
- Douyin: use as a fast demand signal, but verify with another source before treating it as a strong recommendation.
- Web search: prefer official docs for product claims and recent tutorials for fast-changing tools.

## Style

- Be practical, specific, and skeptical.
- Prefer concrete cases over broad categories.
- Prefer creator/platform operations over basic tutorials.
- Stay close to the user's seed topic.
- Keep each item concise.
- Do not over-rely on stars, likes, or view counts.
- Do not invent links, dates, engagement, or source claims.
- If browsing is unavailable, ask the user for links or source material and evaluate what they provide.
