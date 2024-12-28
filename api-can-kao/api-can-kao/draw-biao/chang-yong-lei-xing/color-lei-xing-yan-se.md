---
description: 欢迎使用 Fatality
---

# color 类型（颜色）

颜色类型

_<mark style="color:red;">这是一种在渲染系统中使用的颜色类型 不要将此类型与游戏中使用的颜色混淆 虽然这些类型在内部是可互换的 但在API中它们并不相同</mark>_

**构造函数**

**`__call`**

创建一个新的颜色实例

**参数**

1. 默认颜色（半透明黑色）
   * 无参数
2. 整数颜色
   * `r` int 红色（0 到 255）
   * `g` int 绿色（0 到 255）
   * `b` int 蓝色（0 到 255）
   * `a` int 不透明度（0 到 255）默认为255
3. 十六进制字符串
   * `hex` string 十六进制字符串 格式为 #rrggbbaa #rrggbb #rgba 和 #rgb

**返回值**

* `color` 颜色对象

**示例**

```lua
local white = draw.color(255, 255, 255)
```

**函数**

**`white`**

返回一个不透明的白色

**参数**

* 无参数

**返回值**

* `color` 颜色对象

**示例**

```lua
local white = draw.color.white()
```

**`white_transparent`**

返回一个透明的白色

**参数**

* 无参数

**返回值**

* `color` 颜色对象

**示例**

```lua
local white_t = draw.color.white_transparent()
```

**`black`**

返回一个不透明的黑色

**参数**

* 无参数

**返回值**

* `color` 颜色对象

**示例**

```lua
local black = draw.color.black()
```

**`black_transparent`**

返回一个透明的黑色

**参数**

* 无参数

**返回值**

* `color` 颜色对象

**示例**

```lua
local black_t = draw.color.black_transparent()
```

**`percent`**

返回一个从红色到绿色的颜色 根据提供的百分比

**参数**

* `p` float 百分比（0 到 1）
* `a` float 不透明度 默认为1

**返回值**

* `color` 颜色对象

**示例**

```lua
local yellow = draw.color.percent(0.5)
```

**`gray`**

返回一个从黑色到白色的颜色 根据提供的百分比

**参数**

* `b` float 百分比（0 到 1）
* `a` float 不透明度 默认为1

**返回值**

* `color` 颜色对象

**示例**

```lua
local gray = draw.color.gray(0.5)
```

**`interpolate`**

插值两个颜色

**参数**

* `a` color 起始颜色
* `b` color 结束颜色
* `t` float 插值百分比

**返回值**

* `color` 颜色对象

**示例**

```lua
local a = draw.color.white()
local b = draw.color.black()
local i = draw.color.interpolate(a, b, 0.5) -- 灰色
```

**方法**

**`rgba`**

返回此颜色的整数表示（RGBA格式）

**参数**

* 无参数

**返回值**

* `int` RGBA颜色

**示例**

```lua
local num = col:rgba()
```

**`argb`**

返回此颜色的整数表示（ARGB格式）

**参数**

* 无参数

**返回值**

* `int` ARGB颜色

**示例**

```lua
local num = col:argb()
```

**`bgra`**

返回此颜色的整数表示（BGRA格式）

**参数**

* 无参数

**返回值**

* `int` BGRA颜色

**示例**

```lua
local num = col:bgra()
```

**`abgr`**

返回此颜色的整数表示（ABGR格式）

**参数**

* 无参数

**返回值**

* `int` ABGR颜色

**示例**

```lua
local num = col:abgr()
```

**`darken`**

返回此颜色的更暗的变体

**参数**

* `value` float 调制量（0 到 1）

**返回值**

* `color` 更暗的颜色

**示例**

```lua
local darker = col:darken(0.5)
```

**`mod_a`**

调制颜色的不透明度 这将取现有不透明度 并乘以你提供的值 如果你想要逐步调制相同的颜色而不是设置确切的不透明度数值 这很有用

**参数**

1. 浮点数变体
   * `value` float 不透明度调制（0 到 1）
2. 整数变体
   * `value` int 不透明度调制（0 到 255）

**返回值**

* `color` 调制后的颜色

**示例**

```lua
local half_opacity = col:mod_a(0.5)
```

**`r`**

覆盖红色并返回新颜色

**参数**

* `value` float 新值

**返回值**

* `color` 新颜色

**示例**

```lua
local full_red = col:r(1)
```

**`g`**

覆盖绿色并返回新颜色

**参数**

* `value` float 新值

**返回值**

* `color` 新颜色

**示例**

```lua
local full_green = col:g(1)
```

**`b`**

覆盖蓝色并返回新颜色

**参数**

* `value` float 新值

**返回值**

* `color` 新颜色

**示例**

```lua
local full_blue = col:b(1)
```

**`a`**

覆盖不透明度并返回新颜色

**参数**

* `value` float 新值

**返回值**

* `color` 新颜色

**示例**

```lua
local full_opacity = col:a(1)
```

**`get_r`**

返回红色颜色值

**参数**

* 无参数

**返回值**

* `int` 颜色值

**示例**

```lua
local r = col:get_r()
```

**`get_g`**

返回绿色颜色值

**参数**

* 无参数

**返回值**

* `int` 颜色值

**示例**

```lua
local g = col:get_g()
```

**`get_b`**

返回蓝色颜色值

**参数**

* 无参数

**返回值**

* `int` 颜色值

**示例**

```lua
local b = col:get_b()
```

**`get_a`**

返回不透明度颜色值

**参数**

* 无参数

**返回值**

* `int` 颜色值

**示例**

```lua
local a = col:get_a()
```

**`h`**

返回颜色的色调值

**参数**

* 无参数

**返回值**

* `int` 色调（0 到 359）

**示例**

```lua
local hue = col:h()
```

**`s`**

返回颜色的饱和度值

**参数**

* 无参数

**返回值**

* `float` 饱和度（0 到 1）

**示例**

```lua
local saturation = col:s()
```

**`v`**

返回颜色的亮度值

**参数**

* 无参数

**返回值**

* `float` 亮度（0 到 1）

**示例**

```lua
local brightness = col:v()
```

**`hsv`**

根据提供的HSB值构造新的颜色

**参数**

* `hue` int 色调（0 到 359）
* `saturation` float 饱和度（0 到 1）
* `brightness` float 亮度（0 到 1）
* `alpha` float 覆盖源颜色的不透明度 必须省略 或提供0 到1的值

**返回值**

* `color` 新颜色

**示例**

```lua
local new_col = col:hsv(250, 0.5, 0.1)
```

***

苏黎世银云安全 ©
