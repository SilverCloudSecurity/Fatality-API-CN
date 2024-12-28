---
description: 欢迎使用 Fatality
---

# Font

最后修改时间

25 December 2024

### 简介

`font` 类型表示一个字体对象 内部使用 FreeType 库来光栅化字体字形

此类型继承自 `font_base` 类型 因此其所有基方法和字段在此类型中也可用

***

### 构造函数

#### \_\_call

* **描述**: 构造字体对象
* **注意事项**: 传递无效指针或内存区域小于所需大小将导致崩溃
* **参数**:
  1. **从文件**
     * `path`: `string` - TTF/OTF 文件的路径
     * `size`: `float` - 字体高度 以像素为单位
     * `fl`: `font_flags` - 字体标志 使用 bit 库构造 默认为 0
     * `mi`: `int` - 起始 codepoint 默认为 0
     * `ma`: `int` - 结束 codepoint 默认为 255（整个 ASCII 代码页）
  2. **从内存**
     * `mem`: `ptr` - 指向内存中字体文件的指针
     * `sz`: `int` - 字体文件大小 以字节为单位
     * `size`: `float` - 字体高度 以像素为单位
     * `fl`: `font_flags` - 字体标志 使用 bit 库构造 默认为 0
     * `mi`: `int` - 起始 codepoint 默认为 0
     * `ma`: `int` - 结束 codepoint 默认为 255（整个 ASCII 代码页）
  3. **从内存 带 codepoint 对**
     * `mem`: `ptr` - 指向内存中字体文件的指针
     * `sz`: `int` - 字体文件大小 以字节为单位
     * `size`: `float` - 字体高度 以像素为单位
     * `fl`: `font_flags` - 字体标志 使用 bit 库构造 默认为 0
     * `pairs`: `table[{int, int}...]` - 最小/最大对 这是一个标准数组 包含 {int, int} 对
* **返回值**:
  * `font` - 字体对象
* **示例**:

```lua
local cool_font = draw.font('myfont.ttf', 16)
```

***

苏黎世银云安全 ©
