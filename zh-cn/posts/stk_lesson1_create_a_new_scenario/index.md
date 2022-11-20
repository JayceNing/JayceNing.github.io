# 【STK11官方Tutorial学习笔记】Lesson1：创建新场景


# Lesson 1 Create A New Scenario

对应官方文档：[STK - Model Complex Systems (agi.com)](https://help.agi.com/stk/11.6.1/index.htm#training/StartBuildScenarios.htm%3FTocPath%3DTraining%7CLevel%25201%2520-%2520Beginner%2520Training%7C_____1)

本节讲述如何在 STK 中创建一个新场景。该概念类似于 Adobe 系列软件的工程文件。

{{< bilibili id=BV1Zo4y1d7Jc p=1 >}}

## 创建新场景 (Scenario)

双击STK桌面图标，打开软件后可看到如下窗口。我们可以从中选择创建新场景、打开已有场景或查看使用教程及帮助等。

![](/img/STK_Tutorial/Lesson1/01.png)

点击创建新场景，此时会弹出新的方案向导。

![](/img/STK_Tutorial/Lesson1/02.png)

* 输入该场景的名称，并做出一些有意义相关描述。以便下次使用时，能够快速找到并回忆起该场景的功能。
* 接下来选择保存场景的目录，默认目录与安装时的选项保持一致。通常在C盘的Documents文件夹当中。
* 选择场景的起始时间。
* 创建场景。

![](/img/STK_Tutorial/Lesson1/03.png)

成功后得到的界面如下图所示。

![](/img/STK_Tutorial/Lesson1/04.png)

## 工作区的简单操作

首先关掉 Inset STK Objects 窗口，这个功能会在之后用到。

最大化软件窗口。红框标记出的区域被称为集成工作区 (Integrated Workspace)，后文中简称为工作区。工作区用于展示我们用到的功能窗口 (window)。下图中就有3D和2D地图两个工作窗口。

![](/img/STK_Tutorial/Lesson1/05.png)

点击上方菜单栏 (Menu bar) 中的 Window>Tile Vertically 用以平铺窗口。除此之外，也可以选择垂直平铺窗口 (Tile Horizontally)。

![](/img/STK_Tutorial/Lesson1/06.png)

下方的选项卡 (Tab) 栏会显示当前工作区中存在的窗口。

![](/img/STK_Tutorial/Lesson1/07.png)

## 保存场景

点击菜单栏中的 File 按钮，选择 Save as

![](/img/STK_Tutorial/Lesson1/08.png)

可以看到 STK 已经自动在创建新场景时设置的“保存场景的目录”下，创建了一个与当前场景名称相同的文件夹。单击保存，将场景保存在该文件夹下。

![](/img/STK_Tutorial/Lesson1/09.png)

保存后会得到如下所示的文件。

![](/img/STK_Tutorial/Lesson1/10.png)

当前场景中的任何窗口和插入的物体等都会被保存。所以在进行新的任务场景的开发时，最好选择新建新的场景 （也就是新建一个文件夹），以免之前场景中的相应文件被覆盖掉。

## 熟悉地图控制

在2D地图窗口中，按住鼠标左键左右移动以移动地图。

![](/img/STK_Tutorial/Lesson1/11.png)

使用鼠标滚轮上滑或放大镜 (zoom in) 来放大地图。使用放大镜时，框选出指定放大的地点。同样地，使用鼠标滚轮下滑或 zoom out 按钮可以缩小地图。

![](/img/STK_Tutorial/Lesson1/12.png)

在3D地图中，同样可以按住鼠标左键移动以旋转地球仪。

![](/img/STK_Tutorial/Lesson1/13.png)

使用鼠标滚轮缩放地球仪。除此之外还可以按住鼠标右键上下移动以缩放地球仪。

![](/img/STK_Tutorial/Lesson1/14.png)

使用放大镜将视角固定在某一区域。放大后，左键功能将与之前不同，按住左键移动鼠标将围绕该区域进行旋转。如果还想使用之前平移功能，需要按住鼠标左键的同时，按住shift健。

![](/img/STK_Tutorial/Lesson1/15.png)

使用 Home View 按钮恢复最原始的视图。

![](/img/STK_Tutorial/Lesson1/16.png)

## 熟悉动画控制

使用动画栏 (Animation) 中的播放按钮，地球会按照创建场景时设置的开始时间为起点进行旋转。

![](/img/STK_Tutorial/Lesson1/17.png)

动画栏中的按钮依次为：重置 (Reset)、后退一帧 (Step in Reverse)、倒放 (Reverse)、暂停 (Pause)、播放 (start)、前进一帧 (Step forward)、减速 (Decrease Time Step) 和 加速 (Increase Time Step)。

使用下方的时间线视图 (Timeline View) 调整时间。拖住红框标记的按钮并移动以调整时间。

![](/img/STK_Tutorial/Lesson1/18.png)
