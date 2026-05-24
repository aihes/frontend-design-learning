# Resume Site Skill Variants

同一份简历内容，用不同设计 skill 的方法各生成一套独立站点，方便比较哪种方法适合 Offer-Compass 的“上传简历生成个人网站”功能。

## 对比入口

打开：

```text
http://127.0.0.1:8765/outputs/resume-sites/yuziwei/skill-variants/index.html
```

Codex 前端设计总手册：

```text
http://127.0.0.1:8765/outputs/resume-sites/yuziwei/codex-frontend-design-playbook/index.html
```

## 变体清单

| Skill | 路径 | 设计方向 | 适合场景 |
|---|---|---|---|
| `frontend-design` | `frontend-design-dossier/index.html` | 候选人档案 / dossier，强视觉记忆点 | 对外传播、需要让页面显得明显不同于普通简历模板 |
| `design-taste-frontend` | `design-taste-frontend/index.html` | 非对称、低卡片依赖、高级克制 | 想提升审美和前端工程感，避免模板味 |
| `landing-page-design` | `landing-page-design/index.html` | 转化页，above-the-fold、CTA、信任证据 | 想把简历网站做成获客钩子，吸引留学生/候选人 |
| `design-shotgun` | `design-shotgun-editorial/index.html` | 强探索、编辑海报式、视觉冲击强 | 早期找方向，先看哪个视觉方向更有感觉 |
| `claude-page-review` | `claude-page-review/index.html` | 克制发布版，少而强，文案清晰 | 最稳妥，适合真实发给 HR、内推人、业务面试官 |
| `design-consultation` | `design-consultation-system/index.html` | 设计系统版，强调可复用模板结构 | 最适合沉淀为 Offer-Compass 产品模板 |
| `dark-minimal` | `claude-synthesis/index.html` | 暗色极简、强首屏、微动效 | 适合现代产品型个人主页，但给 HR 时可能稍冷 |
| `interactive-portfolio` | `interactive-portfolio-template/index.html` | 30 秒作品集、项目 case study、明确 CTA | 适合展示个人项目和真实成果，偏 portfolio |
| `tailwind-design-system` | `tailwind-design-system-template/index.html` | CSS tokens、语义色、组件 primitives | 适合沉淀成产品模板系统，方便后续自动生成 |
| `shadcn-layouts` | `shadcn-layouts-shell/index.html` | app shell、侧栏、顶部栏、稳定 grid/scroll | 适合产品后台/仪表盘式候选人视图，不像传统个人站 |
| `frontend-css-patterns` | `frontend-css-patterns-poster/index.html` | 强 typography、有限配色、错位构图 | 适合视觉探索和传播物料，正式投递需收敛 |

## 当前初步判断

- 如果目标是“线上可发布、给 HR/内推人看”：优先看 `claude-page-review`。
- 如果目标是“吸引留学生、作为转化钩子”：优先看 `landing-page-design`。
- 如果目标是“让生成结果显得不模板化”：优先看 `frontend-design` 和 `design-taste-frontend`。
- 如果目标是“沉淀为 Offer-Compass 可复用模板”：优先看 `design-consultation-system`。
- 如果目标是“沉淀为更工程化的模板系统”：优先看 `tailwind-design-system-template`。
- 如果目标是“作品集个人主页”：优先看 `interactive-portfolio-template`。
- 如果目标是“CSS 风格探索”：优先看 `frontend-css-patterns-poster`。
- 如果目标是“先探索审美方向”：优先看 `design-shotgun-editorial`。

## 验证记录

已通过 Playwright 在 390px 移动宽度下检查第一批 6 个变体。第二批模板 skill 变体已生成并做基础结构检查：

- 11 个变体均已接入对比入口。
- 新增 4 个模板 skill 变体均包含 `viewport`、联系入口、姓名和三个核心项目。
- 新增 4 个模板 skill 变体未依赖外部 CDN。
- `documentWidth` 和 `bodyWidth` 均为 390。
