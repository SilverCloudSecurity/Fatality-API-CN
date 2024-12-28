---
description: 欢迎开始使用 Fatality
---

# global\_vars\_t 类型

**欢迎开始使用`global_vars_t`类型**

_<mark style="color:red;">`global_vars_t`</mark><mark style="color:red;">实例提供了一种读取游戏中使用的多个全局变量的方法 更改任何值不受支持且将来也不会支持</mark>_

**字段**

* **real\_time**
  * **类型**:float
  * **描述**:自游戏启动以来经过的时间以秒为单位
* **frame\_count**
  * **类型**:int
  * **描述**:自游戏启动以来渲染的帧数
* **abs\_frame\_time**
  * **类型**:float
  * **描述**:绝对（平均）帧时间基于前几帧时间计算得出不应用于需要精确帧时间如动画的情况
* **max\_clients**
  * **类型**:int
  * **描述**:当前服务器上的最大客户端数量
* **ticks\_this\_frame**
  * **类型**:int
  * **描述**:在当前渲染帧期间经过的tick数超过1的任何值可能表示渲染过程中出现停滞
* **frame\_time**
  * **类型**:float
  * **描述**:上一帧渲染所需的时间可用于动画或其他需要精确帧时间的情况
* **cur\_time**
  * **类型**:float
  * **描述**:自服务器游戏启动以来经过的时间这不表示服务器上的准确时间尽管在某些事件中可能会由软件同步
* **tick\_fraction**
  * **类型**:float
  * **描述**:当前tick的小数值
* **tick\_count**
  * **类型**:int
  * **描述**:自服务器游戏启动以来经过的tick数
* **map\_path**
  * **类型**:string
  * **描述**:当前加载地图文件的相对路径
* **map\_name**
  * **类型**:string
  * **描述**:当前加载地图的名称

***

苏黎世银云安全 ©
