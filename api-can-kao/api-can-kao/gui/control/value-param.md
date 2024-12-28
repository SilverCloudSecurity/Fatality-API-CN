---
description: 欢迎使用 Fatality
---

# Value Param

最后修改时间

25 December 2024

### 简介

`value_param` 类型表示某些控件类型使用的值数据

注意 这部分: `<type>` 用于指定此类型的实例所持有的确切类型 例如 当它说 `value_param<bool>` 时 意味着 `get` 将返回一个 `bool` 值 而 `set` 将仅接受 `bool` 类型作为其 `val` 参数

***

### 方法

#### get

* **描述**: 返回值
* **参数**: 无
* **返回值**:
  * `<type>` - 值
* **示例**:

```lua
ctrl:get_value():get()
```

#### set

* **描述**: 设置值
* **注意事项**: 建议使用控件的 `set_value` 方法 如果有的话
* **参数**:
  * `val`: `<type>` - 值
* **返回值**: 无
* **示例**:

```lua
ctrl:get_value():set(123)
```

#### get\_hotkey\_state

* **描述**: 返回是否有任何活动的热键
* **参数**: 无
* **返回值**:
  * `bool` - 如果有任何热键处于活动状态 返回 `true`
* **示例**:

```lua
if ctrl:get_value():get_hotkey_state() then
    -- ...
end
```

#### disable\_hotkeys

* **描述**: 禁用所有活动的热键 这允许您覆盖值
* **参数**: 无
* **返回值**: 无
* **示例**:

```lua
ctrl:get_value():disable_hotkeys()
```

***

苏黎世银云安全 ©
