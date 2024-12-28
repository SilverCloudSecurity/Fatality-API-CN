---
description: 欢迎使用 Fatality
---

# accessor﻿ 类型

这种类型表示一种安全的方式来访问映射

_<mark style="color:red;">注意 表示该实例持有的特定类型 例如 accessor 意味着 get 将返回一个 texture 实例 而 set 只接受类型为 texture 的对象作为其 obj 参数</mark>_

**方法**

**`__index`**

通过键返回对象

**参数**

* `key` string 对象键

**返回值**

* `<type>` 对象

**示例**

```lua
local main_font = draw.fonts['gui_main']

-- 这也可以工作
local main_font_2 = draw.fonts.gui_main
```

**`__newindex`**

通过键设置对象

**参数**

* `key` string 对象键
* `obj` 对象

**返回值**

* 无

**示例**

```lua
draw.fonts['my_font'] = my_font

-- 这也可以工作
draw.fonts.my_font = my_font
```

***

苏黎世银云安全 ©
