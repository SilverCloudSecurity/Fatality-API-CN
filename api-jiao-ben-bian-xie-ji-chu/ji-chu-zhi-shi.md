# 基础知识

**欢迎开始脚本编写**

在您已经了解了基础知识之后，现在是时候开始编写脚本了。

**启动文本编辑器**

您可以使用任何您喜欢的文本编辑器：Visual Studio Code、Notepad++ 或者简单的记事本。

本地脚本位于以下路径：`<CS2_Directory>/game/csgo/fatality/scripts`。您可能会注意到还有一个 `lib` 目录，我们稍后会介绍它。

创建一个以 `.lua` 结尾的新文件，并开始编写脚本。

**注意：** `.ljbc` 格式无法从本地源加载。

**编写第一个脚本**

一个典型的“Hello world!”示例可能有些简单，因此让我们尝试一个稍微复杂一点的例子。

```lua
local function on_present_queue()
    local d = draw.surface;
    d.font = draw.fonts['gui_main'];
    d:add_text(draw.vec2(50, 50),
        'Hello drawing! My first script speaking.',
        draw.color.white()
    );
end

events.present_queue:add(on_present_queue);
```

现在，我们来分解这个示例脚本：

**定义回调函数**

大部分脚本将在我们提供的几个回调函数中运行。每个事件都有其特定的签名，因此请注意回调函数应接受的参数。`present_queue` 不提供任何参数，因此我们的函数也不需要任何参数。

```lua
local function on_present_queue()
end
```

定义局部变量是可选的，但推荐这样做以更好地管理作用域。

**访问绘图层**

定义了回调函数后，让我们在屏幕上实际绘制一些内容！

为此，您首先需要访问绘图层。我们提供了一个可以在游戏线程中安全使用的绘图层。由于游戏的内部工作方式，强烈建议不要在其他线程中调用游戏函数。幸运的是，所有我们的事件都在游戏线程中运行。

这个设置不仅允许您绘制，还可以查询玩家生命值或其他实体的信息。

要访问该层，只需引用 `draw` 表中的 `surface` 字段：

```lua
local d = draw.surface;
```

您不必将其存储在变量中，但这样可以避免每次都输入 `draw.surface`，不是吗？

**设置字体**

检索到层后，您必须在屏幕上绘制任何文本之前设置一个字体对象。这纯粹是为了性能原因，因此您不必每次绘制文本时都传递一个沉重的字体对象。

所有字体都存储在 `draw.fonts` 中。要访问字体，可以使用点语法或将其视为字典：

```lua
d.font = draw.fonts['gui_main'];
```

**绘制文本**

设置字体后，现在可以绘制一些文本了。

调用层上的 `add_text` 方法。请注意，它是使用冒号语法调用的：`obj:fn()`，因为它是一个方法。

您也可以使用点语法调用方法，只要在第一个参数中提供对象。两种调用方式 `obj:fn()` 和 `obj.fn(obj)` 是相同的。

```lua
d:add_text(draw.vec2(50, 50),
    'Hello drawing! My first script speaking.',
    draw.color.white()
);
```

**注册回调**

现在您已经创建了第一个回调，需要将其注册，以便 Fatality 知道何时调用它。这是通过调用 `events.present_queue` 上的 `add` 方法完成的。

```lua
events.present_queue:add(on_present_queue);
```

**结果**

完成上述步骤后，如果一切正确，您应该会看到类似以下的内容：

<figure><img src="../../.gitbook/assets/fs.png" alt=""><figcaption><p>如图</p></figcaption></figure>

***

苏黎世银云安全 ©
