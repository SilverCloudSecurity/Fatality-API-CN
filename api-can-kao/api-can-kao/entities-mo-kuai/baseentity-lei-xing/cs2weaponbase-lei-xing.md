---
description: 欢迎使用 Fatality
---

# cs2\_weapon\_base 类型

**欢迎开始使用`cs2_weapon_base`类型**

_<mark style="color:red;">`cs2_weapon_base`</mark><mark style="color:red;">表示CCSWeaponBase实体 此类型继承了</mark><mark style="color:red;">`base_entity`</mark><mark style="color:red;">类型 所有基类的方法和字段在此类型中也有效</mark>_

**方法**

* **get\_abs\_origin**
  * **描述**:返回绝对原点（用于渲染的原点）
  * **参数**:无
  * **返回值**
    * **类型**:vector
    * **描述**:原点
  *   **示例**

      ```lua
      local org=wep:get_abs_origin()
      ```
* **get\_id**
  * **描述**:返回武器ID
  * **参数**:无
  * **返回值**
    * **类型**:weapon\_id
    * **描述**:武器ID
  *   **示例**

      ```lua
      local wep_id=wep:get_id()
      ```
* **get\_type**
  * **描述**:返回武器类型
  * **参数**:无
  * **返回值**
    * **类型**:csweapon\_type
    * **描述**:武器类型
  *   **示例**

      ```lua
      local type=wep:get_type()
      ```
* **get\_data**
  * **描述**:返回武器静态数据
  * **参数**:无
  * **返回值**
    * **类型**:ccsweapon\_base\_vdata
    * **描述**:武器数据
  *   **示例**

      ```lua
      local data=wep:get_data()
      ```

***

苏黎世银云安全  ©
