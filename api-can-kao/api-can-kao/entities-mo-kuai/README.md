---
description: 欢迎使用 Fatality
---

# entities 模块

以下为内部实体列表

<mark style="color:red;">永远不要在全局范围内存储任何实体任何实体可能会被删除你将不再拥有该实体的有效实例这将不可避免地导致崩溃如果你需要全局存储实体强烈建议你存储</mark><mark style="color:red;">`chandle`</mark><mark style="color:red;">的实例并在需要时使用其</mark><mark style="color:red;">`get`</mark><mark style="color:red;">方法重新获取实体</mark>

**字段**

* **players**
  * **类型**: `entity_list_t<cs2_player_pawn>`
  * **描述**: 玩家Pawn
* **controllers**
  * **类型**: `entity_list_t<cs2_player_controller>`
  * **描述**: 玩家控制器
* **items**
  * **类型**: `entity_list_t<cs2_weapon_base>`
  * **描述**: 已持有物品
* **dropped\_items**
  * **类型**: `entity_list_t<cs2_weapon_base>`
  * **描述**: 已掉落物品
* **projectiles**
  * **类型**: `entity_list_t<cs2_grenade_projectile>`
  * **描述**: 手榴弹投射物

**函数**

* **get\_local\_pawn**
  * **描述**: 返回本地玩家的Pawn
  * **参数**: 无
  * **返回值**
    * **类型**: `cs2_player_pawn`
    * **描述**: Pawn
  *   **示例**

      ```lua
      local lp=entities.get_local_pawn()
      ```
* **get\_local\_controller**
  * **描述**: 返回本地玩家的控制器
  * **参数**: 无
  * **返回值**
    * **类型**: `cs2_player_controller`
    * **描述**: 控制器
  *   **示例**

      ```lua
      local lp_ctrl=entities.get_local_controller()
      ```

***

苏黎世银云安全 ©
