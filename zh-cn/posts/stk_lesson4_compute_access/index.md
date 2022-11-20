# 【STK11官方Tutorial学习笔记】Lesson4：计算访问


# Lesson 4 Compute Access

对应官方文档：[STK - Compute Access (agi.com)](https://help.agi.com/stk/11.6.1/index.htm#training/StartAccess.htm%3FTocPath%3DTraining%7CLevel%25201%2520-%2520Beginner%2520Training%7C_____4)

本节讲述如何计算两个对象之间的访问 (Access)。该访问将会保存两个对象可以连通时相关的记录。比如空间站途径地面站上空时，两个站点处于连通状态，超过一定范围，连通就会断开。

{{< bilibili id=BV1Zo4y1d7Jc p=4 >}}

## 创建访问

点击 STK 工具栏 (STK Tools) 中的 Access 按钮。

![](/img/STK_Tutorial/Lesson4/01.png)

或者点击 Analysis>Access。

![](/img/STK_Tutorial/Lesson4/02.png)

在弹出的窗口上方选择访问起点。这里以 Bloomington 的传感器为访问起点。点击 Select Object>Bloomington>Sensor1>OK。

![](/img/STK_Tutorial/Lesson4/03.png)

在下方选择访问终点。点击 Compute 进行计算。也可以同时选择多个对象作为终点，这时需要按住 Ctrl 再用鼠标左键进行选择。

![](/img/STK_Tutorial/Lesson4/04.png)

## 查看访问计算结果

点击 Access 窗口中 Reports 部分的 Access... 按钮查看计算报告。

![](/img/STK_Tutorial/Lesson4/05.png)

报告中显示了地面传感器探测到卫星的次数和时间。

![](/img/STK_Tutorial/Lesson4/06.png)

该报告也是交互式的。比如，鼠标右键某一时间，点击 Start Time>Set Animation Time，将该时间设定为当前动画的时间。

![](/img/STK_Tutorial/Lesson4/07.png)

这样，在地图上就能看到空间站正在穿越传感器的探测范围。

![](/img/STK_Tutorial/Lesson4/08.png)

为了使观测更加方便，我们可以先把视角聚焦 (Zoom to) 到地面位置，然后通过鼠标滚轮缩放到合适大小。按住鼠标左键移动鼠标调整视角。然后通过动画栏控制动画播放，进行观察。

## 保存报告快照

在报告窗口中，点击 Save as quick report，保存报告快照。

![](/img/STK_Tutorial/Lesson4/09.png)

点击上方数据栏 (data provider) 中的 报告快照管理器 (Quick Report Manager) 快速查看保存的快照。(Access 是高才保存快照的名称)。

![](/img/STK_Tutorial/Lesson4/10.png)

## 查看 AER 报告

在 Access 窗口中点击 AER。

![](/img/STK_Tutorial/Lesson4/11.png)

点击后，弹出 AER 报告的详细信息。该报告中记录了空间站相对于地面传感器的方位角 (Azimuth)、俯仰角 (Elevation) 和 距离 (Range) 信息。

![](/img/STK_Tutorial/Lesson4/12.png)

上方的 Step 是每次记录的间隔时间。

![](/img/STK_Tutorial/Lesson4/13.png)

点击 Show Step Value，可以看到本次报告以 60 s 为记录的时间间隔。Step 可以手动进行调整，调整后按下回车，下方报告会根据新的 Step 值而改变。

![](/img/STK_Tutorial/Lesson4/14.png)

## 存储视角

如果我们总是需要用到一些固定的视角，但是又不想每次观看该视角都要对地图进行重新调整。可以使用存储视角的功能。

首先，在地图上调整好想要保存的视角。点击上方的 Stored Views 按钮。

![](/img/STK_Tutorial/Lesson4/15.png)

在弹出的窗口中点击 New 以新建视角。

![](/img/STK_Tutorial/Lesson4/16.png)

双击新视角的 View Name 栏，重命名该视角。如本例将该视角命名为 AccessIntervals。点击 OK 保存。

![](/img/STK_Tutorial/Lesson4/17.png)

下次使用时，点击 Store Views 右侧的黑箭头，就会展开已保存的视角。点击视角名称以快速返回对应视角。

![](/img/STK_Tutorial/Lesson4/18.png)

## 连通时间在时间线视图的展示

如果我们想要对地面站能够探测到天空站的时间有一个更感性的认知，可以在时间线视角添加访问连通的时间。在计算访问后，该时间会自动加入时间线视图中。如下图所示，红框框出的轨道中，橙色的部分即为连通时间。

![](/img/STK_Tutorial/Lesson4/19.png)

如果该轨道没有自动显示，也可以手动对其进行添加。
点击 Add Time Componets。

![](/img/STK_Tutorial/Lesson4/20.png)

在弹出的窗口中选中刚才计算出的访问，右侧点击 AccessIntervals。点击 OK 插入。

![](/img/STK_Tutorial/Lesson4/21.png)

## 报告自动更新

当访问两端的对象属性进行更改后，访问的计算结果可以自动更新。
以上述地面站和空间站之间的访问为例。调整地面传感器的探测范围为 1500 km。

![](/img/STK_Tutorial/Lesson4/22.png)

调整后，可以看到下方的时间线视图进行了自动更新。(橙色的连通时间变窄了，因为探测范围变小了）

对于之前计算得出的报告，也会自动进行更新。也可以点击更新 (Refresh) 按钮以获得最新的计算结果。

![](/img/STK_Tutorial/Lesson4/23.png)


