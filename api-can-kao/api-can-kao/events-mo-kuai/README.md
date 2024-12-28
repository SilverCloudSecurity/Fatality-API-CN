---
description: 欢迎使用 Fatality
---

# events 模块

**梳理开始使用 `events` 模块**

_<mark style="color:red;">`events`</mark> <mark style="color:red;"></mark><mark style="color:red;">模块提供了多个事件供 API 使用 包括各种钩子和游戏内事件 每个事件条目是</mark> <mark style="color:red;"></mark><mark style="color:red;">`event_t`</mark> <mark style="color:red;"></mark><mark style="color:red;">对象 此表记录了脚本中使用的事件</mark>_

无需在脚本卸载时手动移除事件 API 引擎会自动处理

**事件**

* **present\_queue**
  * **描述**
    * 每次游戏将帧排队进行渲染时触发 这是唯一允许在屏幕上绘制的位置
  * **参数**
    * 无
* **frame\_stage\_notify**
  * **描述**
    * 每次游戏进入另一个帧阶段时触发 此事件在游戏处理新帧阶段之前调用
  * **参数**
    * **stage** (`client_frame_stage`): 当前帧阶段
* **render\_start\_pre**
  * **描述**
    * 每次游戏开始场景渲染过程时触发 此事件在游戏函数运行之前调用
  * **参数**
    * 无
* **render\_start\_post**
  * **描述**
    * 每次游戏开始场景渲染过程时触发 此事件在游戏函数运行之后调用
  * **参数**
    * **setup** (`cview_setup`): 视图设置信息
* **setup\_view\_pre**
  * **描述**
    * 每次游戏设置视图时触发 此事件在游戏函数运行之前调用
  * **参数**
    * 无
* **setup\_view\_post**
  * **描述**
    * 每次游戏设置视图信息时触发 此事件在游戏函数运行之后调用 可以从 `game.view_render` 服务获取视图信息
  * **参数**
    * 无
* **override\_view**
  * **描述**
    * 每次游戏内部覆盖视图信息时触发 可以自由修改提供的视图设置
  * **参数**
    * **setup** (`cview_setup`): 视图设置信息
* **event**
  * **描述**
    * 每次游戏事件触发时调用 并非监听所有游戏中的事件 如果需要未监听的事件 请使用 `mods.events`
  * **参数**
    * **event** (`game_event_t`): 游戏事件
* **handle\_input**
  * **描述**
    * 每次游戏处理鼠标或控制器输入时触发 是修改鼠标移动的好地方
  * **参数**
    * **type** (`input_type_t`): 输入类型
    * **value** (`ref_holder_t<float>`): 输入值

***

苏黎世银云安全 ©
