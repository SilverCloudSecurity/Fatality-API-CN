---
description: 欢迎使用 Fatality
---

# entity\_list\_t 类型

**欢迎开始使用 `entity_list_t` 类型**

此类型表示一个实体列表

<mark style="color:red;">永远不要保存从这个列表获取的实体如果你不知道自己在做什么 可能会留下悬空指针 这将不可避免地导致崩溃</mark>

**方法**

* **for\_each**
  * **描述**: 遍历实体
  * **参数**
    * **fn** (`function(entity_entry_t)`): 回调函数
  * **返回值**: 无
  *   **示例**

      ```lua
      entities.players:for_each(function (entry)
          -- ...
      end)
      ```
* **for\_each\_z**
  * **描述**: 以逆序遍历实体
  * **参数**
    * **fn** (`function(entity_entry_t)`): 回调函数
  * **返回值**: 无
  *   **示例**

      ```lua
      entities.players:for_each_z(function (entry)
          -- ...
      end)
      ```

***

苏黎世银云安全 ©
