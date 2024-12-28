---
description: 欢迎开始使用 Fatality
---

# cengine\_client 类型

**欢迎开始使用 `cengine_client` 类型**

_<mark style="color:red;">`cengine_client`</mark> <mark style="color:red;"></mark><mark style="color:red;">实例提供了一种与 Source 2 的 Engine-to-Client 服务接口的方法。</mark>_

**方法**

* **get\_last\_timestamp**
  * **描述**: 返回最后的时间戳，以秒为单位。
  * **参数**: 无
  * **返回值**
    * **类型**: float
    * **描述**: 时间戳，以秒为单位。
  *   **示例**

      ```lua
      local last_time = game.engine:get_last_timestamp()
      ```
* **get\_last\_server\_tick**
  * **描述**: 返回最后的服务器 tick 编号。
  * **参数**: 无
  * **返回值**
    * **类型**: int
    * **描述**: 服务器 tick 编号。
  *   **示例**

      ```lua
      local server_tick = game.engine:get_last_server_tick()
      ```
* **in\_game**
  * **描述**: 返回客户端当前是否在游戏中。
  * **参数**: 无
  * **返回值**
    * **类型**: bool
    * **描述**: 游戏状态。
  *   **示例**

      ```lua
      if game.engine:in_game() then
          print("I'm in game!")
      end
      ```
* **is\_connected**
  * **描述**: 返回客户端当前是否连接到游戏服务器。
  * **参数**: 无
  * **返回值**
    * **类型**: bool
    * **描述**: 如果已连接则为 true。
  *   **示例**

      ```lua
      if game.engine:is_connected() then
          print("I'm connected!")
      end
      ```
* **get\_netchan**
  * **描述**: 返回用于网络通信的网络通道。
  * **参数**: 无
  * **返回值**
    * **类型**: cnet\_chan
    * **描述**: 网络通道，如果不存在则为 nil。
  *   **示例**

      ```lua
      local chan = game.engine:get_netchan()
      ```
* **client\_cmd**
  * **描述**: 执行客户端控制台命令。
  * **参数**
    * **cmd** (`string`): 要执行的命令。
    * **unrestricted** (`bool`): 是否保留任何限制，默认为 false。
  * **返回值**: 无
  *   **示例**

      ```lua
      game.engine:client_cmd('say Hello!')
      ```
* **get\_screen\_size**
  * **描述**: 返回客户端窗口屏幕尺寸。
  * **参数**: 无
  * **返回值**
    * **类型**: int
    * **描述**: 宽度。
    * **类型**: int
    * **描述**: 高度。
  *   **示例**

      ```lua
      local w, h = game.engine:get_screen_size()
      ```

***

苏黎世银云安全 ©
