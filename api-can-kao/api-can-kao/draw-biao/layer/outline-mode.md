---
description: 欢迎使用 Fatality
---

# Outline Mode

最后修改时间

25 December 2024

### 简介

`OutlineMode` 枚举用于确定带轮廓形状的轮廓模式。以下是可用的轮廓模式及其描述

***

### 枚举值

#### inset

* **类型**: `Field`
* **描述**: 内嵌轮廓。这意味着轮廓将位于形状内部（从左上角向内 +1px，从右下角向内 -1px）

#### outset

* **类型**: `Field`
* **描述**: 外嵌轮廓。这意味着轮廓将位于形状外部（从左上角向外 -1px，从右下角向外 +1px）

#### center

* **类型**: `Field`
* **描述**: 中心轮廓。这意味着轮廓将与形状大小匹配

***

### 示例用法

```lua
-- 设置轮廓模式为内嵌
shape:set_outline_mode(outline_mode.inset)

-- 设置轮廓模式为外嵌
shape:set_outline_mode(outline_mode.outset)

-- 设置轮廓模式为中心
shape:set_outline_mode(outline_mode.center)
```

***

通过以上文档，您可以详细了解 `OutlineMode` 枚举及其相关字段的功能和用法。希望这些信息对您有所帮助

***

苏黎世银云安全 ©
