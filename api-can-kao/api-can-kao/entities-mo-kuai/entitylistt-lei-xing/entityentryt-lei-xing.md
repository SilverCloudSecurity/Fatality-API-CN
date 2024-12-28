---
description: 欢迎使用 Fatality
---

# entity\_entry\_t 类型

**欢迎开始使用 `entity_entry_t` 类型**

_<mark style="color:red;">`entity_entry_t`</mark> <mark style="color:red;"></mark><mark style="color:red;">表示一个实体条目。</mark>_

**字段**

* **entity**
  * **类型**: `<type>`
  * **描述**: 实体实例。类型取决于你从哪个列表获取它。
* **had\_dataupdate**
  * **类型**: `bool`
  * **描述**: 如果客户端至少一次接收到该实体的更新，则为 `true`。
* **handle**
  * **类型**: `chandle<type>`
  * **描述**: 实体的句柄。如果你需要全局访问实体，可以将此句柄存储在其他地方。
* **avatar**
  * **类型**: `texture`
  * **描述**: 仅在使用 `cs2_player_controller` 类型的条目中可用。玩家的个人资料图片。如果尚未初始化，则为 `nil`。

***

苏黎世银云安全 ©
