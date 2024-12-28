---
description: 欢迎使用 Fatality
---

# Container

最后修改时间

25 December 2024

### 简介

`container` 类型表示一个抽象容器

***

### 方法

#### add

* **描述**: 将控件添加到容器中
* **参数**:
  * `ctrl`: `control` - 要添加的控件
* **返回值**: 无
* **示例**:

```lua
container:add(my_control)
```

#### remove

* **描述**: 从容器中移除控件
* **参数**:
  * `ctrl`: `control` - 要移除的控件
* **返回值**: 无
* **示例**:

```lua
container:remove(my_control)
```

#### find

* **描述**: 通过 ID 查找控件
* **参数**:
  * `id`: `string` - 控件 ID
* **返回值**:
  * `<control>?` - 转换后的控件 如果未找到控件或转换失败 则返回 `nil`
* **示例**:

```lua
local some_cb = container:find('some_cb')
```

***

苏黎世银云安全 ©
