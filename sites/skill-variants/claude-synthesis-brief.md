# Claude Synthesis Brief

请在当前仓库中做一个新的简历个人网站设计版本，用来评估 Claude 的页面设计效果。

## 工作目录

本机 `Offer-Compass-context` 项目目录。

## 背景

我们已经用同一份简历内容生成了 6 个不同前端设计 skill 的版本：

- `outputs/resume-sites/yuziwei/skill-variants/frontend-design-dossier/index.html`
- `outputs/resume-sites/yuziwei/skill-variants/design-taste-frontend/index.html`
- `outputs/resume-sites/yuziwei/skill-variants/landing-page-design/index.html`
- `outputs/resume-sites/yuziwei/skill-variants/design-shotgun-editorial/index.html`
- `outputs/resume-sites/yuziwei/skill-variants/claude-page-review/index.html`
- `outputs/resume-sites/yuziwei/skill-variants/design-consultation-system/index.html`

还有一篇总结文章：

- `outputs/resume-sites/yuziwei/skill-variants/frontend-design-skills-blog.md`

## 你的任务

请基于上面 6 个版本和总结文章，重新设计并实现一个新的网页版本：

- 新目录：`outputs/resume-sites/yuziwei/skill-variants/claude-synthesis/`
- 主文件：`outputs/resume-sites/yuziwei/skill-variants/claude-synthesis/index.html`
- 说明文件：`outputs/resume-sites/yuziwei/skill-variants/claude-synthesis/notes.md`

并且更新：

- `outputs/resume-sites/yuziwei/skill-variants/index.html`

在对比入口里加入这个新版本的卡片链接。

## 设计目标

这不是再做一个花哨页面，而是要验证 Claude 在“真实应届生/实习生个人网站”这个场景下的设计能力。

请综合这 6 个 skill 的优点：

- `frontend-design`：要有识别度，不要像默认 AI 模板。
- `design-taste-frontend`：要有高级前端审美，避免堆卡片、堆渐变、堆居中大标题。
- `landing-page-design`：首屏要清楚，用户知道为什么继续看、为什么联系。
- `design-shotgun`：允许有明确视觉方向，但要收敛到可发布。
- `claude-page-review`：内容要克制可信，适合发给 HR、内推人、业务面试官。
- `design-consultation`：结构要可复用，未来能沉淀成 Offer-Compass 的模板。

## 内容和约束

- 使用现有页面中的简历内容，不要编造经历、奖项、指标或公司背书。
- 候选人定位：产品 / AI / 产品运营实习方向，应届生/本科生。
- 重点突出：两个独立产品、AI 工具使用能力、真实上线/访问/UGC、内容运营和产品拆解能力。
- 页面可以是中文为主，可以少量英文作为视觉标签，但不要装成海外高端模板。
- 单文件 HTML + 内联 CSS/JS 即可，不依赖外部 CDN，不需要构建。
- 移动端必须可读，无横向滚动。
- 不要暴露任何内部 agent、skill、Claude、Codex、cmux 等实现细节到网页正文里。
- 不要修改已有 6 个版本目录里的文件。

## 输出要求

请实际编辑文件。完成后，在最终回复里列出：

- 你新增或修改了哪些文件
- 你采用的核心设计策略
- 你认为相比已有 6 个版本改进在哪里
- 是否做了基本自检
