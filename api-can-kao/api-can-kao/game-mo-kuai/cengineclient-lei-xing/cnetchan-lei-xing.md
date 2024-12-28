---
description: 欢迎开始使用 Fatality
---

# cnet\_chan 类型

**欢迎开始使用`cnet_chan`类型**

`cnet_chan`提供了一种与网络通道类接口的方法

**方法**

* **get\_address**
  * **描述**:如果当前通道为null此函数返回nil
  * **返回值**
    * **类型**:string?
    * **描述**:远程机器的地址字符串IP地址或Steam服务器地址
  *   **示例**

      ```lua
      local chan=game.engine:get_netchan()
      if chan and not chan:is_null()then
          print(chan:get_address())
      end
      ```
* **is\_loopback**
  * **描述**:如果当前通道为null此函数返回nil
  * **返回值**
    * **类型**:bool?
    * **描述**:如果连接到本地机器则为true
  *   **示例**

      ```lua
      local chan=game.engine:get_netchan()
      if chan and not chan:is_null()and chan:is_loopback()then
          print('Connected to localhost!')
      end
      ```
* **is\_null**
  * **描述**:返回通道是否为空
  * **返回值**
    * **类型**:bool
    * **描述**:如果当前通道是虚拟通道则为true
  *   **示例**

      ```lua
      local chan=game.engine:get_netchan()
      if not chan or chan:is_null()then
          print('Not connected!')
      end
      ```
* **get\_latency**
  * **描述**:如果当前通道为null此函数返回nil
  * **返回值**
    * **类型**:float?
    * **描述**:到远程服务器的当前延迟以秒为单位
  *   **示例**

      ```lua
      local chan=game.engine:get_netchan()
      if chan and not chan:is_null()then
          print('Current latency:'..tostring(math.round(chan:get_latency()*1000.0))..'ms')
      end
      ```

***

苏黎世银云安全 ©
