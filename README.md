# Frontend Design Learning

这是一个围绕“如何让 Codex 做出更好的前端页面”的学习仓库。内容来自一次完整的简历站点设计实验：同一份候选人内容，用不同前端设计 Skill、外部设计工具和参考站点生成多套页面，再沉淀成可复用的方法论。

## 在线结构

打开本地首页：

```text
index.html
```

推荐学习顺序：

1. `sites/codex-frontend-design-playbook/index.html`  
   总手册：Skill 原理、外部参考站点、Codex 参考研究再重开发的完整流程。

2. `sites/skill-variants/index.html`  
   Skill 变体对比：同一份内容在不同设计方法下的页面效果。

3. `sites/design-tool-benchmark/index.html`  
   外部工具 benchmark：Variant、Relume、Godly、Land-book 等工具和参考库的截图与分析。

4. `sites/frontend-design-showcase/index.html`  
   前端设计原则展示页：用于观察页面节奏、排版、视觉密度和响应式策略。

5. `docs/skill-reference/index.html`  
   脱敏后的 Skill 公开参考入口：解释每个前端设计 Skill 的适用场景、输入、输出、工作流和验收标准。

6. `sites/original-candidate-site/index.html`  
   原始候选人站点：用于和后续变体对比。

## 内容边界

- 本仓库是静态 HTML 学习材料，不依赖 React、Next.js 或构建流程。
- 仓库内已移除真实邮箱、手机号和邮件跳转链接。
- 案例仍保留姓名、项目、学校和公开作品线索，用于保持设计学习的真实上下文。
- 如果要发布到公开 GitHub Pages，建议再做一次隐私扫描。

## 本地预览

在仓库根目录运行：

```bash
python3 -m http.server 8767
```

然后打开：

```text
http://127.0.0.1:8767/
```

本次验证截图：

- `screenshots/home-desktop.png`
- `screenshots/home-mobile.png`

## 学习重点

- 不要让 Codex 直接“做一个好看的页面”，要先做参考研究。
- Skill 负责原则，外部站点负责参考，Codex 负责重开发，Playwright 负责截图验收。
- 好看的前端不是只调 CSS，而是同时处理叙事、信息架构、视觉方向、设计系统、布局工程和发布审查。

## 公开前检查

```bash
rg -n --hidden -S "[A-Z0-9._%+-]+@[A-Z0-9.-]+\\.[A-Z]{2,}|mail\"\"to:|1[3-9][0-9]{9}" .
```

命令无输出时，说明没有常见邮箱、邮件跳转链接和中国大陆手机号格式命中。
