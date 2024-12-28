---
description: 欢迎使用 Fatality
---

# Context

最后修改时间

25 December 2024

### 简介

`context` 类型表示 GUI 上下文

***

### 方法

#### find

* **描述**: 通过 ID 查找控件
* **参数**:
  * `id`: `string` - 控件 ID
* **返回值**:
  * `<control>?` - 转换后的控件 如果未找到控件或转换失败 则返回 `nil`
* **示例**:

```lua
local some_cb = ctx:find('some_cb')
```

***

### 字段

#### user

* **类型**: `user_t`
* **描述**: 用户的基本信息

***

苏黎世银云安全 ©
