# shadcn-layouts

## 适用场景

用于修正 Tailwind/shadcn 页面中的布局问题，尤其是 app shell、dashboard、全屏页面、滚动容器、flex/grid 和高度链。

## 输入

- 页面源码。
- 当前截图或问题描述。
- 期望布局。
- 使用的组件库和 Tailwind 版本。

## 输出

- 布局诊断。
- 修复后的 class 组合。
- 稳定的 app shell 或 grid 结构。
- 移动端回退规则。

## 核心模型

### 1. 高度链

`h-full` 只有在父元素有明确高度时才有效。

```tsx
<html className="h-full">
  <body className="h-full">
    <div className="h-full">...</div>
  </body>
</html>
```

### 2. flex 溢出

可滚动的 flex 子项通常需要 `min-h-0`。

```tsx
<div className="flex h-full flex-col">
  <header className="shrink-0">...</header>
  <main className="min-h-0 flex-1 overflow-y-auto">...</main>
</div>
```

### 3. grid 父子关系

`grid-cols-*` 必须和 `grid` 在父元素上一起出现。

```tsx
<div className="grid grid-cols-1 gap-4 md:grid-cols-3">
  <section>...</section>
</div>
```

### 4. 滚动容器

滚动容器必须有明确高度或被 flex/grid 约束，否则不会按预期滚动。

## 常见诊断

- SL1：高度链断了，`h-full` 没有效果。
- SL2：flex 子项没有 `min-h-0`，内容把容器撑开。
- SL3：只写了 `grid-cols-*`，没有写 `grid`。
- SL4：Tailwind content paths 或 CSS variables 配置错了。
- SL5：shadcn 组件依赖没有安装。

## 验收标准

- 桌面和移动端都没有横向滚动。
- 主内容区能滚动，导航和 header 不被挤压。
- 固定区域使用 `shrink-0`。
- 滚动区域使用 `min-h-0` 或明确尺寸。
- grid 在移动端能回退为单列。

