---
description: 欢迎开始使用 Fatality
---

# 全局函数

以下是所有全局函数的列表。所谓“全局”，意味着这些函数不需要前缀命名空间，可以直接调用，与其他函数不同

**print**

**函数**

在游戏控制台中打印文本

**参数**

| 名称   | 类型     | 描述           |
| ---- | ------ | ------------ |
| text | string | 要在控制台中打印的字符串 |

**返回值**

无

**示例**

```lua
print('Hello world!'); -- 在控制台中打印 "Hello world!"
```

**error**

**函数**

在游戏控制台中打印错误文本，并关闭脚本。尽量避免使用此函数，仅在发生无法恢复的错误时使用。

**参数**

| 名称   | 类型     | 描述               |
| ---- | ------ | ---------------- |
| text | string | 请参阅 `print` 的文档。 |

**返回值**

无

**示例**

```lua
error('Can\'t recover from this one! Error: ' .. tostring(123));
```

***

苏黎世银云安全 ©