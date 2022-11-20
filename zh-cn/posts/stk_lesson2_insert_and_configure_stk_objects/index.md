# 【STK11官方Tutorial学习笔记】Lesson2：插入并配置STK对象


# Lesson 2 Insert And Configure STK Objects

对应文档：[STK - Insert STK Objects (agi.com)](https://help.agi.com/stk/11.6.1/index.htm#training/StartInsertObjects.htm%3FTocPath%3DTraining%7CLevel%25201%2520-%2520Beginner%2520Training%7C_____2)

本节讲述如何插入并配置一些典型的 STK 对象。

{{< bilibili id=BV1Zo4y1d7Jc p=2 >}}

## 插入地面对象

点击上方菜单栏 Insert>New

![](/img/STK_Tutorial/Lesson2/01.png)

可选择的地面站点如：设施 (Facility)、地点 (Place) 和 目标 (Target)。

![](/img/STK_Tutorial/Lesson2/02.png)

### 插入地点
#### 使用本地数据库方式导入

这里以 Place为例。首先选择左侧的 Place，右边的导入方法选择 From City Database。点击下方 Insert进行插入。

![](/img/STK_Tutorial/Lesson2/03.png)

在新弹出的窗口中输入城市名称，点击 search 进行搜索。

![](/img/STK_Tutorial/Lesson2/04.png)

右侧空白位置会显示搜索结果。选择想要的结果，点击 Insert。

![](/img/STK_Tutorial/Lesson2/05.png)

插入成功后，在左侧对象浏览器 (Object Browser) 会显示当前场景中的物体。同时，地图上也会标记出该处地点。

![](/img/STK_Tutorial/Lesson2/06.png)

#### 联网导入

如果当前设备处于联网状态，在插入 STK 对象时，插入方法可以选择 Search by Address，进行联网导入。

![](/img/STK_Tutorial/Lesson2/07.png)

点击 Insert 后，弹出 Insert by Address 窗口。在上方搜索栏中输入你想要查找的地点。比如本例查找 white house，下方则会返回联网搜索到的结果。选择你想要的结果，点击 Insert Place(s) 进行插入。

![](/img/STK_Tutorial/Lesson2/08.png)

同样地，地图上会显示插入地点的标记。

![](/img/STK_Tutorial/Lesson2/09.png)

### 插入设施
在插入 STK 目标时，选择 Facility>From Standard Object Database。点击 Insert 进行插入。

![](/img/STK_Tutorial/Lesson2/10.png)

AGI 拥有一个地面设施的数据库。在安装 STK 时，该数据库已经安装至本地。除此之外，也可以选择联网搜索。

在新弹出的窗口中，向 Name 栏输入想要搜索设施的名称，点击下方 Search，右侧将返回搜索结果。结果将包含该设施的相关信息，包括该条结果的数据来源 (本地数据库或联网数据)。

单击你想要的数据，点击下方 Insert。

![](/img/STK_Tutorial/Lesson2/11.png)

地图中将会显示插入的结果。

![](/img/STK_Tutorial/Lesson2/12.png)

### 对象聚焦

STK 可以帮助我们快速放大到某一对象所在的地图位置。在对象浏览器中，右键你想要聚焦的对象，点击 Zoom To。

![](/img/STK_Tutorial/Lesson2/13.png)

***注意：这里可能遇到地图没有加载出来的问题如下图所示***

![](/img/STK_Tutorial/Lesson2/14.png)

我这边是网络问题所致。开一下梯子，重新进一下软件就好了。

![](/img/STK_Tutorial/Lesson2/15.png)

由于当前时间 Bloomington 是黑天，所以显示看起来比较黑。

## 插入卫星
### 从数据库导入

菜单栏选择 Insert>New。在弹出的窗口中选择 Satellite>From Standard Object Database>Insert。

![](/img/STK_Tutorial/Lesson2/16.png)

AGI 每天会更新两次卫星数据库。点击菜单栏 Utilities>Data Update 以更新数据。

在弹出的窗口中，依次输入卫星名称，点击搜索，选择你想要的卫星，最后点击插入。如本例搜索名为 geoeye 的卫星。

![](/img/STK_Tutorial/Lesson2/17.png)

接着，搜索 ISS 空间站。该项有很多搜索结果，我想选择编号为25544的结果。点击 Space Surveillance Catalog Number，对结果进行升序排序。选择编号为25544的卫星。(任意一个)

![](/img/STK_Tutorial/Lesson2/18.png)

导入后，在对象浏览器和地图中都能看到结果。

![](/img/STK_Tutorial/Lesson2/19.png)

### 从轨道向导中导入

菜单栏选择 Insert>New。在弹出的窗口中选择 Satellite>Orbit Wizard>Insert。

![](/img/STK_Tutorial/Lesson2/20.png)

使用该工具可以自定义设计卫星运行轨道。

在该向导中，可以选择卫星类型，设置卫星名称，定义卫星的倾角 (Inclination)、海拔 (Altitude) 和 升交点 (RAAN)。点击OK进行导入。

![](/img/STK_Tutorial/Lesson2/21.png)

### 对象聚焦及动画演示

与地面聚焦的方式相同，在对象浏览器中，右键卫星对象，点击 Zoom to。

![](/img/STK_Tutorial/Lesson2/22.png)

此时，地图视野聚焦到空间站位置。可通过 Lesson 1 中介绍的地图控制方法调整目标的视角。

![](/img/STK_Tutorial/Lesson2/23.png)

通过动画栏中的播放按钮开始动画。此时，镜头会跟随被聚焦的空间站进行运动。

![](/img/STK_Tutorial/Lesson2/24.png)

## 插入飞机航线
### 插入默认航线

菜单栏点击 Insert>New。弹出窗口中依次点击 Aircraft>Insert Default>Insert。

![](/img/STK_Tutorial/Lesson2/25.png)

点击后，对象浏览器会新增刚插入的飞机。

为编辑航线，首先点击 3D 地图窗口，使该窗口处于激活状态。然后从上方的对象编辑器中选择刚添加的飞机。点击选项框左侧黄色箱子按钮 (Object Edit Start)，开始编辑航线。

![](/img/STK_Tutorial/Lesson2/26.png)

在地图中放大你想要添加航线的位置。按住 Shift 和鼠标左键以添加节点。

航线编辑操作可分为三类：

* 添加 (Add)：按住 Shift 点击鼠标左键。
* 调整 (Modify)：使用鼠标左键按住并移动需要调整的节点。
* 删除 (Remove)：按住 Shift，鼠标左键点击需要删除的节点。

![](/img/STK_Tutorial/Lesson2/27.png)

点击对象编辑栏的绿色按钮 (Object Edit Accept) 以保存更改，或者红色按钮 (Object Edit Cancel) 以取消更改。

![](/img/STK_Tutorial/Lesson2/28.png)

## 插入导弹
### 定义导弹属性

菜单栏点击 Insert>New。在弹出窗口中依次点击 Missile>Define Properties>Insert。

![](/img/STK_Tutorial/Lesson2/29.png)

在弹出的窗口中设置发射地点 (Launch) 的经纬度和海拔，以及攻击地点 (Impact) 的经纬度和海拔。比如本例默认发射点经纬度为0，攻击点的经纬度分别设置为-20。

![](/img/STK_Tutorial/Lesson2/30.png)

插入后，地图将显示导弹的轨迹。

![](/img/STK_Tutorial/Lesson2/31.png)

## 插入传感器

传感器 (sensor) 也被称作附件 (attached) 或者 子对象 (Subobject)。它被用于记录父对象的相关信息。本节中，将举例插入一个空中对象的传感器和一个地面对象的传感器。

### 插入默认传感器

点击菜单栏 Insert>New。在弹出的窗口中选择 Sensor>Insert Default>Insert。

![](/img/STK_Tutorial/Lesson2/32.png)

点击后，弹出对象选择窗口。选择 Bloomington 作为父对象，点击 OK 插入。

![](/img/STK_Tutorial/Lesson2/33.png)

插入成功后，对象浏览器中的地面地点 Bloomington 下会多出来一个传感器。

![](/img/STK_Tutorial/Lesson2/34.png)

同理，以 CircularSat 为父对象插入默认传感器。

## 时间线视图
在 Lesson1 中动画控制小节，我们简单接触到了时间线视图 (Timelin View)。现在，我们有了更多的对象，让我们将对象与其时间线结合起来。

如果软件下方没有显示时间线视图，首先点击菜单栏 View>Timeline View。

点击时间线视图中的 Add Time Components 以添加时间组件。

![](/img/STK_Tutorial/Lesson2/35.png)

这里以飞机航线为例。在弹出窗口中选择 Aircraft1>AvailabilityTimeSpan>OK。即选择飞机起飞到降落的这段时间。

![](/img/STK_Tutorial/Lesson2/36.png)

点击后，时间线视图中将会多出飞机时间线的轨道。

当前时间线视图的宽度，是我们创建场景时设定的起始时间。我们可以将宽度设定为某一对象的时间跨度，方便我们观察该对象在该段时间内的运动情况。如下图，右键飞机的时间线轨道，点击 Center。

![](/img/STK_Tutorial/Lesson2/37.png)

此时，时间线视图的时间跨度，将会以飞机对象为准。

![](/img/STK_Tutorial/Lesson2/38.png)

拖动时间线上的滑动按钮，以观察对象在这段时间的运动情况。

![](/img/STK_Tutorial/Lesson2/39.png)

为返回原始的时间线跨度，右击场景 (STK_Fundamentals Availability) 的时间线轨道，点击 Center。
