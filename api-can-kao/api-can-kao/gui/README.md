---
description: 欢迎使用 Fatality
---

# GUI

最后修改时间

25 December 2024

### 简介

`gui` 表暴露了软件的 GUI 系统

子部分中描述的所有类型和枚举必须以 `gui.` 前缀

***

### 字段

#### ctx

* **类型**: `context`
* **描述**: GUI 上下文

#### notify

* **类型**: `notification_system`
* **描述**: 通知系统

***

### 函数

#### make\_control

* **描述**: 将控件包装在一个布局中 该布局包含一个标签和该特定控件 如果希望控件显示良好 应将其添加到组框中 此外 还可以向返回的控件添加任何其他控件 这些控件将堆叠在初始控件的左侧
* **参数**:
  * `text`: `string` - 标签值
  * `c`: `control` - 控件对象
* **返回值**:
  * `layout` - 布局对象
* **示例**:

```lua
local row = gui.make_control('Hello checkbox!', my_cb)
```

***

苏黎世银云安全 ©
