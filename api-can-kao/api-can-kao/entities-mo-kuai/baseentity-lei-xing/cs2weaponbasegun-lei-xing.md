---
description: 欢迎使用 Fatality
---

# cs2\_weapon\_base\_gun 类型

**欢迎开始使用 `cs2_weapon_base_gun` 类型**

<mark style="color:red;">`cs2_weapon_base_gun`</mark> <mark style="color:red;"></mark><mark style="color:red;">表示 CCSWeaponBaseGun 类 此类型继承了</mark> <mark style="color:red;"></mark><mark style="color:red;">`base_entity`</mark> <mark style="color:red;"></mark><mark style="color:red;">类 所有基类的方法和字段在此类型中也有效</mark>

**方法**

* **get\_abs\_origin**
  * **描述**: 返回绝对原点（用于渲染的原点）
  * **参数**: 无
  * **返回值**
    * **类型**: vector
    * **描述**: 原点
  *   **示例**

      ```lua
      local org=wep:get_abs_origin()
      ```
* **get\_max\_speed**
  * **描述**: 返回持有此武器时的最大玩家速度
  * **参数**: 无
  * **返回值**
    * **类型**: float
    * **描述**: 最大速度以UPS为单位
  *   **示例**

      ```lua
      local spd=wep:get_max_speed()
      ```
* **get\_inaccuracy**
  * **描述**: 返回当前不准确度值
  * **参数**
    * **mode** (`csweapon_mode`): 武器模式
  * **返回值**
    * **类型**: float
    * **描述**: 不准确度值
  *   **示例**

      ```lua
      local inacc=wep:get_inaccuracy(csweapon_mode.primary_mode)
      ```
* **get\_spread**
  * **描述**: 返回当前散布值
  * **参数**
    * **mode** (`csweapon_mode`): 武器模式
  * **返回值**
    * **类型**: float
    * **描述**: 散布值
  *   **示例**

      ```lua
      local spread=wep:get_spread(csweapon_mode.primary_mode)
      ```
* **get\_id**
  * **描述**: 返回武器ID
  * **参数**: 无
  * **返回值**
    * **类型**: weapon\_id
    * **描述**: 武器ID
  *   **示例**

      ```lua
      local wep_id=wep:get_id()
      ```
* **get\_type**
  * **描述**: 返回武器类型
  * **参数**: 无
  * **返回值**
    * **类型**: csweapon\_type
    * **描述**: 武器类型
  *   **示例**

      ```lua
      local type=wep:get_type()
      ```
* **get\_data**
  * **描述**: 返回武器静态数据
  * **参数**: 无
  * **返回值**
    * **类型**: ccsweapon\_base\_vdata
    * **描述**: 武器数据
  *   **示例**

      ```lua
      local data=wep:get_data()
      ```
* **is\_gun**
  * **描述**: 如果此武器是枪械则返回true
  * **参数**: 无
  * **返回值**
    * **类型**: bool
    * **描述**: 如果是枪械则为true
  *   **示例**

      ```lua
      if wep:is_gun()then
          -- ...
      end
      ```
* **is\_attackable**
  * **描述**: 如果可以使用此武器攻击则返回true
  * **参数**: 无
  * **返回值**
    * **类型**: bool
    * **描述**: 如果可以攻击则为true
  *   **示例**

      ```lua
      if wep:is_attackable()then
          -- ...
      end
      ```
* **has\_secondary\_attack**
  * **描述**: 如果此武器有次要攻击模式则返回true
  * **参数**: 无
  * **返回值**
    * **类型**: bool
    * **描述**: 如果有次要攻击模式则为true
  *   **示例**

      ```lua
      if wep:has_secondary_attack()then
          -- ...
      end
      ```
* **has\_spread**
  * **描述**: 如果此武器有散布（例如刀具没有散布）则返回true
  * **参数**: 无
  * **返回值**
    * **类型**: bool
    * **描述**: 如果有散布则为true
  *   **示例**

      ```lua
      if wep:has_spread()then
          -- ...
      end
      ```

***

苏黎世银云安全 ©
