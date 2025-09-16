# 修改日志

## 2025-09-16

### 修改内容：修复夜晚模式下"当前莎莎语录总数"文本颜色问题

**文件：** `layouts/gallery-home.html`
**行数：** 第18行
**问题：** 夜晚模式下"当前莎莎语录总数"文本颜色为灰色（gray-300），可读性差
**解决方案：** 将夜晚模式下的文本颜色改为白色

**修改前：**
```html
<p class="hx:text-lg hx:text-gray-600 dark:hx:text-gray-300">当前莎莎语录总数：{{ $totalImages }}</p>
```

**修改后：**
```html
<p class="hx:text-lg hx:text-gray-600 dark:hx:text-white">当前莎莎语录总数：{{ $totalImages }}</p>
```

**修改说明：**
- 保持白天模式的颜色不变（`hx:text-gray-600`）
- 将夜晚模式的颜色从 `dark:hx:text-gray-300` 改为 `dark:hx:text-white`
- 提高了夜晚模式下文本的可读性和对比度