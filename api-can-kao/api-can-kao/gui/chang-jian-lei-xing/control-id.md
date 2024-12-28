---
description: 欢迎使用 Fatality
---

# Control ID

### 最后修改时间

25 December 2024

### 简介

`control_id` 类型表示一个控件 ID

***

### 构造函数

#### \_\_call

* **描述**: 构造 ID 结构
* **参数**:
  * `id`: `string` - ID
* **返回值**:
  * `control_id` - ID 结构
* **示例**:

```lua
lualocal id = gui.control_id('my_id')
```

***

### 字段

#### id

* **只读**
* **类型**: `int`
* **描述**: ID 的哈希表示

#### id\_string

* **只读**
* **类型**: `string`
* **描述**: ID 的正常表示

***

苏黎世银云安全 ©
