---
title: SDK描述文件(VRC Avatar Descriptor)简介
permalink: /archives/215.html
date: 2022-05-07 23:30:56
categories:
    - 其他教程
tags:
---

## 添加描述文件

在“层级”中选中模型名字即可在右方组件搜索添加“VRC Avatar Descriptor”

![img](https://jsd.cdn.zzko.cn/gh/yexca/picx-images-hosting@master/2022-VRChat/03-AvatarDescriptor/image.48d8ypvvpq00.webp)

第一个为VRC的描述，第二个为蓝图

## 一、View

![img](https://jsd.cdn.zzko.cn/gh/yexca/picx-images-hosting@master/2022-VRChat/03-AvatarDescriptor/image.3i0xx2om69e0.webp)

用于调整视角球，即在游戏中看到的位置，一般放在两眼中间

点击“Edit”即可在“场景”中调整位置，调整完成后点击“Return”

## 二、LipSync

定义后模型可在开麦说话时开口

![img](https://jsd.cdn.zzko.cn/gh/yexca/picx-images-hosting@master/2022-VRChat/03-AvatarDescriptor/image.40e4lutgnbi0.webp)

一般点击“Auto Detect!”可自动添加，如无法正常识别请手动添加

一般“Mode”为第四个“Viseme Blend Shape” ，然后将模型的“Body”或“Face”拖入“Face Mesh” ，一般情况如下(如识别不出请手动选择）

![img](https://jsd.cdn.zzko.cn/gh/yexca/picx-images-hosting@master/2022-VRChat/03-AvatarDescriptor/image.5mxy376p4sk0.webp)

若没有以上东西请禁用，即“Mode”选“默认”，或者自行研究骨骼实现

## 三、Eye Look

![img](https://jsd.cdn.zzko.cn/gh/yexca/picx-images-hosting@master/2022-VRChat/03-AvatarDescriptor/image.12j6dlfdgibk.webp)

眼部相关，点击“Enable”开始更改

### General

全局设定眼部移动

![img](https://jsd.cdn.zzko.cn/gh/yexca/picx-images-hosting@master/2022-VRChat/03-AvatarDescriptor/image.2nr8oejxht60.webp)

“Calm-Excited”影响眨眼的频率

“Shy-Confident”影响自己的模型看向其他玩家模型的频率以及看向其他玩家时视线停留的时间

### Eyes

#### Transforms

定义眼骨的位置

![img](https://jsd.cdn.zzko.cn/gh/yexca/picx-images-hosting@master/2022-VRChat/03-AvatarDescriptor/image.3fvueycbkhw0.webp)

找到相应骨骼拖入即可，如没有请跳过

#### Rotation States

定义眼部骨骼旋转的范围，只有当上一项填入眼骨才可用

![img](https://jsd.cdn.zzko.cn/gh/yexca/picx-images-hosting@master/2022-VRChat/03-AvatarDescriptor/image.5lbk2uslvks0.webp)

定义向前，上，下，左，右看时眼睛的移动

点击“Preview”可进行编辑，可以在场景中进行旋转，点击“X”轴左方的链子可分别定义左右眼，当调整好后点击“Return”保存

### Eyelids

定义闭眼，向上看和向下看

![img](https://jsd.cdn.zzko.cn/gh/yexca/picx-images-hosting@master/2022-VRChat/03-AvatarDescriptor/image.2ljvn9o52940.webp)

一般“Eyelid Type”选择“Blendshapes”，然后将“Body”或“Face”拖入“Eyelids Mesh”

在“Blendshapes”可定义闭眼与向上看和向下看

**注意：**此处向上看与向上看与上一项“Eyes-Rotation”中的向上看和向下看是相同的，若使用上方定义可选择“-none-”

游戏中眼部出现异常可在这个模块调整，图省事可直接“disable”

## Playable Layers

参考：[动画层 (Playable Layers) 简介](/archives/44)

## Lower Body

![img](https://jsd.cdn.zzko.cn/gh/yexca/picx-images-hosting@master/2022-VRChat/03-AvatarDescriptor/image.1mkbsgxttbuo.webp)

第一个：头部有轻微移动会有小碎步的效果

第二个：全身追踪时是否启用Locomotion

## Expressions

添加参考与官方数值：[动画层 (Playable Layers) 简介](/archives/44)

## Colliders

新SDK3特有，用于定义头部、身体、手脚的碰撞

![img](https://jsd.cdn.zzko.cn/gh/yexca/picx-images-hosting@master/2022-VRChat/03-AvatarDescriptor/image.775z0ziwkxc0.webp)

点击“Edit”即可定义位置与大小，可在场景中进行编辑

点击左方的链条即可分别设置左右位置

此处设置的不仅是碰撞体积也是交互系统发送端的大小

具体参考：[交互系统(Contacts)简介](/archives/172)