---
description: 欢迎开始使用 Fatality
---

# vector 类型

<mark style="color:red;">`vector`</mark> <mark style="color:red;"></mark><mark style="color:red;">类型是一个常见的 3D 向量（x, y, z）</mark>

此类型支持以下操作：`+`, `-`, `/`, `*` 和 `==`

**字段**

* **x**
  * **类型**: float
  * **描述**: X 坐标。
* **y**
  * **类型**: float
  * **描述**: Y 坐标。
* **z**
  * **类型**: float
  * **描述**: Z 坐标。

**构造函数 `__call`**

**构造函数**

构造一个向量。

**参数**

1. **默认向量 (0, 0, 0)**
   * **无参数**。
2. **单个值**
   * **名称**: value
   * **类型**: float
   * **描述**: X 和 Y 坐标。
3. **XYZ 值**
   * **名称**: x
     * **类型**: float
     * **描述**: X 坐标。
   * **名称**: y
     * **类型**: float
     * **描述**: Y 坐标。
   * **名称**: z
     * **类型**: float
     * **描述**: Z 坐标。

**返回值**

* **类型**: vector
* **描述**: 向量。

**示例**

```lua
local vec = vector(5, 25, 12);
```

**方法 `is_zero`**

**方法**

如果此向量在容差范围内，则返回 `true`。

**参数**

* **名称**: tolerance
  * **类型**: float
  * **描述**: 允许的最大容差。默认为 0.01。

**返回值**

* **类型**: bool
* **描述**: 如果所有值在 -tolerance 和 tolerance 范围内，则返回 `true`。

**示例**

```lua
local vec = vector(0, 0.1, 0.5);
print(tostring(vec:is_zero(1))); -- 将打印 'true'，因为每个值都在 -1 和 1 的范围内
```

**方法 `dist`**

**方法**

返回到另一个向量的距离。

**参数**

* **名称**: other
  * **类型**: vector
  * **描述**: 要计算距离的向量。

**返回值**

* **类型**: float
* **描述**: 到另一个向量的距离。

**示例**

```lua
local vec1 = vector(0, 0, 0);
local vec2 = vector(1, 1, 5);
print(tostring(vec1:dist(vec2)));
```

**方法 `dist_sqr`**

**方法**

返回到另一个向量的平方距离。

此方法在性能上比非平方变体更快。如果需要额外性能，请使用此方法。

**参数**

* **名称**: other
  * **类型**: vector
  * **描述**: 要计算距离的向量。

**返回值**

* **类型**: float
* **描述**: 到另一个向量的平方距离。

**示例**

```lua
local vec1 = vector(0, 0, 0);
local vec2 = vector(1, 1, 5);
print(tostring(vec1:dist_sqr(vec2)));
```

**方法 `dist_2d`**

**方法**

返回到另一个向量的 2D 距离（仅使用 x 和 y 值）。

**参数**

* **名称**: other
  * **类型**: vector
  * **描述**: 要计算距离的向量。

**返回值**

* **类型**: float
* **描述**: 到另一个向量的距离。

**示例**

```lua
local vec1 = vector(0, 0, 0);
local vec2 = vector(1, 1, 5);
print(tostring(vec1:dist_2d(vec2)));
```

**方法 `dist_2d_sqr`**

**方法**

返回到另一个向量的 2D 平方距离（仅使用 x 和 y 值）。

此方法在性能上比非平方变体更快。如果需要额外性能，请使用此方法。

**参数**

* **名称**: other
  * **类型**: vector
  * **描述**: 要计算距离的向量。

**返回值**

* **类型**: float
* **描述**: 到另一个向量的平方距离。

**示例**

```lua
local vec1 = vector(0, 0, 0);
local vec2 = vector(1, 1, 5);
print(tostring(vec1:dist_2d_sqr(vec2)));
```

**方法 `cross`**

**方法**

返回与另一个向量的叉积。

**参数**

* **名称**: other
  * **类型**: vector
  * **描述**: 要计算叉积的向量。

**返回值**

* **类型**: vector
* **描述**: 叉积。

**示例**

```lua
local vec1 = vector(0, 0, 0);
local vec2 = vector(1, 1, 5);
local cross = vec1:cross(vec2);
```

**方法 `is_valid`**

**方法**

如果此向量中的所有值都是有限的，则返回 `true`。

**参数**

* **无参数**。

**返回值**

* **类型**: bool
* **描述**: 如果值是有限的，则返回 `true`。

**示例**

```lua
local vec = vector(5, 1, 6);
if vec:is_valid() then
    -- ...
end
```

**方法 `length`**

**方法**

返回此向量的长度。

**参数**

* **无参数**。

**返回值**

* **类型**: float
* **描述**: 此向量的长度。

**示例**

```lua
local vec = vector(5, 1, 6);
local length = vec:length();
```

**方法 `length_sqr`**

**方法**

返回此向量的平方长度。

此方法在性能上比非平方变体更快。如果需要额外性能，请使用此方法。

**参数**

* **无参数**。

**返回值**

* **类型**: float
* **描述**: 此向量的长度。

**示例**

```lua
local vec = vector(5, 1, 6);
local length = vec:length_sqr();
```

**方法 `length_2d`**

**方法**

返回此向量的 2D 长度。

**参数**

* **无参数**。

**返回值**

* **类型**: float
* **描述**: 此向量的长度。

**示例**

```lua
local vec = vector(5, 1, 6);
local length = vec:length_2d();
```



**方法 `length_2d_sqr`**

**方法**

返回此向量的 2D 平方长度。

此方法在性能上比非平方变体更快。如果需要额外性能，请使用此方法。

**参数**

* **无参数**。

**返回值**

* **类型**: float
* **描述**: 此向量的长度。

**示例**

```lua
local vec = vector(5, 1, 6);
local length = vec:length_2d_sqr();
```

**方法 `dot`**

**方法**

返回两个向量的点积。

**参数**

* **名称**: other
  * **类型**: vector
  * **描述**: 要计算点积的向量。

**返回值**

* **类型**: float
* **描述**: 点积。

**示例**

```lua
local vec1 = vector(
```

***

苏黎世银云安全 ©
