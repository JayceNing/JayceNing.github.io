# 【STK11官方Tutorial学习笔记】Lesson8：方向-俯仰角遮罩工具


# Lesson 9 AzEI Mask Tool
对应官方文档：[STK - Create an AzEl Mask from a 3D Model (agi.com)](https://help.agi.com/stk/11.6.1/index.htm#training/StartSensorAzEl.htm%3FTocPath%3DTraining%7CLevel%25202%2520-%2520Advanced%2520Training%7C_____2)

本节课将讨论如何使用 STK 的 AzEI 遮罩工具。

{{< bilibili id=BV1Zo4y1d7Jc p=10 >}}

## 创建新场景

打开 STK 软件，点击创建新场景。

![](/img/STK_Tutorial/Lesson9/01.png)

将新场景命名为 STK_SensorAzEIMasking。

保持场景默认的开始时间不变，结束时间修改为 1 秒之后。(+1sec)
点击 OK。

![](/img/STK_Tutorial/Lesson9/02.png)

先将新场景保存一下。

点击工具栏中的保存按钮。

![](/img/STK_Tutorial/Lesson9/03.png)

将场景保存在场景名称命名的目录下。在弹出窗口中直接点击保存即可。

![](/img/STK_Tutorial/Lesson9/04.png)

为了方便接下来的观察，我们关掉时间线视图，并将 3D 地图窗口最大化。

![](/img/STK_Tutorial/Lesson9/05.png)

## 为场景添加地形

在对象浏览器中右击场景，点击属性。

![](/img/STK_Tutorial/Lesson9/06.png)

### 禁用地形服务器

点击 Basic>Terrain。勾选掉 Use terrain server for analysis 的选项。点击OK。

![](/img/STK_Tutorial/Lesson9/07.png)

### 导入本地地形

点击 3D 地图工具栏中的地球管理器 (Globe Manager)。

![](/img/STK_Tutorial/Lesson9/08.png)

在左侧弹出的地球管理器中，点击 Add Terrain/Imagery。

![](/img/STK_Tutorial/Lesson9/09.png)

点击右侧的 ... 打开地形文件所在文件夹。

* 该文件夹位于 <STK 的安装路径>\AGI\STK 11\Data\Resources\stktraining\imagery
* 比如我的位于 D:\Program Files\AGI\STK 11\Data\Resources\stktraining\imagery

选中 StHelens_Training.pdtt 文件。

点击 Add。

![](/img/STK_Tutorial/Lesson9/10.png)

弹出提示窗口：是否想使用此地形用于分析。点击 Yes 即可。

![](/img/STK_Tutorial/Lesson9/11.png)

在地球管理器中，右击导入的地形，点击 Zoom to 以聚焦到地形所在位置。

在 3D 地图中调整合适的视角。

![](/img/STK_Tutorial/Lesson9/12.png)

## 插入地面站

点击菜单栏 Insert>New。

![](/img/STK_Tutorial/Lesson9/13.png)

插入对象选择地点 (Place)，插入方式选择来自城市数据库 (From City Database)。

点击 Insert。

![](/img/STK_Tutorial/Lesson9/14.png)

在名称 (Name) 输入框中输入 morton。

点击搜索 (Search)。

在返回结果中找到位于华盛顿 (Washington) 的数据。

点击插入 (Insert)。

![](/img/STK_Tutorial/Lesson9/15.png)

### 确保 Morton 考虑到其地形影响

在对象浏览器中右击 Morton，点击属性。

![](/img/STK_Tutorial/Lesson9/16.png)

点击 Basic>Position。确保使用地形数据 (Use terrain data) 选项已勾选。修改距地距离 (Height Above Ground) 为 20 英尺 (20 ft)。

点击 Apply 应用修改。

![](/img/STK_Tutorial/Lesson9/17.png)

### 为地点添加 AzEIMask

此步骤用于定义方向-仰角遮罩 (Azimuth-elevation mask) 以便使用该遮罩作为计算访问时的约束。

点击 Basic>AzEIMask。

使用栏选择地形数据 (Terrain Data)。

勾选使用遮罩作为计算访问时的约束 (Use Mask for Access Constraint) 选项。

点击 OK。

![](/img/STK_Tutorial/Lesson9/18.png)

不要忘记时常保存你的更改。因为 STK 不会自动保存。

![](/img/STK_Tutorial/Lesson9/19.png)

## 在地面站上添加传感器

在菜单栏中点击插入对象 (Insert Object) 按钮。

![](/img/STK_Tutorial/Lesson9/20.png)

对象类型选择传感器 (Sensor)，插入方式选择默认插入 (Insert Default)。

点击插入 (Insert)。

![](/img/STK_Tutorial/Lesson9/21.png)

在弹出窗口中，传感器附着 (Attached) 的对象选择地点 Morton。点击 OK。

![](/img/STK_Tutorial/Lesson9/22.png)

在对象浏览器中右键传感器 (Sensor1)。点击 Rename 将其重命名为 SatTracker。

![](/img/STK_Tutorial/Lesson9/23.png)

## 确保传感器使用了父对象的AzEIMask
在对象浏览器中右键传感器，点击属性。

![](/img/STK_Tutorial/Lesson9/24.png)

点击 Basic>Definition。将传感器类型修改为 Complex Conic。其半角 (Half Angles) 的外角 (Outer) 设定为 180 deg。点击 Apply。

![](/img/STK_Tutorial/Lesson9/25.png)

点击 Constraints>Basic。勾选 Az-EI Mask 选项。点击 Apply。

![](/img/STK_Tutorial/Lesson9/26.png)

## 展示地形遮罩

点击 2D Graphics>Projection。勾选使用约束 (Use Constraints) 选项，选择约束为 AzEIMask。点击 Apply。

![](/img/STK_Tutorial/Lesson9/27.png)

点击 3D Graphics>Projection。将空间投影 (Space Projection) 修改为 50 km。点击 OK。

![](/img/STK_Tutorial/Lesson9/28.png)

返回 3D 地图，调整相机视角。此时看到的是 50 km 高空以下的遮罩，所以其形状呈现出锯齿状。

![](/img/STK_Tutorial/Lesson9/29.png)

换一个视角，可以明显看出 50 km 的具体含义。

![](/img/STK_Tutorial/Lesson9/30.png)

## 建模遮罩对象
在菜单栏中点击插入对象 (Insert Object) 按钮。

插入对象选择设施 (Facility)。插入方式选择默认插入 (Insert Default)。点击插入 (Insert)。

![](/img/STK_Tutorial/Lesson9/31.png)

在对象浏览器中将该设施重命名为 Building。

![](/img/STK_Tutorial/Lesson9/32.png)

聚焦于 Morton。

![](/img/STK_Tutorial/Lesson9/33.png)

将 3D 地图下的视野调整至下图所示。我们将在上方的白色建筑位置插入设施 (Building)。

![](/img/STK_Tutorial/Lesson9/34.png)

在 3D 对象编辑器工具栏将对象调整为设施/Building。点击开始编辑按钮。

![](/img/STK_Tutorial/Lesson9/35.png)

按住 Shift 健，鼠标左键点击白色建筑的中心。

![](/img/STK_Tutorial/Lesson9/36.png)

点击确认更改。

![](/img/STK_Tutorial/Lesson9/37.png)

确认后，3D 地图中将显示一个白色球状建筑物。

![](/img/STK_Tutorial/Lesson9/38.png)

## 创建传感器 AzEI Mask

在对象浏览器中右击 SatTracker。点击 Sensor>AzEI Mask。

![](/img/STK_Tutorial/Lesson9/39.png)

遮罩物体 (Obscuring Objects) 选择 Building。

将输出文件 (Output file) 名称修改为 MyBodyMask。

窗维度 (Window Dim) 修改为 500。

点击 Apply。

确保当前窗口没有挡住左上角窗口。

点击 Compute。

![](/img/STK_Tutorial/Lesson9/40.png)

在弹出窗口中，选择将 MyBodyMask 保存到当前场景文件夹下。默认文件夹即为当前场景文件夹，点击保存即可。

![](/img/STK_Tutorial/Lesson9/41.png)

计算后，关闭两个窗口，并保存当前场景。

## 确保访问计算时传感器用到了 body mask 文件
在对象浏览器中右击 SatTracker，点击属性。

![](/img/STK_Tutorial/Lesson9/42.png)

点击 Basic>Sensor AzEI Mask。使用 MaskFile。点击右侧的 ... 按钮，找到刚才保存的 MyBodyMask.bmsk 文件，点击打开。

![](/img/STK_Tutorial/Lesson9/43.png)

勾选使用遮罩作为计算访问的约束 (Use Mask for Access Constraint)。点击 Apply。

![](/img/STK_Tutorial/Lesson9/44.png)

## 展示 Body Mask 的遮罩
点击 2D Graphics>Projection。

在视野栏 (Field of View) 的约束中，我们不仅想使用之前添加的地形条件约束 (AzEIMask)，我们还想添加之后加入的建筑物的约束 (SensorAzEIMask)。

因此，我们在约束栏中向下滚动，找到 SensorAzEIMask。按住 Ctrl 健，之后使用鼠标左键选择 SensorAzEIMask。

点击 OK。

![](/img/STK_Tutorial/Lesson9/45.png)

此时，在 3D 地图中可以看到建筑物遮挡了传感器的视野。不像添加 SensorAzEIMask 之前视野能够穿过建筑物。

![](/img/STK_Tutorial/Lesson9/46.png)

放大到更大尺度也是一样。这个圆弧就是圆形的建筑物遮挡引起的。

![](/img/STK_Tutorial/Lesson9/47.png)
