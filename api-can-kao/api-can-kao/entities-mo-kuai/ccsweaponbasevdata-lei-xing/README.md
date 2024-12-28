---
description: 欢迎使用 Fatality
---

# ccsweapon\_base\_vdata 类型

**欢迎开始使用 `ccsweapon_base_vdata` 类型**

_<mark style="color:red;">`ccsweapon_base_vdata`</mark> <mark style="color:red;"></mark><mark style="color:red;">表示武器的静态数据</mark>_

**字段**

* **built\_right\_handed**
  * **类型**: bool
  * **描述**: 武器是否为右手法设计
* **allow\_flipping**
  * **类型**: bool
  * **描述**: 武器是否可以翻转为左手使用
* **linked\_cooldowns**
  * **类型**: bool
  * **描述**: 武器的冷却时间是否与其他武器关联
* **flags**
  * **类型**: int
  * **描述**: 与武器相关的各种标志
* **primary\_ammo\_type**
  * **类型**: int
  * **描述**: 主弹夹使用的弹药类型
* **secondary\_ammo\_type**
  * **类型**: int
  * **描述**: 副弹夹使用的弹药类型
* **max\_clip1**
  * **类型**: int
  * **描述**: 主弹夹的最大容量
* **max\_clip2**
  * **类型**: int
  * **描述**: 副弹夹的最大容量
* **default\_clip1**
  * **类型**: int
  * **描述**: 主弹夹的默认弹药数量
* **default\_clip2**
  * **类型**: int
  * **描述**: 副弹夹的默认弹药数量
* **reserve\_ammo\_as\_clips**
  * **类型**: bool
  * **描述**: 备用弹药是否以额外弹夹形式存储
* **weight**
  * **类型**: int
  * **描述**: 武器的重量
* **auto\_switch\_to**
  * **类型**: bool
  * **描述**: 捡起时游戏是否会自动切换到此武器
* **auto\_switch\_from**
  * **类型**: bool
  * **描述**: 游戏是否会自动从该武器切换出去
* **rumble\_effect**
  * **类型**: int
  * **描述**: 与此武器关联的震动效果
* **slot**
  * **类型**: int
  * **描述**: 武器占据的库存槽位
* **position**
  * **类型**: int
  * **描述**: 武器在库存槽位中的位置
* **weapon\_type**
  * **类型**: csweapon\_type
  * **描述**: 武器类型
* **weapon\_category**
  * **类型**: csweapon\_category
  * **描述**: 武器类别
* **gear\_slot**
  * **类型**: int
  * **描述**: 与此武器关联的装备槽位
* **gear\_slot\_position**
  * **类型**: int
  * **描述**: 武器在装备槽位中的位置
* **default\_loadout\_slot**
  * **类型**: int
  * **描述**: 武器的默认装备槽位
* **s\_wrong\_team\_msg**
  * **类型**: string
  * **描述**: 当错误队伍使用武器时显示的消息
* **price**
  * **类型**: int
  * **描述**: 武器的购买价格
* **kill\_award**
  * **类型**: int
  * **描述**: 使用此武器击杀后给予玩家的现金奖励
* **primary\_reserve\_ammo\_max**
  * **类型**: int
  * **描述**: 主弹夹的最大备用弹药量
* **secondary\_reserve\_ammo\_max**
  * **类型**: int
  * **描述**: 副弹夹的最大备用弹药量
* **melee\_weapon**
  * **类型**: bool
  * **描述**: 武器是否为近战武器
* **has\_burst\_mode**
  * **类型**: bool
  * **描述**: 武器是否有连发模式
* **is\_revolver**
  * **类型**: bool
  * **描述**: 武器是否为左轮手枪
* **cannot\_shoot\_underwater**
  * **类型**: bool
  * **描述**: 武器是否不能在水下射击
* **name**
  * **类型**: string
  * **描述**: 武器的内部名称
* **anim\_extension**
  * **类型**: string
  * **描述**: 武器使用的动画扩展
* **e\_silencer\_type**
  * **类型**: int
  * **描述**: 武器兼容的消音器类型
* **crosshair\_min\_distance**
  * **类型**: int
  * **描述**: 武器的最小准心扩散距离
* **crosshair\_delta\_distance**
  * **类型**: int
  * **描述**: 射击时准心扩散距离的变化
* **is\_full\_auto**
  * **类型**: bool
  * **描述**: 武器是否为全自动
* **num\_bullets**
  * **类型**: int
  * **描述**: 每次射击发射的子弹数量
* **cycle\_time**
  * **类型**: cfiring\_mode
  * **描述**: 连续射击的时间间隔
* **max\_speed**
  * **类型**: cfiring\_mode
  * **描述**: 持有此武器时玩家的最大移动速度
* **spread**
  * **类型**: cfiring\_mode
  * **描述**: 射击时的基础散布值
* **inaccuracy\_crouch**
  * **类型**: cfiring\_mode
  * **描述**: 蹲伏时的不准确度
* **inaccuracy\_stand**
  * **类型**: cfiring\_mode
  * **描述**: 站立时的不准确度
* **inaccuracy\_jump**
  * **类型**: cfiring\_mode
  * **描述**: 跳跃时的不准确度
* **inaccuracy\_land**
  * **类型**: cfiring\_mode
  * **描述**: 落地后的不准确度
* **inaccuracy\_ladder**
  * **类型**: cfiring\_mode
  * **描述**: 攀爬梯子时的不准确度
* **inaccuracy\_fire**
  * **类型**: cfiring\_mode
  * **描述**: 射击时的不准确度
* **inaccuracy\_move**
  * **类型**: cfiring\_mode
  * **描述**: 移动时的不准确度
* **recoil\_angle**
  * **类型**: cfiring\_mode
  * **描述**: 射击时的后坐力角度
* **recoil\_angle\_variance**
  * **类型**: cfiring\_mode
  * **描述**: 后坐力角度的偏差
* **recoil\_magnitude**
  * **类型**: cfiring\_mode
  * **描述**: 射击时的后坐力大小
* **recoil\_magnitude\_variance**
  * **类型**: cfiring\_mode
  * **描述**: 后坐力大小的偏差
* **tracer\_frequency**
  * **类型**: cfiring\_mode
  * **描述**: 射击时可见曳光弹的频率
* **inaccuracy\_jump\_initial**
  * **类型**: float
  * **描述**: 刚跳跃时的初始不准确度
* **inaccuracy\_jump\_apex**
  * **类型**: float
  * **描述**: 跳跃顶点时的不准确度
* **inaccuracy\_reload**
  * **类型**: float
  * **描述**: 重新装弹后的不准确度
* **recoil\_seed**
  * **类型**: int
  * **描述**: 用于确定后坐力模式的种子值
* **spread\_seed**
  * **类型**: int
  * **描述**: 用于确定武器散布的种子值
* **time\_to\_idle\_after\_fire**
  * **类型**: float
  * **描述**: 射击后武器恢复到空闲状态所需的时间
* **idle\_interval**
  * **类型**: float
  * **描述**: 武器空闲动画之间的时间间隔
* **attack\_movespeed\_factor**
  * **类型**: float
  * **描述**: 使用此武器攻击时玩家移动速度的减少因子
* **heat\_per\_shot**
  * **类型**: float
  * **描述**: 每次射击产生的热量
* **inaccuracy\_pitch\_shift**
  * **类型**: float
  * **描述**: 射击时由于不准确度引起的俯仰偏移
* **inaccuracy\_alt\_sound\_threshold**
  * **类型**: float
  * **描述**: 触发替代声音的不准确度阈值
* **bot\_audible\_range**
  * **类型**: float
  * **描述**: 机器人能听到此武器射击的距离
* **use\_radio\_subtitle**
  * **类型**: string
  * **描述**: 武器动作是否使用无线电字幕
* **unzooms\_after\_shot**
  * **类型**: bool
  * **描述**: 射击后武器是否自动取消缩放
* **hide\_view\_model\_when\_zoomed**
  * **类型**: bool
  * **描述**: 缩放时是否隐藏视图模型
* **zoom\_levels**
  * **类型**: int
  * **描述**: 武器可用的缩放级别数量
* **zoom\_fov1**
  * **类型**: int
  * **描述**: 第一级缩放的视野 (FOV)
* **zoom\_fov2**
  * **类型**: int
  * **描述**: 第二级缩放的视野 (FOV)
* **zoom\_time0**
  * **类型**: float
  * **描述**: 初始缩放状态的过渡时间
* **zoom\_time1**
  * **类型**: float
  * **描述**: 第一级缩放的过渡时间
* **zoom\_time2**
  * **类型**: float
  * **描述**: 第二级缩放的过渡时间
* **iron\_sight\_pull\_up\_speed**
  * **类型**: float
  * **描述**: 拉起武器机械瞄具的速度
* **iron\_sight\_put\_down\_speed**
  * **类型**: float
  * **描述**: 放下武器机械瞄具的速度
* **iron\_sight\_fov**
  * **类型**: float
  * **描述**: 使用机械瞄具瞄准时的视野 (FOV)
* **iron\_sight\_pivot\_forward**
  * **类型**: float
  * **描述**: 机械瞄具前倾点
* **iron\_sight\_looseness**
  * **类型**: float
  * **描述**: 使用机械瞄具瞄准时的松散度
* **ang\_pivot\_angle**
  * **类型**: vector
  * **描述**: 机械瞄具的枢轴角度
* **vec\_iron\_sight\_eye\_pos**
  * **类型**: vector
  * **描述**: 使用机械瞄具瞄准时的眼睛位置
* **damage**
  * **类型**: int
  * **描述**: 武器的基础伤害
* **headshot\_multiplier**
  * **类型**: float
  * **描述**: 头部命中伤害倍率
* **armor\_ratio**
  * **类型**: float
  * **描述**: 穿透装甲的伤害比例
* **penetration**
  * **类型**: float
  * **描述**: 武器穿透材料的能力
* **range**
  * **类型**: float
  * **描述**: 武器的有效射程
* **range\_modifier**
  * **类型**: float
  * **描述**: 根据射程调整的伤害倍率
* **flinch\_velocity\_modifier\_large**
  * **类型**: float
  * **描述**: 大幅度闪避时的速度修正
* **flinch\_velocity\_modifier\_small**
  * **类型**: float
  * **描述**: 小幅度闪避时的速度修正
* **recovery\_time\_crouch**
  * **类型**: float
  * **描述**: 蹲伏时精度恢复时间
* **recovery\_time\_stand**
  * **类型**: float
  * **描述**: 站立时精度恢复时间
* **recovery\_time\_crouch\_final**
  * **类型**: float
  * **描述**: 蹲伏时最终精度恢复时间
* **recovery\_time\_stand\_final**
  * **类型**: float
  * **描述**: 站立时最终精度恢复时间
* **recovery\_transition\_start\_bullet**
  * **类型**: int
  * **描述**: 精度恢复过渡的起始子弹数
* **recovery\_transition\_end\_bullet**
  * **类型**: int
  * **描述**: 精度恢复过渡的结束子弹数
* **throw\_velocity**
  * **类型**: float
  * **描述**: 投掷物品（如手榴弹）的速度
* **v\_smoke\_color**
  * **类型**: vector
  * **描述**: 武器烟雾效果的颜色
* **anim\_class**
  * **类型**: string
  * **描述**: 与此武器关联的动画类

***

苏黎世银云安全 ©
