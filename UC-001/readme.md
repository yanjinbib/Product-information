# 一、产品说明

变色龙Ultra 源自开源项目Chameleon Ultra。主要用途是**复制**、**分析**、**模拟** 125kHz 和 13.56MHz 的 NFC 卡片。通过一个设备，最多可以同时模拟 8 张 IC卡、8 张 ID 卡，共 16 张卡片。

项目地址：https://github.com/RfidResearchGroup/ChameleonUltra/

## 主要功能

| 功能    | 介绍                               |
|:-----:|:--------------------------------:|
| id卡读写 | 读取写入ID卡数据                        |
| IC卡读写 | 读取写入IC卡数据                        |
| 侦测密钥  | 解密三代全加密卡                         |
| 储存卡片  | 可最多保存8张IC卡，8张ID卡；休眠状态下直接在门禁处刷卡开门 |

## 使用场景

场景1：我们多个门禁卡，将这些门禁卡保存到变色龙中，下次直接用变色龙开门

场景2：朋友来我的小区开门禁不方便，我复制一张新卡给他

场景3：手机手环无法复制加密门禁卡，通过变色龙解密数据，再把数据写入到手机或手环中

# 二、配套软件下载

下载地址：https://www.jianguoyun.com/p/DbHzgscQhOKNDRjN_OUFIAA

IOS 和 Mac 客户端请在应用商店搜索 Chameleon Ultra GUI 下载

**连接教程**

<iframe src="//player.bilibili.com/player.html?bvid=BV1cGC3Y2Ebj&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>

# 三、读卡

目前卡片类型主要有ID卡，IC卡，CPU卡。CPU卡无法破解，市场占有率比较低，此处不做讨论。

先判断自己卡片是什么类型，可以用变色龙读取试试，高频能读到就是IC卡，低频能读到就是ID卡。注意读高频使用正面贴近卡片，读低频使用背面贴近卡片，两面板子对应不同的频率。

## 1. ID卡读取

<iframe src="//player.bilibili.com/player.html?bvid=BV1PKC3YDE3H&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>

## 2. IC卡读取

**非加密IC卡读取（读取失败移步到下一个视频）**

<iframe src="//player.bilibili.com/player.html?bvid=BV1wuC3YUE2b&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>

**半加密IC卡读取（读取失败移步到下一个视频）**

<iframe src="//player.bilibili.com/player.html?bvid=BV1wuC3YUE2b&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>

**全加密IC卡侦测**

<iframe src="//player.bilibili.com/player.html?bvid=BV1jCCGY5E1r&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>

# 四、写数据到变色龙

1. 在软件中点击想要保存的卡槽
2. 选择之前读卡时保存的卡片
3. 写入到卡槽中即可

# 五、写数据到空白卡

1. 准备一张空白卡贴近变色龙，IC 频率就用CUID卡，ID 频率就用ID5577卡
2. 在软件中选择写入卡片
3. 按提示完成操作

# 六、其他应用场景

## 一、写数据到手机或手环

1. 首先复制卡片到手机卡包中，仅复制卡号即可
2. 设置卡片为默认卡
3. 变色龙贴近手机背面，选择对应的卡包写入即可
