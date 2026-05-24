# tailwind-design-system

## 适用场景

用于把设计方向落到 Tailwind CSS 和 shadcn/ui 体系里。重点不是安装组件，而是建立 token、主题和封装后的 design-system primitive。

## 输入

- 设计方向或 `DESIGN.md`。
- Tailwind 版本。
- 是否使用 shadcn/ui。
- 需要的主题：light、dark、多品牌或单品牌。
- 组件范围：button、card、input、dialog、tabs 等。

## 输出

- CSS variables。
- Tailwind theme 映射。
- 组件 primitive。
- 主题切换策略。
- 校验命令和组件使用规则。

## 工作流

1. 确认 Tailwind 版本。
   - v3 和 v4 写法不同，不能混用。
   - 先看项目配置，再决定写法。

2. 定义 token。
   - background / foreground。
   - primary / primary-foreground。
   - secondary / secondary-foreground。
   - destructive / destructive-foreground。
   - radius、shadow、spacing、font。

3. 映射到 Tailwind。
   - CSS-first 项目用 CSS 变量和 `@theme`。
   - config-first 项目在 `tailwind.config` 中映射。

4. 包装组件。
   - 不直接在业务代码里到处使用原始 shadcn 样式。
   - 用 `components/ds/Button`、`components/ds/Card` 这类 wrapper 固定 variant、size、radius 和状态。

5. 校验。
   - build 通过。
   - dark mode 或主题切换可用。
   - 所有新增组件使用 token，而不是硬编码散色。

## Token 示例

```css
:root {
  --background: oklch(0.99 0 0);
  --foreground: oklch(0.15 0 0);
  --primary: oklch(0.55 0.18 250);
  --primary-foreground: oklch(0.98 0 0);
  --radius: 8px;
}
```

## 验收标准

- 颜色都有 foreground 配对。
- 组件通过 design-system wrapper 使用。
- 没有散落的十六进制颜色。
- radius、shadow、spacing 统一。
- shadcn 默认外观被改成项目自己的视觉语言。

