---
description: 欢迎使用 Fatality
---

# adapter 类型（渲染适配器）

渲染适配器类型

_<mark style="color:red;">这种类型表示渲染系统中使用的渲染适配器</mark>_

**方法**

**`get_back_buffer`**

返回一个后台缓冲纹理 可能返回一个空白或过时的纹理 如果后台缓冲纹理未更新

**参数**

* 无参数

**返回值**

* `ptr` 后台缓冲纹理指针

**示例**

```lua
local bb = adapter:get_back_buffer()
```

**`get_back_buffer_downsampled`**

返回后台缓冲纹理的4倍下采样版本

**参数**

* 无参数

**返回值**

* `ptr` 下采样后台缓冲纹理指针

**示例**

```lua
local ds = adapter:get_back_buffer_downsampled()
```

**`get_shared_texture`**

返回一个共享纹理 该纹理通常复制下采样后台缓冲纹理 但会在图层渲染开始前自动更新一次

**参数**

* 无参数

**返回值**

* `ptr` 共享纹理指针

**示例**

```lua
local shared = adapter:get_shared_texture()
```
