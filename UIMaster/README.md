UI Master是为了让游戏开发者更能专注于游戏内容本身而制作的一体式UI框架。
如果所有的游戏都有UI，那么不妨现将其做成“轮子”。
使用这个框架来省去诸如“UI设计”“设置系统”“成就系统”等工作吧！

## 操作准备

### 文本相关预设

1. 导入TMP Essentials：Edit > Project Setting > Text Mesh Pro > Import TMP Essentials。
    - 需要先安装TMP的预设。
2. 富文本设置：
    - 在Project Setting > TextMesh Pro > Settings中，将Default Sprite Asset替换为`SpriteAsset_Default`。
    - 将Default Style Sheet替换为`StyleSheet_Default`。
    - 将Default Font Asset替换为`NotoSansSC-Black SDF`文件。当然，后续可以根据项目需求替换为其他字体。

### 本地化相关预设

1. 在Package Manager中安装Localization本地化插件。
2. 在Project Setting > Localization中，将默认的本地化文件替换上去。

### 输入系统相关预设

1. 在Project Setting > Api Compatibility [Level中将替换为.NET](http://xn--level-9n1h5c952lqwojqi.net/) Framework。
2. 将Active Input Handling替换为Input System Package。
    - 我们使用新的控制系统来支持项目中的UI设置。
    - 在Package Manager中安装Input System。

### 渲染管线相关预设

1. 在Package Manager中安装Universal RP（通用渲染管线）。
2. 在Project Setting > URP Global Settings中，将已有的Rendering Asset资产拖拽进去。如果有问题，可以在该页面进行修复。
    - 这套方案会与URP绑定，所以需要适配。如果不使用URP，需要在SettingManager中将Value命名空间相关的代码注释或删除。

### 建议操作

1. 在Project Setting中，将Color Space改为Linear。这可能对游戏的美术效果有影响，为了确保最佳品质。

[UI Master官网](https://uimaster.vercel.app/)


#更新日志
时间：2024年11月29
版本：2.3
更新说明：
【重点】
1.将设置功能做的更加解耦，灵活。现在的设置功能不在需要数据、方法、实体三个东西站在一起，而是只在数据管理中创建对应方法的类就行。
