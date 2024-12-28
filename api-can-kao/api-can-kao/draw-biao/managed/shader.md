---
description: 欢迎使用 Fatality
---

# Shader

最后修改时间

25 December 2024

### 简介

`shader` 类型表示一个着色器 HLSL 文档

此类型继承自 `managed` 类型 因此其所有基方法和字段在此类型中也可用

仅支持片段着色器（在 DirectX 中称为像素着色器）

渲染系统使用 Shader Version 4 (ps\_4\_0)

***

### HLSL 结构

#### 常量缓冲区字段

| 名称    | 类型       | 描述          |
| ----- | -------- | ----------- |
| mvp   | float4x4 | 投影矩阵        |
| tex   | float2   | 纹理尺寸        |
| time  | float    | 渲染时间（不是帧时间） |
| alpha | float    | 全局不透明度覆盖    |

#### 输入字段

| 名称  | 类型     | 描述                                         |
| --- | ------ | ------------------------------------------ |
| pos | float4 | 屏幕上的顶点位置 (x, y, z over w) 注册: SV\_POSITION |
| col | float4 | 顶点颜色色调 (r, g, b, a) 注册: COLOR0             |
| uv  | float2 | UV 坐标 (u, v) 注册: TEXCOORD0                 |

#### 绑定对象

| 名称       | 类型        | 描述    |
| -------- | --------- | ----- |
| sampler0 | sampler   | 纹理采样器 |
| texture0 | Texture2D | 纹理对象  |

#### 模板

```hlsl
cbuffer cb : register(b0) {
    float4x4 mvp;
    float2 tex;
    float time;
    float alpha;
};

struct PS_INPUT {
    float4 pos : SV_POSITION;
    float4 col : COLOR0;
    float2 uv : TEXCOORD0;
};

sampler sampler0;
Texture2D texture0;
```

***

### 构造函数

#### \_\_call

* **描述**: 构造着色器
* **参数**:
  * `src`: `string` - 着色器源代码
* **返回值**:
  * `shader` - 着色器对象
* **示例**:

```lua
local blur = draw.shader([[
// define constant buffer.
cbuffer cb : register(b0) {
    float4x4 mvp;
    float2 tex;
    float time;
    float alpha;
};

// define input.
struct PS_INPUT {
    float4 pos : SV_POSITION;
    float4 col : COLOR0;
    float2 uv : TEXCOORD0;
};

// use texture sampler and texture.
sampler sampler0;
Texture2D texture0;

float4 main(PS_INPUT inp) : SV_Target {
    float radius = 2.0; // blur radius
    float2 inv_size = 1.0 / tex.xy; // inversed size of the texture
    float weight = 0.0; // total weight
    float4 color = 0.0; // total color

    // perform a gaussian blur
    for (float x = -radius; x <= radius; x += 1.0)
    {
        for (float y = -radius; y <= radius; y += 1.0)
        {
            float2 coord = inp.uv + float2(x, y) * inv_size;
            color += texture0.Sample(sampler0, coord) * exp(-((x * x + y * y) / (2.0 * radius * radius)));
            weight += exp(-((x * x + y * y) / (2.0 * radius * radius)));
        }
    }

    // average the color
    color /= weight;
    color.a *= inp.col.a; // apply alpha modulation
    return color;
}
]])
```

***

苏黎世银云安全 ©
