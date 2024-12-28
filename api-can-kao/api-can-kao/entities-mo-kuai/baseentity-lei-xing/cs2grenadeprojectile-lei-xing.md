---
description: 欢迎使用 Fatality
---

# cs2\_grenade\_projectile 类型

**欢迎开始使用 `cs2_grenade_projectile` 类型**

_<mark style="color:red;">`cs2_grenade_projectile`</mark> <mark style="color:red;"></mark><mark style="color:red;">表示手榴弹投射物。此类型继承了</mark> <mark style="color:red;"></mark><mark style="color:red;">`base_entity`</mark> <mark style="color:red;"></mark><mark style="color:red;">类，所有基类的方法和字段在此类型中也有效</mark>_

**方法**

* **get\_abs\_origin**
  * **描述**: 返回绝对原点（用于渲染的原点）
  * **参数**: 无
  * **返回值**
    * **类型**: vector
    * **描述**: 原点
  *   **示例**

      ```lua
      local org = gren:get_abs_origin()
      ```
* **get\_grenade\_type**
  * **描述**: 返回手榴弹类型
  * **参数**: 无
  * **返回值**
    * **类型**: int
    * **描述**: 手榴弹类型
  *   **示例**

      ```lua
      local type = gren:get_grenade_type()
      ```

***

苏黎世银云安全  ©
