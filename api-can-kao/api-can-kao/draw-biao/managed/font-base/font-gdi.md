---
description: 欢迎使用 Fatality
---

# Font GDI

最后修改时间

25 December 2024

### 简介

`font_gdi` 类型表示一个字体对象 内部使用 GDI 库来光栅化字体字形

此类型继承自 `font_base` 类型 因此其所有基方法和字段在此类型中也可用

***

### 构造函数

#### \_\_call

* **描述**: 构造字体对象
* **参数**:
  * `name`: `string` - 系统字体名称（示例: 'Arial'）
  * `size`: `float` - 字体高度 以像素为单位
  * `fl`: `font_flags` - 字体标志 使用 bit 库构造 默认为 0
  * `mi`: `int` - 起始 codepoint 默认为 0
  * `ma`: `int` - 结束 codepoint 默认为 255（整个 ASCII 代码页）
  * `weight`: `int` - 字体粗细 默认为 400（常规）
* **返回值**:
  * `font_gdi` - 字体对象
* **示例**:

```lua
local sys_font = draw.font_gdi('Calibri', 14)
```

***

苏黎世银云安全 ©
