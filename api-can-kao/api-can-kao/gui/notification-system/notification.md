---
description: 欢迎使用 Fatality
---

# Notification

最后修改时间

25 December 2024

### 简介

`notification` 类型表示一个通知项

***

### 构造函数

#### \_\_call

* **描述**: 构造通知
* **参数**:
  * `hdr`: `string` - 标题（标题）
  * `txt`: `string` - 文本（正文）
  * `ico`: `texture?` - 图标 默认为 `nil`
* **返回值**:
  * `notification` - 通知对象
* **示例**:

```lua
local notif = gui.notification('Hello', 'Lua works!')
```

***

苏黎世银云安全 ©
