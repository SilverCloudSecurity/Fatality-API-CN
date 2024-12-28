---
description: 欢迎使用 Fatality
---

# Font Base

最后修改时间

25 December 2024

### 简介

`font_base` 类型表示字体类型的基类 无法直接创建此类型的实例 而应使用其子类型

此类型继承自 `managed` 类型 因此其所有基方法和字段在此类型中也可用

#### 定义

* **codepoint**: 字符的 Unicode 表示
* **kerning**: 两个字符之间的距离
* **glyph**: 字符的视觉表示

***

### 字段

#### height

* **只读**
* **类型**: `float`
* **描述**: 字体高度 以像素为单位

#### ascent

* **类型**: `float`
* **描述**: 字体上升值 以像素为单位

#### descent

* **类型**: `float`
* **描述**: 字体下降值 以像素为单位

#### line\_gap

* **类型**: `float`
* **描述**: 字体行间距 以像素为单位

#### kerning\_gap

* **类型**: `float`
* **描述**: 字体 kerning 间距 以像素为单位

#### outline\_alpha

* **类型**: `float`
* **描述**: 字体轮廓不透明度（0 到 1） 默认值为 0.45

#### flags

* **只读**
* **类型**: `font_flags`
* **描述**: 字体标志 使用 bit 库读取标志

#### y\_offset

* **类型**: `int`
* **描述**: 字形 Y 偏移量 以像素为单位 将改变图集中的字形位置 创建字体后更改此值将毫无意义

#### x\_offset

* **类型**: `int`
* **描述**: 字形 X 偏移量 以像素为单位 将改变图集中的字形位置 创建字体后更改此值将毫无意义

#### fallback\_font

* **类型**: `font_base`
* **描述**: 备用字体 如果在当前字体中找不到字形 将使用此备用字体 当一个字体没有特定符号的 codepoints 而另一个字体有 但您仍然希望优先使用此字体的字形时很有用

#### dropshadow\_color

* **类型**: `color`
* **描述**: 阴影颜色 仅使用 R G B 值

***

### 方法

#### get\_kerned\_char\_width

* **描述**: 返回字符宽度 包括 kerning
* **参数**:
  * `left`: `int` - 上一个字符的 codepoint
  * `right`: `int` - 当前字符的 codepoint
* **返回值**:
  * `float` - 距离 以像素为单位
* **示例**:

```lua
local w = font:get_kerned_char_width(prev_cp, cp)
```

#### get\_kerning

* **描述**: 返回单个字符的 kerning 值 如果禁用 kerning 将返回 kerning 间距
* **参数**:
  * `cp`: `int` - Codepoint
* **返回值**:
  * `float` - Kerning 值 以像素为单位
* **示例**:

```lua
local k = font:get_kerning(cp)
```

#### get\_text\_size

* **描述**: 返回文本区域大小
* **参数**:
  * `text`: `string` - 文本
  * `skip_scaling`: `bool` - 如果设置为 `true` 将跳过全局 DPI 缩放 默认为 `false`
  * `til_newline`: `bool` - 计算大小直到遇到换行符 默认为 `false`
* **返回值**:
  * `vec2` - 文本区域大小
* **示例**:

```lua
local sz = font:get_text_size('Hello!')
```

#### wrap\_text

* **描述**: 将文本包装以满足目标宽度 通过按单词断开文本并在之间插入换行符来实现 如果一个单词比目标宽度长 将使用该单词的宽度
* **参数**:
  * `text`: `string` - 要包装的文本
  * `width`: `float` - 目标宽度
* **返回值**:
  * `string` - 包装后的文本
* **示例**:

```lua
local shorter = font:wrap_text('This is some very long text!', 50)
```

#### get\_glyph

* **描述**: 返回字符的字形信息
* **参数**:
  * `codepoint`: `int` - Codepoint
* **返回值**:
  * `glyph_t` - 字形信息
* **示例**:

```lua
local glyph = font:get_glyph(cp)
```

#### get\_texture

* **描述**: 返回包含提供的字形的纹理图集
* **参数**:
  * `gl`: `glyph_t` - 字符字形
* **返回值**:
  * `int` - 纹理指针 或者如果未找到则为 `nil`
* **示例**:

```lua
local atlas = font:get_texture(glyph)
```

***

通过以上文档 您可以详细了解 `font_base` 类型及其相关字段和方法的功能和用法 希望这些信息对您有所帮助

***

苏黎世银云安全 ©
