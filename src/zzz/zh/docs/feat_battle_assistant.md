---
lang: zh-CN
title: 功能-战斗助手
---

## 0.使用前需知

使用本页说明的功能时，建议阅读以下内容：
::: important
- 无特殊需求的话，所有位置自动战斗脚本均推荐使用 `全配队通用`
- 使用专属脚本前，请确定脚本的开发时间，是否为过时未维护的脚本
- 若你要自定义游戏按键，请在游戏内设置好按键后，在脚本的 `「设置」-「游戏设置」-「游戏按键」` 内进行同步修改。
:::

## 快速开始-自动战斗
目前结合了 画面识别 和 [声音识别](https://github.com/ImLaoBJie/ZZZSoundTrigger)  
如果觉得好用，欢迎给原项目点赞。  

### 战斗助手
自动战斗作用于一条龙的所有战斗场景，也可以在`「游戏助手」`中配合使用。

- **战斗配置** 脚本的操作逻辑，默认建议使用 `「全通用配置」`
- **GPU运算** 建议启用
- **截图间隔** 能正常使用就不要修改
- **手柄类型** 按需设置（需安装[手柄驱动]()） tip：手柄目前仅适配了战斗相关功能

### 闪避助手
~~**有全自动战斗真的有人半自动吗**~~  
主要用于帮助大家日常过剧情、活动、深渊时，可以辅助闪避，降低游戏难度。  

- **闪避方式** 按需选择，名字都挺好理解的
- **GPU运算** 建议启用
- **截图间隔** 能正常使用就不要修改
- **手柄类型** 按需设置（需安装[手柄驱动]()）

## 战斗助手功能分类详解

|  功能   | 说明  |
|  ----  | ----  |
| [闪避助手](#_1-闪避助手) | 自动闪避\闪A\弹反 |
| [自动战斗]() | 哈?你问我这是干什么的? |
| [指令调试]() | 单指令循环执行测试工具 |
| [配置信息]() | 用于查看战斗脚本相关信息 |

## 1.闪避助手

### 1.1.配置内容
1. 闪避方式 - 开启后脚本会自动检测游戏画面中的闪避光，请按照下文`「配置文件」`进行配置。
1. GPU运算 - 开启后脚本会使用 GPU 进行画面识别，通常可以提高识别速度和准确率，但可能会导致部分显卡驱动不稳定。
1. 截图间隔 - 闪避检测的截图间隔，默认 0.02 秒。
1. 手柄类型 - 选择手柄类型，目前支持`Xbox`和`DS4`（见 [手柄支持](feat_gamepad.md)）。

### 1.2.闪避方式配置文件

|配置文件|作用|
|---|---|
|本-格挡|`本·比格` 专用，使用特殊攻击进行格挡|
|闪避|闪避后切普通攻击|
|切换角色-下一个|黄光切换下一个角色后进行普通攻击；红光闪避切普通攻击|
|切换角色-强攻|黄光切换强攻角色后进行普通攻击；红光闪避切普通攻击|
|闪A切下一个|黄光闪避后普通攻击，切换到下一个角色；红光闪避切普通攻击|
|闪A切强攻|黄光闪避后普通攻击，切换到强攻角色；红光闪避切普通攻击|

## 2.自动战斗

自动战斗作用于一条龙的所有战斗场景，也可以在`「战斗助手」`中单独使用。

### 2.1.配置内容

1. 配队选择：根据配队类型分别为`全配对通用/专属配队/战斗逻辑配队`。
    - 全配队通用 - 适用于大部分角色的通用配置，对队伍搭配没有要求。
    - 专属配队 - 适用于特定角色队伍的专属配置，对队伍的要求可在`「战斗助手」-「配置信息」`中查看。
    - 战斗逻辑配队 - 适用于特定战斗逻辑的配置。
2. F12调试：用于检查当前配置是否生效，自动战斗能否正常运行。
3. 配置共享：为网友自发上传，可自行下载使用，在此诚挚感谢各位网友的贡献。

## 3.指令调试

指令调试主要用于查看当前指令的执行情况，方便用户检测战斗模块运行状况，了解脚本的执行逻辑。

### 3.1.配置内容

1. 指令调试 - 开启后脚本会在`「战斗助手」`中显示当前指令的执行情况。
1. 循环指令 - 用于检测战斗指令的连贯性。
1. 手柄支持 - 选择手柄类型，目前支持`Xbox`和`DS4`（见 [手柄支持](feat_gamepad.md)）。

## 4.配置信息

配置信息用于查看当前脚本的自动战斗配置信息，包括基础信息与适用配队

### 4.1.使用说明

点击`选择已有`即可查看当前配队的配置信息，点击取消则可继续查看下一配队。

- 基础信息 - 显示所选战斗脚本的基础信息，包括作者，版本号，简介。
- 适用配队 - 显示所选战斗脚本适用的配队信息。

## 5.反馈或开发

### 5.1.漏判误判反馈

相关情况可以到 [这里](https://github.com/OneDragon-Anything/ZenlessZoneZero-OneDragon/issues/new?assignees=&labels=bug&projects=&template=02-bug-dodge-assistant.yml&title=%5B%E9%97%AE%E9%A2%98%E5%8F%8D%E9%A6%88%5D+%5B%E9%97%AA%E9%81%BF%E5%8A%A9%E6%89%8B%5D+) 反馈。

请注明副本方便作者复现，并使用脚本的`「开发工具」-「截图助手」`，截取有问题的游戏截图后打包发给作者，截图会保存在 `.debug/images` 中。

- 漏判 ( 出现了黄光/红光，但脚本没有识别到 ) : 可以在出现后使用手动按钮触发截图保存。
- 误判 ( 没有出现黄光/红光，但脚本误认为出现了，造成乱闪避 ) : 打开`「闪避检测」`，脚本会自动把认为有光的图保存下来。

### 5.2.闪避助手开发

闪避助手的配置文件，放置在 `config/dodge` 文件夹下。

|配置文件|作用|
|---|---|
|本-格挡.sample.yml|`本·比格` 专用，使用 `特殊攻击` 进行格挡|
|闪避.sample.yml|闪避之后进行一次普通攻击|
|切换角色-下一个.sample.yml|黄光时切换到`下一个`角色后进行一次普通攻击；红光时闪避之后进行一次普通攻击|
|切换角色-强攻.sample.yml|黄光时切换到`强攻`角色后进行一次普通攻击；红光时闪避之后进行一次普通攻击|
|闪A切下一个.sample.yml|黄光时闪避 -> 普通攻击 -> 切换到下一个角色 -> 普通攻击；红光时闪避之后进行一次普通攻击|
|闪A切强攻.sample.yml|黄光时闪避 -> 普通攻击 -> 切换到强攻角色 -> 普通攻击；红光时闪避之后进行一次普通攻击|

### 5.3.自动战斗开发

战斗助手底层都是指令的配置，可以参考以下文档编写适合自己配队的指令。
如果有自己修改了觉得好用的配置，欢迎提交PR。

- [朱鸢示例教程(新)(未完成)](../auto_battle_guide/zhu_yuan/zhu_yuan_01.md)
- [自定义指令基础(新)(未完成)](../auto_battle_guide/basic/basic_00_yaml.md)
- [自定义指令介绍(旧)](./feat_custom_op.md)