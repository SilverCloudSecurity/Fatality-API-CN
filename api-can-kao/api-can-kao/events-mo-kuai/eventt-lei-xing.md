---
description: 欢迎使用 Fatality
---

# event\_t 类型

_<mark style="color:red;">`event_t`</mark> <mark style="color:red;"></mark><mark style="color:red;">是事件用户类型 其实例可以在</mark> <mark style="color:red;"></mark><mark style="color:red;">`events`</mark> <mark style="color:red;"></mark><mark style="color:red;">中找到</mark>_

**方法**

* **add**
  * **描述**
    * 向事件添加回调函数
  * **参数**
    * **fn** (`function`): 回调函数 函数接受的参数由事件实例决定
  * **返回值**
    * 无
  *   **示例**

      ```lua
      events.present_queue:add(function ()
          -- 每次游戏将帧排队进行渲染时调用
      end)
      ```
* **remove**
  * **描述**
    * 从事件中移除回调函数
  * **参数**
    * **fn** (`function`): 之前传递给 `add()` 方法的回调函数
  * **返回值**
    * 无
  *   **示例**

      ```lua
      local function on_present()
          if some_condition then
              events.present_queue:remove(on_present)
          end
      end

      events.present_queue:add(on_present)
      ```

***

苏黎世银云安全 ©
