---
description: 欢迎使用 Fatality
---

# Font Flags

最后修改时间

25 December 2024

### 简介

`font_flags` 枚举确定字体对象应具有的标志 设置这些标志仅在类型构造时可能

***

### 字段

#### shadow

* **类型**: `Field`
* **描述**: 为字体字形添加 1px 阴影

#### outline

* **类型**: `Field`
* **描述**: 为字体字形添加 1px 轮廓

#### anti\_alias

* **类型**: `Field`
* **描述**: 启用字体字形的抗锯齿 仅适用于 GDI 字体

#### no\_dpi

* **类型**: `Field`
* **描述**: 禁用此字体的 DPI 缩放 默认情况下 字体字形将根据全局 DPI 缩放进行缩放

#### no\_kern

* **类型**: `Field`
* **描述**: 禁用此字体的字形 kerning

#### mono

* **类型**: `Field`
* **描述**: 启用光栅化时的强提示算法 仅适用于 FreeType 字体

#### light

* **类型**: `Field`
* **描述**: 启用光栅化时的轻提示算法 仅适用于 FreeType 字体

***

苏黎世银云安全 ©
