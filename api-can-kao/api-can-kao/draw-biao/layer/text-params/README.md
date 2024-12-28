---
description: 欢迎使用 Fatality
---

# Text Params

最后修改时间

25 December 2024

### 简介

`text_params` 类型用于确定文本对齐方式。行对齐仅在文本有多行时才有意义。默认情况下，所有后续行将从文本的左侧开始。您可以使用带有行参数的函数之一来更改此行为。例如，如果将 `right` 传递给行对齐，所有后续行将从右侧开始。文本对齐将保持由 `v` 和 `h` 参数指定的方式。

***

### 函数

#### with\_v

* **描述**: 创建带有垂直对齐的 `text_params` 实例
* **参数**:
  * `v`: `text_alignment` - 垂直对齐
* **返回值**:
  * `text_params` - 创建的文本参数
* **示例**:

```lua
local align_top = draw.text_params.with_v(draw.text_alignment.top)
```

#### with\_h

* **描述**: 创建带有水平对齐的 `text_params` 实例
* **参数**:
  * `h`: `text_alignment` - 水平对齐
* **返回值**:
  * `text_params` - 创建的文本参数
* **示例**:

```lua
local align_right = draw.text_params.with_h(draw.text_alignment.right)
```

#### with\_line

* **描述**: 创建带有行对齐的 `text_params` 实例
* **参数**:
  * `line`: `text_alignment` - 行对齐
* **返回值**:
  * `text_params` - 创建的文本参数
* **示例**:

```lua
local lines_center = draw.text_params.with_line(draw.text_alignment.center)
```

#### with\_vh

* **描述**: 创建带有垂直和水平对齐的 `text_params` 实例
* **参数**:
  * `v`: `text_alignment` - 垂直对齐
  * `h`: `text_alignment` - 水平对齐
* **返回值**:
  * `text_params` - 创建的文本参数
* **示例**:

```lua
local align_bottom_right = draw.text_params.with_vh(draw.text_alignment.bottom, draw.text_alignment.right)
```

#### with\_vline

* **描述**: 创建带有垂直和行对齐的 `text_params` 实例
* **参数**:
  * `v`: `text_alignment` - 垂直对齐
  * `line`: `text_alignment` - 行对齐
* **返回值**:
  * `text_params` - 创建的文本参数
* **示例**:

```lua
local align = draw.text_params.with_vline(draw.text_alignment.bottom, draw.text_alignment.center)
```

#### with\_hline

* **描述**: 创建带有水平和行对齐的 `text_params` 实例
* **参数**:
  * `h`: `text_alignment` - 水平对齐
  * `line`: `text_alignment` - 行对齐
* **返回值**:
  * `text_params` - 创建的文本参数
* **示例**:

```lua
local align = draw.text_params.with_hline(draw.text_alignment.center, draw.text_alignment.center)
```

#### with\_vhline

* **描述**: 创建带有垂直、水平和行对齐的 `text_params` 实例
* **参数**:
  * `v`: `text_alignment` - 垂直对齐
  * `h`: `text_alignment` - 水平对齐
  * `line`: `text_alignment` - 行对齐
* **返回值**:
  * `text_params` - 创建的文本参数
* **示例**:

```lua
local align = draw.text_params.with_vhline(draw.text_alignment.center, draw.text_alignment.center, draw.text_alignment.center)
```

***

苏黎世银云安全 ©
