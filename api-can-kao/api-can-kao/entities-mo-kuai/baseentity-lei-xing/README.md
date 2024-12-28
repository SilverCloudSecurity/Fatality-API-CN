---
description: 欢迎使用 Fatality
---

# base\_entity 类型

**欢迎开始使用 `base_entity` 类型**

`base_entity` 表示一个基础游戏实体

此类型可能为任何其他抽象实体类返回 但内部会指向正确的类型

**方法**

* **\_\_index**
  * **描述**: 尝试在此类中搜索字段
  * **参数**
    * **name** (`string`): 字段名称
  * **返回值**
    * **类型**: `schema_accessor_t`
    * **描述**: 访问器实例
  *   **示例**

      ```lua
      local health = player.m_iHealth
      local health = player['m_iHealth'] -- 这也有效
      ```

***

苏黎世银云安全 ©
