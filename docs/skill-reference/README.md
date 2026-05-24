# Frontend Design Skill Reference

这是本仓库的公开 Skill 参考版。它不是本机 Skill 原文备份，而是把本次实验里真正有用的方法抽成可分享、可复现的参考文档。

公开原则：

- 不包含本机绝对路径、公司名、内部主机、内部项目和账号信息。
- 不依赖某个私有 Skill 源码。读者可以直接把对应参考文档作为 prompt 或工作流说明给 Codex 使用。
- 保留可执行的判断框架：什么时候用、需要什么输入、输出什么、怎么验收。
- 不复制参考站点、品牌资产、客户数据或无法验证的指标。

## 推荐使用顺序

| 阶段 | 参考文件 | 用途 |
| --- | --- | --- |
| 1. 叙事重组 | [interactive-portfolio.md](interactive-portfolio.md) | 把简历或作品集从时间顺序改成证明顺序。 |
| 2. 视觉方向 | [frontend-design.md](frontend-design.md) | 选择明确页面气质，避免通用 AI 模板。 |
| 3. 多方案探索 | [design-shotgun.md](design-shotgun.md) | 方向不确定时先生成多套差异化方案。 |
| 4. 审美校准 | [design-taste-frontend.md](design-taste-frontend.md) | 清理紫蓝渐变、三列卡片、默认字体等 AI 味。 |
| 5. 设计系统 | [design-consultation.md](design-consultation.md) | 沉淀品牌、字体、颜色、间距、动效和设计原则。 |
| 6. Tailwind 落地 | [tailwind-design-system.md](tailwind-design-system.md) | 把设计方向变成 token 和组件 primitive。 |
| 7. 布局稳定 | [shadcn-layouts.md](shadcn-layouts.md) | 处理 app shell、高度链、滚动和 grid/flex 问题。 |
| 8. CSS 细节 | [frontend-css-patterns.md](frontend-css-patterns.md) | 提供字体、色彩、动效、背景和空间组合模式。 |
| 9. 转化页 | [landing-page-design.md](landing-page-design.md) | 设计 landing page 的首屏、CTA 和信任证据。 |
| 10. 发布审查 | [claude-page-review.md](claude-page-review.md) | 用第二模型视角检查文案、层级、真实性、隐私和移动端。 |

## 一条可复用总指令

```text
你要设计一个用户可见的前端页面。先不要直接写代码。

按下面顺序执行：
1. 用 interactive-portfolio 方法确认页面叙事：目标用户、首屏问题、最强证据、CTA。
2. 用 frontend-design 方法选择一个明确视觉方向，并解释为什么适合这个页面。
3. 如果方向不确定，用 design-shotgun 生成 3 个差异明显的方向，再选一个深化。
4. 用 design-consultation 输出字体、颜色、间距、组件、动效和禁用项。
5. 如果使用 Tailwind/shadcn，用 tailwind-design-system 和 shadcn-layouts 固化 token、组件和布局约束。
6. 用 frontend-css-patterns 补足排版、背景、动效和响应式细节。
7. 实现后用 design-taste-frontend 做反 AI 味检查。
8. 发布前用 claude-page-review 的标准检查文案、真实性、隐私和移动端截图。

不要编造数据、客户、奖项、推荐语或联系方式。不要暴露本机路径、内部项目名、公司名、账号信息和不可公开的运行环境。
```

