---
description: 欢迎使用 Fatality
---

# Math（数学）模块

<mark style="color:red;">`math`</mark> <mark style="color:red;"></mark><mark style="color:red;">模块扩展了 Lua 内置的</mark> <mark style="color:red;"></mark><mark style="color:red;">`math`</mark> <mark style="color:red;"></mark><mark style="color:red;">表 提供了额外的数学函数和工具</mark>

**函数**

* **calc\_angle**
  * **函数**
    * 计算两个向量之间的角度
  * **参数**
    * **src** (`vector`): 源向量
    * **dst** (`vector`): 目标向量
  * **返回值**
    * **类型**: `vector`
    * **描述**: 角度
  *   **示例**

      ```lua
      local ang = math.calc_angle(vec1 vec2)
      ```
* **angle\_normalize**
  * **函数**
    * 角度归一化
  * **参数**
    * **angle** (`float`): 输入角度
  * **返回值**
    * **类型**: `float`
    * **描述**: 归一化后的角度
  *   **示例**

      ```lua
      local norm = math.angle_normalize(560)
      ```
* **approach\_angles**
  * **函数**
    * 以一定速度接近目标角度
  * **参数**
    * **from** (`vector`): 起始角度
    * **to** (`vector`): 目标角度
    * **speed** (`float`): 接近速度
  * **返回值**
    * **类型**: `vector`
    * **描述**: 角度差
  *   **示例**

      ```lua
      local ang = math.approach_angles(from to 1.0 / game.global_vars.frametime)
      ```
* **edge\_point**
  * **函数**
    * 返回盒子边缘上的一个点
  * **参数**
    * **mins** (`vector`): 盒子最小值
    * **maxs** (`vector`): 盒子最大值
    * **dir** (`vector`): 点的方向（角度）
    * **radius** (`float`): 区域半径
  * **返回值**
    * **类型**: `vector`
    * **描述**: 点
  *   **示例**

      ```lua
      local point = math.edge_point(mins maxs dir 5)
      ```
* **lerp**
  * **函数**
    * 线性插值
  * **参数**
    * **t1** (`float`): 起始值
    * **t2** (`float`): 结束值
    * **progress** (`float`): 插值量
  * **返回值**
    * **类型**: `float`
    * **描述**: 插值后的值
  *   **示例**

      ```lua
      local mid = math.lerp(0 100 0.5)
      ```
* **vector\_angles**
  * **函数**
    * 从向量计算角度
  * **参数**
    * **forward** (`vector`): 源向量
    * **up** (`vector`): 上向量 默认为 `nil`
  * **返回值**
    * **类型**: `vector`
    * **描述**: 角度
  *   **示例**

      ```lua
      local ang = math.vector_angles(fw)
      ```
* **world\_to\_screen**
  * **函数**
    * 将世界中的一个点转换到视口
  * **参数**
    * **xyz** (`vector`): 世界中的点
    * **round** (`bool`): 是否四舍五入输出 默认为 `true`
  * **返回值**
    * **类型**: `vec2`
    * **描述**: 视口中的点
  *   **示例**

      ```lua
      local point = math.world_to_screen(game_point)
      ```
* **clamp**
  * **函数**
    * 将值限制在最小值和最大值之间
  * **参数**
    * **n** (`float`): 值
    * **lower** (`float`): 最小值
    * **upper** (`float`): 最大值
  * **返回值**
    * **类型**: `float`
    * **描述**: 限制后的值
  *   **示例**

      ```lua
      local x = math.clamp(50 5 25) -- 25
      ```
* **remap\_val**
  * **函数**
    * 将值从一个范围映射到另一个范围
  * **参数**
    * **val** (`float`): 值
    * **a** (`float`): 源范围的最小值
    * **b** (`float`): 源范围的最大值
    * **c** (`float`): 目标范围的最小值
    * **d** (`float`): 目标范围的最大值
  * **返回值**
    * **类型**: `float`
    * **描述**: 映射后的值
  *   **示例**

      ```lua
      local mapped = math.remap_val(0.5 0 1 0 100) -- 50
      ```
* **remap\_val\_clamped**
  * **函数**
    * 将值从一个范围映射到另一个范围 并基于源范围进行限制
  * **参数**
    * **val** (`float`): 值
    * **a** (`float`): 源范围的最小值
    * **b** (`float`): 源范围的最大值
    * **c** (`float`): 目标范围的最小值
    * **d** (`float`): 目标范围的最大值
  * **返回值**
    * **类型**: `float`
    * **描述**: 映射后的值
  *   **示例**

      ```lua
      local mapped = math.remap_val_clamped(5 0 1 0 100) -- 100
      ```
* **vec2**
  * **函数**
    * `draw.vec2()` 的别名
  *   **示例**

      ```lua
      local vec = math.vec2(5 5)
      ```
* **vec3**
  * **函数**
    * `vector()` 的别名
  *   **示例**

      ```lua
      local vec = math.vec3(5 12 5)
      ```

***

苏黎世银云安全 ©
