# frontend-css-patterns

## 适用场景

用于不绑定框架的 CSS 视觉细节：字体、颜色、动效、背景、空间组合和 Tailwind token 映射。

## 输入

- 设计方向或 token。
- 页面气质。
- 是否使用 Tailwind。
- 浏览器和性能约束。

## 输出

- CSS custom properties。
- 字体和排版尺度。
- 色彩主题。
- 动效模式。
- 背景纹理和空间组合。

## 关键模式

### 1. Token 优先

如果项目已有设计 token，不要重新发明颜色、字体和间距。

```css
:root {
  --color-bg: #faf7f0;
  --color-fg: #171512;
  --color-accent: #9f3f2c;
  --font-display: "Avenir Next", sans-serif;
}
```

### 2. 字体搭配

- Display 字体负责记忆点。
- Body 字体负责可读性。
- Mono 字体适合数据、编号、技术信息。

### 3. 色彩

- 使用有限 palette。
- 背景、文字、强调色先稳定。
- 不要把所有 section 都做成同色系变化。

### 4. 动效

高质量动效通常不是多，而是集中：

```css
@keyframes fade-in-up {
  from { opacity: 0; transform: translateY(16px); }
  to { opacity: 1; transform: translateY(0); }
}

.reveal {
  animation: fade-in-up 0.6s ease-out both;
}
```

### 5. 空间组合

- 通过非对称、重叠、留白和不同宽度制造节奏。
- 固定格式元素要用稳定尺寸。
- 不用 hover 状态改变布局尺寸。

## 验收标准

- CSS 变量清晰。
- 字体和页面气质匹配。
- 动效只影响 transform/opacity。
- 背景细节不影响可读性。
- 移动端没有文字溢出和横向滚动。

