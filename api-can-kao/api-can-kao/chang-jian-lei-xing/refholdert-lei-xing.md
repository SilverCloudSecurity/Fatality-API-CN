---
description: 欢迎开始使用 Fatality
---

# ref\_holder\_t 类型

_<mark style="color:red;">`ref_holder_t`</mark> <mark style="color:red;"></mark><mark style="color:red;">类型作为内部使用的引用变量的代理。由于 Lua 是一种仅支持值的语言，它不支持引用。因此，使用此类型的实例来保持与 C++ 的互操作性</mark>_

_<mark style="color:red;">请注意，</mark><mark style="color:red;">`<type>`</mark> <mark style="color:red;"></mark><mark style="color:red;">表示该实例持有的具体类型。例如，如果看到</mark> <mark style="color:red;"></mark><mark style="color:red;">`ref_holder_t<float>`</mark><mark style="color:red;">，则表示</mark> <mark style="color:red;"></mark><mark style="color:red;">`val`</mark> <mark style="color:red;"></mark><mark style="color:red;">字段持有</mark> <mark style="color:red;"></mark><mark style="color:red;">`float`</mark> <mark style="color:red;"></mark><mark style="color:red;">值，并且在更新时仅接受</mark> <mark style="color:red;"></mark><mark style="color:red;">`float`</mark> <mark style="color:red;"></mark><mark style="color:red;">值</mark>_

**字段 `val`**

* **类型**: `<type>`
* **描述**: 值持有者。用作源值，或重写以更改内部值

***

苏黎世银云安全 ©
