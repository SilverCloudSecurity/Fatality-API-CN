---
description: 欢迎使用 Fatality
---

# schema\_accessor\_t 类型

_<mark style="color:red;">`schema_accessor_t`</mark> <mark style="color:red;"></mark><mark style="color:red;">表示一个特殊结构，用于引用实体对象中的某个字段</mark>_

你可以使用 `type()` 函数检查返回的类型

不要在事件范围之外存储此类型的实例，因为实体可能会被移除

**方法**

* **get**
  * **描述**: 返回字段的值
  * **参数**: 无
  * **返回值**
    * **类型**: `<type>`
    * **描述**: 字段的值
  *   **示例**

      ```lua
      local health = player.m_iHealth:get()
      ```
* **set**
  * **描述**: 设置字段的值
  * **参数**
    * **value** (`<type>`): 要设置的值
  * **返回值**: 无
  *   **示例**

      ```lua
      player.m_iHealth:set(50) -- 实际上不会对健康值产生影响
      ```

***

苏黎世银云安全 ©
