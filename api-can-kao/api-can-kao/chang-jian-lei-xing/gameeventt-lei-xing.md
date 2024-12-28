---
description: 欢迎开始使用 Fatality
---

# game\_event\_t 类型

<mark style="color:red;">`game_event_t`</mark> <mark style="color:red;"></mark><mark style="color:red;">类型描述了一个游戏事件</mark>

**方法 `get_name`**

**方法**

返回事件名称

**参数**

* **无参数**

**返回值**

* **类型**: string
* **描述**: 事件名称

**示例**

```lua
if event:get_name() == 'player_hurt' then
    -- ...
end
```

**方法 `get_bool`**

**方法**

通过键返回布尔值

**参数**

* **名称**: key
  * **类型**: string
  * **描述**: 条目键

**返回值**

* **类型**: bool
* **描述**: 条目值 如果找不到该键，则返回 `false`

**示例**

```lua
event:get_bool('some_key');
```

**方法 `get_int`**

**方法**

通过键返回整数值

**参数**

* **名称**: key
  * **类型**: string
  * **描述**: 条目键

**返回值**

* **类型**: int
* **描述**: 条目值。如果找不到该键，则返回 `0`

**示例**

```lua
event:get_int('some_key');
```

**方法 `get_float`**

**方法**

通过键返回浮点数值

**参数**

* **名称**: key
  * **类型**: string
  * **描述**: 条目键

**返回值**

* **类型**: float
* **描述**: 条目值。如果找不到该键，则返回 `0.0`

**示例**

```lua
event:get_float('some_key');
```

**方法 `get_string`**

**方法**

通过键返回字符串值

**参数**

* **名称**: key
  * **类型**: string
  * **描述**: 条目键

**返回值**

* **类型**: string
* **描述**: 条目值。如果找不到该键，则返回 `''`

**示例**

```lua
event:get_string('some_key');
```

**方法 `get_controller`**

**方法**

通过键返回控制器

**参数**

* **名称**: key
  * **类型**: string
  * **描述**: 条目键

**返回值**

* **类型**: cs2\_player\_controller
* **描述**: 控制器

**示例**

```lua
event:get_controller('userid');
```

**方法 `get_pawn_from_id`**

**方法**

通过键返回实体

**参数**

* **名称**: key
  * **类型**: string
  * **描述**: 条目键

**返回值**

* **类型**: cs2\_player\_pawn
* **描述**: 实体

**示例**

```lua
event:get_pawn_from_id('userid');
```

***

苏黎世银云安全 ©
