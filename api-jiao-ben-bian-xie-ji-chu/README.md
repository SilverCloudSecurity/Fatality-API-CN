---
description: 欢迎开始使用 Fatality
---

# API 脚本编写基础

**欢迎使用 Fatality API**

Fatality 的 API 设计旨在镜像软件的内部结构，为您提供对其子系统的实质性控制。某些可能导致不稳定或损坏的功能受到限制。

**重要提示：**\
工作坊脚本目前未受保护，可能被提取。保护措施将尽快推出。

**基本概念**

我们的脚本引擎使用 LuaJIT 2.1（带有少量自定义）。它完全兼容 Lua 5.1，并包含一些 Lua 5.2 的增强功能。

标准库 `baselib`、`bit`、`ffi`、`math`、`string` 和 `table` 可用。请注意，`ffi` 库仅在启用“允许不安全”选项时可用。更多详情请参阅官方 Lua 文档。

如果我们在任何时候修改了任何标准函数，我们将记录这些更改以保持透明。

**文档概述**

在整个 API 参考中，您会遇到用于描述特定方法或字段的各种标签。

**标签说明**

* **Field（字段）**：表示这是一个标准字段。其类型将在名称下方解释。
* **Function（函数）**：表示这是一个函数，使用点语法调用（例如 `obj.fn()`）。
* **Method（方法）**：表示这是一个方法，建议使用冒号语法调用（例如 `obj:fn()`）。
* **Constructor（构造函数）**：表示这是一个构造函数定义。您不应调用任何特定字段，而是直接调用类型本身（例如 `vector()`）。
* **Read Only（只读）**：表示该字段是只读的，其值无法更改。此限制通常不扩展到任何子元素。

**参数和返回列表**

参数和返回值按您必须提供或捕获的确切顺序列出。例如，如果一个参数显示在第一位，则应作为第一个参数传递给函数。同样，对于返回值：第一个列出的值将放置在您声明的第一个变量中，依此类推。

**类型说明**

某些类型描述包含特殊符号：

* `type?` 表示该类型可能是 `nil`。
* `type<other>` 表示内部方法或字段将使用 `other` 类型。
* `<other>` 表示该类型将是 `other` 或其任何子类型。

**规则**

为了确保您的脚本安全且易于使用，我们实施了许多安全措施。但由于某些特定功能的工作方式，我们无法完全确保其绝对安全。因此，在编写脚本之前，请注意以下几点：

**您控制 Lua 状态**

您可以替换或覆盖 API 函数，但您有责任维护稳定的行为。如果您在默认 API 中遇到任何错误（FFI 除外），请报告给我们以便解决问题。

**优先考虑安全性**

使用 FFI 授予您广泛的自由度。请记住，任何可能对用户造成伤害的脚本都是不允许的，并将被移除。尽可能依赖提供的 API 或请求额外功能，如果需要当前未提供的功能。严格禁止自定义“脚本加载器”。

**保持软件可用性**

避免隐藏无关的 UI 元素、阻碍用户输入或干扰整体用户体验。破坏功能或骚扰用户的脚本将从工作坊中移除。

***

苏黎世银云安全 ©