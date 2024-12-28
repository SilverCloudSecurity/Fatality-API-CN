---
description: 欢迎使用 Fatality
---

# cs2\_player\_controller 类型

**欢迎开始使用 `cs2_player_controller` 类型**

_<mark style="color:red;">`cs2_player_controller`</mark> <mark style="color:red;"></mark><mark style="color:red;">表示 CCSPlayerController 类。此类型继承了</mark> <mark style="color:red;"></mark><mark style="color:red;">`base_entity`</mark> <mark style="color:red;"></mark><mark style="color:red;">类，所有基类的方法和字段在此类型中也有效。</mark>_

**方法**

* **is\_enemy**
  * **描述**: 如果此玩家是本地玩家的敌人，则返回 true
  * **参数**: 无
  * **返回值**
    * **类型**: bool
    * **描述**: 如果是敌人则为 true
  *   **示例**

      ```lua
      if player:is_enemy() then
          -- ...
      end
      ```
* **get\_name**
  * **描述**: 返回经过清理的玩家名称
  * **参数**: 无
  * **返回值**
    * **类型**: string
    * **描述**: 玩家名称
  *   **示例**

      ```lua
      local name = player:get_name()
      ```
* **get\_pawn**
  * **描述**: 返回与此控制器关联的 Pawn
  * **参数**: 无
  * **返回值**
    * **类型**: cs2\_player\_pawn
    * **描述**: Pawn 实例
  *   **示例**

      ```lua
      local pawn = ctrl:get_pawn()
      ```
* **get\_active\_weapon**
  * **描述**: 返回当前激活的武器
  * **参数**: 无
  * **返回值**
    * **类型**: cs2\_weapon\_base\_gun
    * **描述**: 武器实例。
  *   **示例**

      ```lua
      local wep = player:get_active_weapon()
      ```
* **get\_observer\_pawn**
  * **描述**: 返回此控制器使用的观察者 Pawn
  * **参数**: 无
  * **返回值**
    * **类型**: base\_entity
    * **描述**: 实体
  *   **示例**

      ```lua
      local obs_pawn = ctrl:get_observer_pawn()
      ```
* **get\_observer\_target**
  * **描述**: 返回此控制器当前正在观察的 Pawn
  * **参数**: 无
  * **返回值**
    * **类型**: base\_entity
    * **描述**: 实体
  *   **示例**

      ```lua
      local obs = ctrl:get_observer_target()
      ```
* **get\_observer\_mode**
  * **描述**: 返回当前的观察者模式
  * **参数**: 无
  * **返回值**
    * **类型**: observer\_mode\_t
    * **描述**: 观察者模式。
  *   **示例**

      ```lua
      local mode = ctrl:get_observer_mode()
      ```

***

苏黎世银云安全 ©
