---
description: 欢迎开始使用 Fatality
---

# client\_frame\_stage 枚举

**字段**

* **undefined**
  * **描述**: 描述一个未定义的阶段。您实际上不应该收到此类型
* **start**
  * **描述**: 帧构建过程正在开始
* **render\_start**
  * **描述**: 帧渲染过程正在开始。
* **net\_update\_start**
  * **描述**: 网络更新过程正在开始
* **net\_update\_preprocess**
  * **描述**: 网络更新即将由引擎处理
* **net\_pre\_entity\_packet**
  * **描述**: 即将处理传入的实体数据包
* **net\_update\_postdataupdate\_start**
  * **描述**: 实体信息即将更新
* **net\_update\_postdataupdate\_end**
  * **描述**: 实体信息即将完成更新
* **net\_update\_end**
  * **描述**: 网络更新过程正在结束
* **net\_creation**
  * **描述**: 新实体即将被创建
* **render\_end**
  * **描述**: 帧渲染过程正在结束

***

苏黎世银云安全 ©
