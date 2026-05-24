# design-consultation

## 适用场景

用于新项目或模板化能力的设计系统建立。目标是先形成设计源头，再写页面，避免颜色、字体、间距和组件规则散落在代码里。

## 输入

- 产品定位。
- 目标用户。
- 页面类型。
- 竞品或参考站点。
- 品牌关键词。
- 技术栈和组件库。

## 输出

- 设计方向。
- 字体、色彩、间距、圆角、阴影、动效规则。
- 组件使用原则。
- `DESIGN.md` 或等价设计系统文档。
- 预览页面或 token 示例。

## 工作流

1. 产品上下文。
   - 这个产品要被谁记住？
   - 它最重要的信任信号是什么？
   - 用户在这个页面上要完成什么判断？

2. 参考研究。
   - 选择同类产品和反差参考。
   - 抽象信息架构、视觉密度、字体、色彩、CTA。
   - 不复制品牌资产。

3. 完整提案。
   - Aesthetic direction：页面气质。
   - Typography：display/body/mono。
   - Color：背景、文字、强调、状态色。
   - Spacing：section、grid、组件内部间距。
   - Layout：容器宽度、断点、信息优先级。
   - Motion：只保留服务理解的动效。

4. 风险设计。
   - 安全项保证一致性。
   - 风险项建立记忆点。
   - 每个风险都要说明收益和代价。

5. 写入设计源头。

## DESIGN.md 模板

```markdown
# Design System

## Product Context

## Aesthetic Direction

## Typography

## Color

## Spacing

## Layout

## Components

## Motion

## Decisions Log
```

## 验收标准

- 有明确视觉立场。
- token 能落到代码。
- 组件规则能复用。
- 风险项不是装饰，而是服务产品记忆点。
- 后续页面不会靠即兴 CSS 维持一致性。

