---
description: 欢迎使用 Fatality
---

# Control

最后修改时间

25 December 2024

### 简介

`control` 类型表示一个抽象的 GUI 控件

***

### 字段

#### id

* **只读**
* **类型**: `int`
* **描述**: 控件 ID

#### id\_string

* **只读**
* **类型**: `string`
* **描述**: 控件 ID 的字符串表示 对于某些控件 可能为空

#### is\_visible

* **只读**
* **类型**: `bool`
* **描述**: 控件的可见性状态

#### parent

* **只读**
* **类型**: `control?`
* **描述**: 父控件 对于某些控件 可能为 `nil`

#### type

* **只读**
* **类型**: `control_type`
* **描述**: 控件的类型

#### inactive

* **类型**: `bool`
* **描述**: 如果设置为 `true` 将标记此控件为非活动状态

#### inactive\_text

* **类型**: `string`
* **描述**: 控件非活动时显示的工具提示文本 替代默认工具提示

#### inactive\_color

* **类型**: `color`
* **描述**: 非活动控件的标签颜色覆盖

#### tooltip

* **类型**: `string`
* **描述**: 工具提示文本

#### aliases

* **类型**: `table[string]`
* **描述**: 此控件的别名列表 用于搜索框支持不同命名（例如 用户搜索 "Double tap" 将找到 "Rapid fire"）

***

### 方法

#### get\_hotkey\_state

* **描述**: 返回控件的任何热键是否处于活动状态
* **参数**: 无
* **返回值**:
  * `bool` - 如果任何热键处于活动状态 返回 `true`
* **示例**:

```lua
if ctrl:get_hotkey_state() then
    -- ...
end
```

#### set\_visible

* **描述**: 更改控件的可见性状态
* **注意事项**: 对于位于包含大量其他控件的布局中的控件 调用此方法可能会由于自动堆叠导致性能问题
* **参数**:
  * `val`: `bool` - 可见性状态
* **返回值**: 无
* **示例**:

```lua
ctrl:set_visible(false)
```

#### add\_callback

* **描述**: 向控件添加回调
* **参数**:
  * `cbk`: `function` - 回调函数
* **返回值**: 无
* **示例**:

```lua
ctrl:add_callback(function ()
    print('Callback invoked!')
end)
```

#### cast

* **描述**: 尝试将控件向下转换为正确的类型
* **注意事项**: 由于 Lua 引擎的限制 无法自动向下转换变量 通常不需要调用此方法 除非找到某个控件尚未转换为所需类型 `find()` 方法会自动执行正确的类型转换
* **参数**: 无
* **返回值**:
  * `<control>` - 新类型 如果有
* **示例**:

```lua
local checkbox = maybe_checkbox:cast()
```

#### reset

* **描述**: 重置控件的状态 此操作通常在直接更改控件的 `value_param` 时需要
* **参数**: 无
* **返回值**: 无
* **示例**:

```lua
ctrl:reset()
```

***

苏黎世银云安全 ©
