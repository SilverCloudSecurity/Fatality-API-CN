---
description: 欢迎使用 Fatality
---

# Layer

### 最后修改时间

25 December 2024

### 简介

`Layer` 是一种用于存储渲染命令、顶点和索引数据的类型。这是推送形状和控制渲染状态的唯一方式。

***

### 字段

#### g

* **只读**
* **类型**: `command`
* **描述**: 下一个要推送到队列的渲染命令。这是你想要更改的对象，例如设置纹理或更改渲染模式。

#### font

* **类型**: `font_base`
* **描述**: 与 `add_text` 一起使用的字体。如果未设置任何字体，则不会渲染文本。

#### tex\_sz

* **类型**: `vec2?`
* **描述**: 纹理尺寸。如果尝试渲染带纹理的圆角形状时需要此值，以便渲染系统正确映射 UV 坐标到渲染的形状。

#### skip\_dpi

* **类型**: `bool`
* **描述**: 如果设置为 `true`，将跳过全局 DPI 缩放。默认值为 `true`。

***

### 方法

#### add\_triangle\_filled

* **描述**: 添加单色填充三角形。
* **参数**: 无
* **返回值**: 无
* **示例**:

```lua
-- 示例代码
layer:add_triangle_filled(...)
```

#### add\_quad\_filled

* **描述**: 添加单色填充四边形。
* **参数**: 无
* **返回值**: 无
* **示例**:

```lua
-- 示例代码
layer:add_quad_filled(...)
```

#### add\_rect\_filled

* **描述**: 添加单色填充矩形。
* **参数**: 无
* **返回值**: 无
* **示例**:

```lua
-- 示例代码
layer:add_rect_filled(...)
```

#### add\_circle\_filled

* **描述**: 添加单色填充圆形。
* **参数**: 无
* **返回值**: 无
* **示例**:

```lua
-- 示例代码
layer:add_circle_filled(...)
```

#### add\_triangle\_filled\_multicolor

* **描述**: 添加多色填充三角形。
* **参数**: 无
* **返回值**: 无
* **示例**:

```lua
-- 示例代码
layer:add_triangle_filled_multicolor(...)
```

#### add\_rect\_filled\_multicolor

* **描述**: 添加多色填充矩形。
* **参数**: 无
* **返回值**: 无
* **示例**:

```lua
-- 示例代码
layer:add_rect_filled_multicolor(...)
```

#### add\_circle\_filled\_multicolor

* **描述**: 添加多色填充圆形。
* **参数**: 无
* **返回值**: 无
* **示例**:

```lua
-- 示例代码
layer:add_circle_filled_multicolor(...)
```

#### add\_quad\_filled\_multicolor

* **描述**: 添加多色填充四边形。
* **参数**: 无
* **返回值**: 无
* **示例**:

```lua
-- 示例代码
layer:add_quad_filled_multicolor(...)
```

#### add\_pill\_multicolor

* **描述**: 添加多色药丸形状。
* **参数**: 无
* **返回值**: 无
* **示例**:

```lua
-- 示例代码
layer:add_pill_multicolor(...)
```

#### add\_shadow\_line

* **描述**: 添加阴影线。
* **参数**: 无
* **返回值**: 无
* **示例**:

```lua
-- 示例代码
layer:add_shadow_line(...)
```

#### add\_shadow\_rect

* **描述**: 添加带阴影的矩形。
* **参数**: 无
* **返回值**: 无
* **示例**:

```lua
-- 示例代码
layer:add_shadow_rect(...)
```

#### add\_glow

* **描述**: 添加发光框。
* **参数**: 无
* **返回值**: 无
* **示例**:

```lua
-- 示例代码
layer:add_glow(...)
```

#### add\_rect\_filled\_rounded

* **描述**: 添加圆角填充矩形。
* **参数**: 无
* **返回值**: 无
* **示例**:

```lua
-- 示例代码
layer:add_rect_filled_rounded(...)
```

#### add\_rect\_filled\_rounded\_multicolor

* **描述**: 添加多色圆角填充矩形。
* **参数**: 无
* **返回值**: 无
* **示例**:

```lua
-- 示例代码
layer:add_rect_filled_rounded_multicolor(...)
```

#### add\_triangle

* **描述**: 添加描边三角形。
* **参数**: 无
* **返回值**: 无
* **示例**:

```lua
-- 示例代码
layer:add_triangle(...)
```

#### add\_quad

* **描述**: 添加描边四边形。
* **参数**: 无
* **返回值**: 无
* **示例**:

```lua
-- 示例代码
layer:add_quad(...)
```

#### add\_rect

* **描述**: 添加描边矩形。
* **参数**: 无
* **返回值**: 无
* **示例**:

```lua
-- 示例代码
layer:add_rect(...)
```

#### add\_circle

* **描述**: 添加描边圆形。
* **参数**: 无
* **返回值**: 无
* **示例**:

```lua
-- 示例代码
layer:add_circle(...)
```

#### add\_line

* **描述**: 添加线条。
* **参数**: 无
* **返回值**: 无
* **示例**:

```lua
-- 示例代码
layer:add_line(...)
```

#### add\_line\_multicolor

* **描述**: 添加多色线条。
* **参数**: 无
* **返回值**: 无
* **示例**:

```lua
-- 示例代码
layer:add_line_multicolor(...)
```

#### add\_rect\_rounded

* **描述**: 添加圆角填充矩形。
* **参数**: 无
* **返回值**: 无
* **示例**:

```lua
-- 示例代码
layer:add_rect_rounded(...)
```

#### add\_text

* **描述**: 添加文本。
* **提示**: 如果未设置字体，此函数将不执行任何操作。
* **参数**: 无
* **返回值**: 无
* **示例**:

```lua
-- 示例代码
layer:add_text(...)
```

#### override\_clip\_rect

* **描述**: 覆盖带有交集支持的裁剪矩形。
* **参数**: 无
* **返回值**: 无
* **示例**:

```lua
-- 示例代码
layer:override_clip_rect(...)
```

***

苏黎世银云安全 ©
