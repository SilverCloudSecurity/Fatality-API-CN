---
description: 欢迎使用 Fatality
---

# Glow Parts

最后修改时间

25 December 2024

### 简介

`glow_parts` 枚举用于确定形状周围发光效果的哪些部分应该被渲染

***

### 枚举值

#### tl

* **类型**: `Field`
* **描述**: 绘制左上角

#### tr

* **类型**: `Field`
* **描述**: 绘制右上角

#### bl

* **类型**: `Field`
* **描述**: 绘制左下角

#### br

* **类型**: `Field`
* **描述**: 绘制右下角

#### t

* **类型**: `Field`
* **描述**: 绘制顶部线条

#### l

* **类型**: `Field`
* **描述**: 绘制左侧线条

#### r

* **类型**: `Field`
* **描述**: 绘制右侧线条

#### b

* **类型**: `Field`
* **描述**: 绘制底部线条

#### all\_left

* **类型**: `Field`
* **描述**: 绘制所有左侧形状 包括左上角和左下角以及左侧线条

#### all\_right

* **类型**: `Field`
* **描述**: 绘制所有右侧形状 包括右上角和右下角以及右侧线条

#### all\_top

* **类型**: `Field`
* **描述**: 绘制所有顶部形状 包括左上角和右上角以及顶部线条

#### all\_bottom

* **类型**: `Field`
* **描述**: 绘制所有底部形状 包括左下角和右下角以及底部线条

#### all

* **类型**: `Field`
* **描述**: 绘制整个形状周围的发光效果

#### no\_bottom

* **类型**: `Field`
* **描述**: 绘制发光效果但不包括底部线条

#### no\_top

* **类型**: `Field`
* **描述**: 绘制发光效果但不包括顶部线条

#### no\_right

* **类型**: `Field`
* **描述**: 绘制发光效果但不包括右侧线条

#### no\_left

* **类型**: `Field`
* **描述**: 绘制发光效果但不包括左侧线条

***

### 示例用法

```lua
-- 绘制左上角
shape:set_glow_parts(glow_parts.tl)

-- 绘制右上角
shape:set_glow_parts(glow_parts.tr)

-- 绘制左下角
shape:set_glow_parts(glow_parts.bl)

-- 绘制右下角
shape:set_glow_parts(glow_parts.br)

-- 绘制顶部线条
shape:set_glow_parts(glow_parts.t)

-- 绘制左侧线条
shape:set_glow_parts(glow_parts.l)

-- 绘制右侧线条
shape:set_glow_parts(glow_parts.r)

-- 绘制底部线条
shape:set_glow_parts(glow_parts.b)

-- 绘制所有左侧形状
shape:set_glow_parts(glow_parts.all_left)

-- 绘制所有右侧形状
shape:set_glow_parts(glow_parts.all_right)

-- 绘制所有顶部形状
shape:set_glow_parts(glow_parts.all_top)

-- 绘制所有底部形状
shape:set_glow_parts(glow_parts.all_bottom)

-- 绘制整个发光效果
shape:set_glow_parts(glow_parts.all)

-- 绘制发光效果但不包括底部线条
shape:set_glow_parts(glow_parts.no_bottom)

-- 绘制发光效果但不包括顶部线条
shape:set_glow_parts(glow_parts.no_top)

-- 绘制发光效果但不包括右侧线条
shape:set_glow_parts(glow_parts.no_right)

-- 绘制发光效果但不包括左侧线条
shape:set_glow_parts(glow_parts.no_left)
```

***

苏黎世银云安全 ©
