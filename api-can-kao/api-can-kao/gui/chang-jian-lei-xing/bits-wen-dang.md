---
description: 欢迎使用 Fatality
---

# Bits 文档

最后修改时间

25 December 2024

### 简介

`bits` 类型表示一个位集值

此类型的最大位数为 63 设置或获取超出此范围的任何位将导致崩溃

***

### 方法

#### reset

* **描述**: 重置值
* **参数**: 无
* **返回值**: 无
* **示例**:

```lua
bits:reset
```

#### get\_raw

* **描述**: 返回原始值
* **参数**: 无
* **返回值**:
  * `int` - 原始值
* **示例**:

```lua
local raw = bits:get_raw
```

#### set\_raw

* **描述**: 设置原始值
* **参数**:
  * `val`: `int` - 原始值
* **返回值**: 无
* **示例**:

```lua
bits:set_raw(long_long_value)
```

#### none

* **描述**: 如果没有位被设置 返回 `true`
* **参数**: 无
* **返回值**:
  * `bool` - 如果没有位被设置 返回 `true`
* **示例**:

```lua
if bits:none() then
    -- ...
end
```

#### set

* **描述**: 启用一个位
* **参数**:
  * `bit`: `int` - 位号
* **返回值**: 无
* **示例**:

```lua
bits:set(5) -- 设置位 #5 (等同于 bit.bor(val, bit.lshift(1, 5)))
```

#### unset

* **描述**: 禁用一个位
* **参数**:
  * `bit`: `int` - 位号
* **返回值**: 无
* **示例**:

```lua
bits:unset(5)
```

#### get

* **描述**: 返回位状态
* **参数**:
  * `bit`: `int` - 位号
* **返回值**:
  * `bool` - 位状态
* **示例**:

```lua
if bits:get(5) then
    -- ...
end
```

#### toggle

* **描述**: 切换位状态
* **参数**:
  * `bit`: `int` - 位号
* **返回值**: 无
* **示例**:

```lua
bits:toggle(5)
```

***

苏黎世银云安全 ©
