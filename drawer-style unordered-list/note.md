# 笔记

## 1. `min-height: 100vh;` 的作用
- 设置 **`min-height: 100vh;`** 是为了让整个 **`body`** 元素垂直居中。
- 使用 **`100vh`** 可以确保元素填满整个屏幕高度。
- 使用 **`min-height: 50%`** 可能导致内容不垂直居中，特别是在内容高度超过这个值时。

---

## 2. 关于 `<li>` 标签中的 `style="--i:7;"`
- **`--i`** 是 **CSS 自定义属性**，允许在 CSS 中动态使用和管理样式。
- 可以使用 **`var(--i)`** 来获取这个变量的值，以控制样式。

---

## 3. 解释 `z-index: calc(1 * var(--i));`
- **`z-index`** 控制元素的堆叠顺序，值越大，元素越在上。
- 使用 **`calc(1 * var(--i))`** 根据 `--i` 的值动态设置 `z-index`，实现视觉上的层叠效果。

---

## 4. `transition: 1s;` 的作用
- 表示元素在属性变化时的过渡效果，过渡持续 **1 秒**。
- 可以使用户体验更流畅，常用于 **颜色**、**位置** 等属性的变化。

---

## 5. 使用 `display: block;` 而不是 `flex`
- **`display: block;`** 允许链接占据整个父元素宽度，使得用户更容易点击。
- 使用 **`flex`** 需要更多的设置，不如 **`block`** 简单直观。

---

## 6. `text-transform: uppercase;` 的解释
- 将文本转换为 **大写字母**，无论原始文本形式如何。
- 例如，**`Title 1`** 将在页面显示为 **`TITLE 1`**。

---

## 7. `transform: translate(40px, 40px);` 的作用
- 对元素应用 **平移变换**，将其向右和平移 **40 像素**，向下和平移 **40 像素**。
- 结合 **`transition`** 属性，使得动画平滑过渡，增加视觉效果。

---

## 8. 关于 `position: absolute;`
- 使用 **`absolute`** 允许精确控制伪元素的位置，脱离文档流。
- 如果用 **`relative`**，元素仍占据空间，定位可能不符合预期。

---

## 9. `content: attr(data-text);` 的解释
- 在伪元素中显示元素的 **`data-text`** 属性值。
- 允许在不修改 HTML 的情况下，动态显示关联信息。

---

## 10. 什么是伪元素？
- **伪元素** 是 CSS 中用于在元素的特定部分插入内容或样式的选择器。
  - 常用的伪元素有：
    - **`::before`**：在元素内容前插入。
    - **`::after`**：在元素内容后插入。
    - **`::first-line`** 和 **`::first-letter`**：用于样式化文本的第一行和首字母。
- **优点**：增强网页设计的灵活性和美观性，而不修改 HTML 结构。

---

```css
/* 示例代码 */
ul li:hover {
    background-color: #0030a0;
    transform: translate(40px, 40px);
    transition: 1s;
}
