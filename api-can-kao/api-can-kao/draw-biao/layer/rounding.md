---
description: 欢迎使用 Fatality
---

# Rounding

### 最后修改时间

25 December 2024

### 简介

`Rounding` 枚举用于确定圆角形状的圆角模式

***

### 枚举值

#### tl

* **类型**: `Field`
* **描述**: 圆化左上角

#### tr

* **类型**: `Field`
* **描述**: 圆化右上角

#### bl

* **类型**: `Field`
* **描述**: 圆化左下角

#### br

* **类型**: `Field`
* **描述**: 圆化右下角

#### t

* **类型**: `Field`
* **描述**: 圆化顶部两个角。这与使用 `bit.bor(draw.rounding.tl, draw.rounding.tr)` 的结果相同

#### l

* **类型**: `Field`
* **描述**: 圆化左侧两个角。这与使用 `bit.bor(draw.rounding.tl, draw.rounding.bl)` 的结果相同

#### r

* **类型**: `Field`
* **描述**: 圆化右侧两个角。这与使用 `bit.bor(draw.rounding.tr, draw.rounding.br)` 的结果相同

#### b

* **类型**: `Field`
* **描述**: 圆化底部两个角。这与使用 `bit.bor(draw.rounding.bl, draw.rounding.br)` 的结果相同

#### all

* **类型**: `Field`
* **描述**: 圆化所有角。这与使用 `bit.bor(draw.rounding.tl, draw.rounding.tr, draw.rounding.bl, draw.rounding.br)` 的结果相同

***

### 示例用法

```lua
-- 圆化左上角
shape:set_rounding(draw.rounding.tl)

-- 圆化右上角
shape:set_rounding(draw.rounding.tr)

-- 圆化左下角
shape:set_rounding(draw.rounding.bl)

-- 圆化右下角
shape:set_rounding(draw.rounding.br)

-- 圆化顶部两个角
shape:set_rounding(draw.rounding.t)

-- 圆化左侧两个角
shape:set_rounding(draw.rounding.l)

-- 圆化右侧两个角
shape:set_rounding(draw.rounding.r)

-- 圆化底部两个角
shape:set_rounding(draw.rounding.b)

-- 圆化所有角
shape:set_rounding(draw.rounding.all)
```

***

通过以上文档 您可以详细了解 `Rounding` 枚举及其相关字段的功能和用法 希望这些信息对您有所帮助

***

苏黎世银云安全 ©
