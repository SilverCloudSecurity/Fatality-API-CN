---
description: 欢迎使用 Fatality
---

# draw 表

**欢迎开始使用 `draw` 表**

_<mark style="color:red;">`draw`</mark> <mark style="color:red;"></mark><mark style="color:red;">表描述了软件的渲染系统</mark>_

所有子节中描述的类型和枚举必须以 `draw.` 为前缀 以避免与其他类型混淆 例如 渲染和游戏中的不同颜色类型

**字段**

* **adapter**
  * **类型**: adapter
  * **描述**: 渲染适配器
  * **读取权限**: 只读
* **frame\_time**
  * **类型**: float
  * **描述**: 渲染帧时间 全局变量 `global_vars_t.frame_time` 的别名
  * **读取权限**: 只读
* **time**
  * **类型**: float
  * **描述**: 时间 单位为秒 全局变量 `global_vars_t.real_time` 的别名
  * **读取权限**: 只读
* **scale**
  * **类型**: float
  * **描述**: 全局 DPI 缩放
  * **读取权限**: 只读
* **display**
  * **类型**: vec2
  * **描述**: 显示区域大小 (视口尺寸) `cengine_client:get_screen_size` 将返回相同值 修改此向量的任何值将导致未定义行为
  * **读取权限**: 只读
* **textures**
  * **类型**: accessor
  * **描述**: 所有管理纹理的字符串到纹理映射 可以查询和推送具有自定义 ID 的纹理 当向此映射添加纹理时 它将在需要时自动销毁和重新创建 (例如 当 DX11 设备丢失时)
  * **内置纹理**:
    * `gui_loading`: 加载旋转器
    * `gui_user_avatar`: 当前用户的个人资料图片 如果未设置头像则可能为 nil
    * `gui_icon_up`: 向上箭头
    * `gui_icon_down`: 向下箭头
    * `gui_icon_copy`: 复制图标
    * `gui_icon_paste`: 粘贴图标
    * `gui_icon_add`: 添加图标
    * `gui_icon_search`: 搜索图标
    * `gui_icon_settings`: 设置图标 (齿轮)
    * `gui_icon_bug`: 昆虫图标
    * `gui_icon_key.N`: 键盘/鼠标键图标 替换 N 为所需按钮的字符代码
    * `icon_rage`: RAGE 选项卡图标
    * `icon_legit`: LEGIT 选项卡图标
    * `icon_visuals`: VISUALS 选项卡图标
    * `icon_misc`: MISC 选项卡图标
    * `icon_scripts`: LUA 选项卡图标
    * `icon_skins`: SKINS 选项卡图标
    * `icon_cloud`: 云图标
    * `icon_file`: 文件图标
    * `icon_refresh`: 刷新图标
    * `icon_save`: 保存图标
    * `icon_configs`: "Configs" 弹出窗口图标
    * `icon_keys`: 键盘图标
    * `icon_info`: "About" 弹出窗口图标
    * `icon_close`: 关闭图标 (叉号)
    * `icon_load`: 加载图标
    * `icon_import`: 导入图标
    * `icon_export`: 导出图标
    * `icon_delete`: 删除图标
    * `icon_autoload`: "Autoload" 图标
    * `icon_allow_insecure`: "Allow insecure" 图标
    * `icon_cloud_upd`: 云更新图标
    * `player_texture`: 玩家预览纹理
  * **读取权限**: 只读
* **fonts**
  * **类型**: accessor\<font\_base>
  * **描述**: 所有管理字体的字符串到字体映射 可以查询和推送具有自定义 ID 的字体 当向此映射添加字体时 它将在需要时自动销毁和重新创建 (例如 当 DX11 设备丢失时)
  * **内置字体**:
    * `gui_debug`: Verdana 13px
    * `gui_title`: Figtree ExtraBold 23px
    * `gui_main`: Figtree Medium 14px
    * `gui_main_shadow`: Figtree Medium 14px 带阴影
    * `gui_main_fb`: Segoe UI Semibold 14px
    * `gui_bold`: Figtree ExtraBold 14px
    * `gui_bold_fb`: Segoe UI Black 14px
    * `gui_semi_bold`: Figtree SemiBold 14px
    * `gui_semi_bold_fb`: Segoe UI Bold 14px
  * **读取权限**: 只读
* **shaders**
  * **类型**: accessor
  * **描述**: 所有管理着色器的字符串到着色器映射 可以查询和推送具有自定义 ID 的着色器 当向此映射添加着色器时 它将在需要时自动销毁和重新创建 (例如 当 DX11 设备丢失时)
  * **内置着色器**:
    * `blur_f`: 高斯模糊着色器
  * **读取权限**: 只读
* **surface**
  * **类型**: layer
  * **描述**: 可以在此图层上渲染
  * **读取权限**: 只读

***

苏黎世银云安全 ©
