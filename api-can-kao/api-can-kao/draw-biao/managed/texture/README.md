---
description: 欢迎使用 Fatality
---

# Texture

最后修改时间

25 December 2024

### 简介

`texture` 类型表示一个纹理对象

此类型继承自 `managed` 类型 因此其所有基方法和字段在此类型中也可用

支持的纹理格式包括:

* JPEG (.jpg, .jpeg) - 不支持 12 bpc 和算术编码
* PNG (.png)
* TGA (.tga)
* BMP (.bmp) - 不支持 1 bpp 和 RLE 变体
* PSD (.psd) - 仅支持合成视图 无额外通道 8/16 bpc
* GIF (.gif) - 仅支持第一帧 动画 GIF 请使用 `animated_texture`
* HDR (.hdr)
* PIC (.pic)
* PNM (.pnm, .ppm, .pgm) - PPM 和 PGM 仅支持二进制格式

***

### 构造函数

#### \_\_call

* **描述**: 构造此类型的实例
* **注意事项**: 传递无效指针或内存区域小于所需大小将导致崩溃
* **参数**:
  1. **从文件**
     * `path`: `string` - 有效纹理文件的路径
  2. **从内存**
     * `data`: `ptr` - 指向内存中纹理文件数据的指针
     * `sz`: `int` - 纹理文件数据的大小
  3. **从 RGBA 数据**
     * `data`: `ptr` - 指向内存中 RGBA 数据的指针
     * `w`: `int` - 宽度
     * `h`: `int` - 高度（行数）
     * `p`: `int` - 行宽（每行字节数）
* **返回值**:
  * `texture` - 纹理对象
* **示例**:

```lua
local tex = draw.texture('funny_meme.png')
```

***

### 字段

#### is\_animated

* **只读**
* **类型**: `bool`
* **描述**: 如果此实例为 `animated_texture` 则设置为 `true`

***

### 方法

#### get\_size

* **描述**: 返回此纹理的大小
* **参数**: 无
* **返回值**:
  * `vec2` - 纹理尺寸
* **示例**:

```lua
local sz = tex:get_size
```

***

苏黎世银云安全 ©
