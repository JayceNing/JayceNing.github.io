# 【STK11官方Tutorial学习笔记】Lesson7：电影时间线


# Lesson 7 The Movie Timeline
对应官方文档：[STK - Share Your Work (agi.com)](https://help.agi.com/stk/11.6.1/index.htm#training/StartShareWork.htm%3FTocPath%3DTraining%7CLevel%25201%2520-%2520Beginner%2520Training%7C_____7)

本节介绍如何使用电影时间线向导 (Movie Timeline Wizard) 在 STK 中对场景进行录制。以空间站围绕地球运动为例。

{{< bilibili id=BV1Zo4y1d7Jc p=7 >}}

## 场景布置

首先，在对象浏览器中取消勾选多余的对象，仅留下 Bloomington 地面站 和 ZARYA 空间站。

![](/img/STK_Tutorial/Lesson7/01.png)

聚焦 (Zoom to) 于空间站，调整到合适的视角。使 3D 地图面向空间站前进的方向，运动轨迹的拐点清晰可见。

![](/img/STK_Tutorial/Lesson7/02.png)

保存该视角。将其命名为 MovieView。

![](/img/STK_Tutorial/Lesson7/03.png)

![](/img/STK_Tutorial/Lesson7/04.png)

## 打开电影时间线工具栏

点击菜单栏中的 View>Toolbars>Movie Timeline。在上方显示电影时间线工具栏。

![](/img/STK_Tutorial/Lesson7/05.png)

显示成功后，电影时间线工具栏如下图所示。

![](/img/STK_Tutorial/Lesson7/06.png)

## 开启电影向导

点击电影时间线工具栏中的录制按钮 (Record from the Movie Timeline)。

![](/img/STK_Tutorial/Lesson7/07.png)

### 文件名及格式

在弹出的电影向导中，首先选择下方的录制格式。本例中选择录制格式为 WMV。

接下来，点击上方的 Save as 选择存储位置。

![](/img/STK_Tutorial/Lesson7/08.png)

本例将录制结果存于 STK_Fundamentals 文件夹，文件名设置为 Movie.wmv。设置完成后，点击 Next 来到下一步。

![](/img/STK_Tutorial/Lesson7/09.png)

### 录制窗口

本步骤选择录制的窗口。我们选择 3D 窗口进行录制。单击 Next。

![](/img/STK_Tutorial/Lesson7/10.png)

### 分辨率

此步骤选择录制的分辨率。点击预设栏 (Preset) 选择分辨率，本例选择 720P。

![](/img/STK_Tutorial/Lesson7/11.png)

选择后，3D 窗口会自动调整其大小。如图所示，该窗口比选择之前变得更宽了。

确保该分辨率没有问题后，点击 Next。

![](/img/STK_Tutorial/Lesson7/12.png)

### 相机视角
接下来，选择相机的视角。可以录制当前的视角或者保存的视角。我们选择之前保存的 MovieView 视角 (这里有一点挡住了，不过还是可以看得出来第二个是 Movie View)。点击 Next。

![](/img/STK_Tutorial/Lesson7/13.png)

### 时间和时长

本步骤中，设置录制的时间范围，和录制影片的时长。

首先选择录制的时间范围，该时间范围对应场景当中的时间。本例中，选择开始时间到其之后的 10 分钟内为录制的时间范围。因此，将 End Time 设定为 Start time 之后的十分钟 (这里 Start time 的开始日期被挡住了，因为本例中开始日期是 11 日，所以 End Time 要修改日期为11)。

![](/img/STK_Tutorial/Lesson7/14.png)

接下来，设置录制视频的时长。本例中，设定录制视频时长为 5 秒，在右侧电影回放时长栏 (Movie playback length) 输入 5 sec。鼠标点击左侧步长 (Step size) 输入框，其值会根据录制时长自动调整。

![](/img/STK_Tutorial/Lesson7/15.png)

点击预览 (Preview speed) 按钮，3D 地图中将按当前设置播放预览视频，方便对速度进行调整。

![](/img/STK_Tutorial/Lesson7/16.png)

### 大小和质量

本步骤用于设置生成视频的大小和质量。

下图中四个红框代表：

* 抗锯齿 (Anti-aliasing)：本例选择默认抗锯齿。
* 运动模糊 (Motion blur)：该项默认不勾选。本例中勾选。(勾选框被挡住了一大半，还好露出来一点点可以勾选)。
* 离屏渲染 (Off-screen render)：该项默认勾选。(幸好是默认的，要不这块被挡住了还选不上）
* 质量 (Quality)：本例选择高质量 (High)。

点击 Next。

![](/img/STK_Tutorial/Lesson7/17.png)

### 录制

本步骤中，右侧显示录制信息总结。确认没有问题后，点击下方开始录制 (Begin Record) 按钮以生成视频。

![](/img/STK_Tutorial/Lesson7/18.png)

录制过程比较慢，需要耐心等待一会。

![](/img/STK_Tutorial/Lesson7/19.png)

导出成功。

![](/img/STK_Tutorial/Lesson7/20.png)

访问 [agi.com/resources](agi.com/resources) 以获取更多的电影教程。

