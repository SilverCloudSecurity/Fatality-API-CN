---
description: 欢迎使用 Fatality
---

# chandle 类型

**欢迎开始使用 `chandle` 类型**

_<mark style="color:red;">`chandle`</mark> <mark style="color:red;"></mark><mark style="color:red;">表示实体句柄 可以使用</mark> <mark style="color:red;"></mark><mark style="color:red;">`==`</mark> <mark style="color:red;"></mark><mark style="color:red;">运算符比较此类型</mark>_

**方法**

* **get**
  * **描述**: 返回实体 如果未找到则返回 nil
  * **参数**: 无
  * **返回值**
    * **类型**: `<type>`
    * **描述**: 实体实例
  *   **示例**

      ```lua
      local ent = handle:get()
      ```
* **valid**
  * **描述**: 如果句柄有效则返回 true
  * **参数**: 无
  * **返回值**
    * **类型**: bool
    * **描述**: 如果有效则为 true
  *   **示例**

      ```lua
      if handle:valid() then
          -- ...
      end
      ```
* **is\_clientside**
  * **描述**: 如果句柄链接到客户端实体则返回 true
  * **参数**: 无
  * **返回值**
    * **类型**: bool
    * **描述**: 如果是客户端实体则为 true
  *   **示例**

      ```lua
      if handle:is_clientside() then
          -- ...
      end
      ```

***

苏黎世银云安全 ©
