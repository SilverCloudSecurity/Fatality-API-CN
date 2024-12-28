---
description: 欢迎使用 Fatality
---

# events\_t 模块

`events_t`模块让你管理自定义游戏内事件监听器

_<mark style="color:red;">请注意游戏服务器知道你在监听哪些事件 内部我们只监听无论如何都会发送给客户端的事件 如果你决定监听服务器不期望的事件 可能在官方服务器上引起问题</mark>_

**方法**

* **add\_listener**
  * **描述**:添加游戏事件到监听器
  * **注意**:内部我们监听以下事件 添加这些事件到监听器是不必要的
    * player\_hurt
    * item\_purchase
    * bullet\_impact
    * weapon\_fire
    * bomb\_beginplant
    * bomb\_abortplant
    * bomb\_planted
    * bomb\_defused
    * bomb\_exploded
    * round\_start
    * game\_newmap
    * map\_shutdown
  * **参数**
    * **name**(`string`):事件名称
  * **返回值**:无
  *   **示例**

      ```lua
      mods.events:add_listener('round_end')
      ```

***

苏黎世银云安全 ©
