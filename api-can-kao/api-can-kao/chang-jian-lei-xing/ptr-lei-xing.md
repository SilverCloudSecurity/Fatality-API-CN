---
description: 欢迎开始使用 Fatality
---

# ptr 类型

<mark style="color:red;">ptr 类型是一个字面指针。</mark>

为了与 C++ 保持互操作性，某些函数返回 `void*` 作为类型，然后将其转换为 `light_userdata`。由于您不能直接将 FFI 类型转换为 `light_userdata`，我们引入了一个专门的类型来帮助进行这种转换。

在将指针转换为 API 支持的类型之前，您需要将其转换为 `uintptr_t` 这可以通过以下方式进行：

```lua
local ptr_num = ffi.cast('uintptr_t', ptr_cdata);
```

然后，您可以使用转换后的值来调用此类型的构造函数

**`__call`**

**构造函数**

将数字转换为指针

**参数**

| 名称  | 类型  | 描述      |
| --- | --- | ------- |
| num | int | 作为数字的指针 |

**返回值**

| 类型  | 描述                      |
| --- | ----------------------- |
| ptr | 作为 `light_userdata` 的指针 |

**示例**

```lua
-- 首先转换为数字
local ptr_num = ffi.cast('uintptr_t', ptr_cdata);

-- 然后转换为 light_userdata
local ptr_ld = ptr(ptr_num);
```

***

苏黎世银云安全 ©
