---
description: 欢迎使用 Fatality
---

# vec2 类型

#### `vec2` 类型文档

**欢迎开始使用 `vec2` 类型**

`vec2` 类型是渲染系统中使用的 2D 向量。

***

### 构造函数

#### \_\_call

**描述**: 创建一个新的 2D 向量实例。

**参数**

1. **默认向量 (0, 0)**
   * **类型**: 无
2. **单个值**
   * **名称**: value
   * **类型**: float
   * **描述**: X 和 Y 坐标
3. **XY 值**
   * **名称**: x
   * **类型**: float
   * **描述**: X 坐标
   * **名称**: y
   * **类型**: float
   * **描述**: Y 坐标

**返回值**

* **类型**: vec2
* **描述**: 新向量

**示例**

```lua
local vec = draw.vec2(5, 10)
```

***

### 字段

#### x

**类型**: float\
**描述**: X 坐标

#### y

**类型**: float\
**描述**: Y 坐标

***

### 方法

#### floor

**描述**: 返回取整后的向量变体。

**参数**: 无

**返回值**

* **类型**: vec2
* **描述**: 取整后的变体

**示例**

```lua
local fl = vec:floor()
```

#### ceil

**描述**: 返回向上取整后的向量变体。

**参数**: 无

**返回值**

* **类型**: vec2
* **描述**: 向上取整后的变体

**示例**

```lua
local ceiled = vec:ceil()
```

#### round

**描述**: 返回四舍五入后的向量变体。

**参数**: 无

**返回值**

* **类型**: vec2
* **描述**: 四舍五入后的变体

**示例**

```lua
local rounded = vec:round()
```

#### len

**描述**: 返回此向量的长度。

**参数**: 无

**返回值**

* **类型**: float
* **描述**: 长度

**示例**

```lua
local length = vec:len()
```

#### len\_sqr

**描述**: 返回此向量的平方长度。此方法实际上比非平方变体更快，如果需要额外性能请使用它。

**参数**: 无

**返回值**

* **类型**: float
* **描述**: 平方长度

**示例**

```lua
local squared_length = vec:len_sqr()
```

#### dist

**描述**: 返回到另一个向量的距离。

**参数**

* **名称**: other
* **类型**: vec2
* **描述**: 其他向量

**返回值**

* **类型**: float
* **描述**: 距离

**示例**

```lua
local distance = vec1:dist(vec2)
```

#### dist\_sqr

**描述**: 返回到另一个向量的平方距离。此方法实际上比非平方变体更快，如果需要额外性能请使用它。

**参数**

* **名称**: other
* **类型**: vec2
* **描述**: 其他向量

**返回值**

* **类型**: float
* **描述**: 平方距离

**示例**

```lua
local squared_distance = vec1:dist_sqr(vec2)
```

***

苏黎世银云安全 ©
