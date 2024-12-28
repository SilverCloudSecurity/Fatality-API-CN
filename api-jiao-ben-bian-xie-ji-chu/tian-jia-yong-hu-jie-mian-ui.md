---
description: 欢迎开始使用 Fatality
---

# 添加用户界面（UI）

添加用户界面文档

**欢迎开始添加用户界面**

在您已经了解了基础知识之后，现在让我们通过允许用户切换文本来扩展我们的脚本。我们可以通过在菜单中添加一个控件来实现这一点。

### 创建控件

首先，我们创建一个简单的复选框：

```lua
local cb = gui.checkbox(gui.control_id('my_checkbox'));
```

每个控件都有一个唯一的 ID，UI 框架使用该 ID 在容器中区分控件。确保您的控件 ID 不与其他控件冲突，否则可能会导致状态损坏或其他问题。

要创建 ID，请调用 `gui.control_id` 并传递所需的 ID。

然后，通过调用 `gui.checkbox` 并传递您创建的 ID 结构来创建复选框。

### 构建行

默认情况下，控件通常放置在行中——这些布局以特定方式堆叠元素。我们提供了一个简单的辅助函数 `gui.make_control`。

```lua
local row = gui.make_control('My checkbox', cb);
```

### 将行添加到组

有了控件和行，接下来将它们添加到一个组中。

> **注意：**
>
> 要查看组和控件 ID，可以在 SCRIPTS 标签中启用调试模式。

在这个示例中，我们将使用 `lua>elements a` 组。首先，在全局上下文中找到该组：

```lua
local group = gui.ctx:find('lua>elements a');
```

然后调用其 [`add`](https://lua.fatality.win/container.html#add) 方法以包含您的行：

```lua
group:add(row);
```

这样就完成了！

### 使用值

接下来，让我们修改之前的脚本，使文本仅在复选框被选中时出现。在绘制文本之前，将绘制代码用 `if` 语句包裹：

```lua
if cb:get_value():get() then
```

并在之后关闭 `if` 语句。

最终脚本应如下所示：

```lua
local cb = gui.checkbox(gui.control_id('my_checkbox'));
local row = gui.make_control('My checkbox', cb);
local group = gui.ctx:find('lua>elements a');
group:add(row);

local function on_present_queue()
    if cb:get_value():get() then
        local d = draw.surface;
        d.font = draw.fonts['gui_main'];
        d:add_text(draw.vec2(50, 50),
            'Hello drawing! My first script speaking.',
            draw.color.white()
        );
    end
end

events.present_queue:add(on_present_queue);
```

**结果**

完成上述步骤后，如果一切正确，您应该会看到类似以下的内容：

<figure><img src="../../.gitbook/assets/ex1.png" alt=""><figcaption><p>如图</p></figcaption></figure>

***

苏黎世银云安全 ©
