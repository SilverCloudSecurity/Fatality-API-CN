---
description: 欢迎使用 Fatality
---

# Animated Texture

最后修改时间

25 December 2024

### 简介

`animated_texture` 类型表示一个动画纹理 此纹理类型仅支持动画 GIF 格式 不支持 APNG

此类型继承自 `texture` 类型 因此其所有基方法和字段在此类型中也可用

如果传递不支持的类型 它将像 `texture` 类型一样工作 控制帧和循环将毫无意义

虽然可以使用此类型进行纹理图集 但强烈不推荐 这将产生额外的纹理对象 并且整体性能会更差 建议构造实际的纹理图集 使用 `texture` 类型 并使用纹理映射

***

### 构造函数

#### \_\_call

* **描述**: 构造动画纹理
* **注意事项**: 传递无效指针或内存区域小于所需大小将导致崩溃
* **参数**:
  1. **从文件**
     * `path`: `string` - 纹理文件的路径
  2. **从内存**
     * `data`: `ptr` - 指向内存中纹理文件数据的指针
     * `sz`: `int` - 纹理文件数据的大小
* **返回值**:
  * `animated_texture` - 动画纹理实例
* **示例**:

```lua
local gif = draw.animated_texture('funny_gif.gif')
```

***

### 字段

#### should\_loop

* **类型**: `bool`
* **描述**: 如果设置为 `false` 将不会自动循环动画 默认为 `true`

***

### 方法

#### reset\_loop

* **描述**: 重置循环 从第一帧开始运行
* **参数**: 无
* **返回值**: 无
* **示例**:

```lua
gif:reset_loop
```

#### set\_frame

* **描述**: 设置动画的特定帧 如果启用了循环 将从传递的帧继续循环 否则 将显示动画的特定帧
* **注意事项**: 帧计数从 0 开始 无效的帧号将被限制在有效范围内
* **参数**:
  * `frame`: `int` - 帧号
* **返回值**: 无
* **示例**:

```lua
gif:set_frame(5)
```

#### get\_frame\_count

* **描述**: 返回动画中的帧数
* **参数**: 无
* **返回值**:
  * `int` - 帧数
* **示例**:

```lua
local frames = gif:get_frame_count
gif:set_frame(frames - 2) -- 设置为最后一帧
```

***

苏黎世银云安全 ©
