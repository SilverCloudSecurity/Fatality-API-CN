---
description: 欢迎使用 Fatality
---

# Checkbox

最后修改时间

25 December 2024

### 简介

`checkbox` 类型表示一个复选框控件

此类型继承自 `control` 类型 因此其所有基方法和字段在此类型中也可用

***

### 构造函数

#### \_\_call

* **描述**: 构造复选框
* **参数**:
  * `id`: `control_id` - ID
* **返回值**:
  * `checkbox` - 复选框实例
* **示例**:

```lua
local cb = gui.checkbox(gui.control_id('my_id'))
```

***

### 方法

#### get\_value

* **描述**: 返回复选框的值
* **参数**: 无
* **返回值**:
  * `value_param<bool>` - 值数据
* **示例**:

```lua
local val = cb:get_value():get()
```

#### set\_value

* **描述**: 设置复选框的值
* **注意事项**: 建议使用此方法而不是 `value_param` 的 `set` 方法
* **参数**:
  * `val`: `bool` - 新值
* **返回值**: 无
* **示例**:

```lua
cb:set_value(true)
```

***

苏黎世银云安全 ©
