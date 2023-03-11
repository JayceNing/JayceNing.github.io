# 【STK11官方Tutorial学习笔记】Lesson12: 体积任务


# Lesson 12-1 Volumetrics Task

对应官方文档：[STK - Build a Volumetric Object (agi.com)](https://help.agi.com/stk/11.6.1/index.htm#training/StartVolume.htm%3FTocPath%3DTraining%7CLevel%25202%2520-%2520Advanced%2520Training%7C_____5)

本节任务：构建操作区域 (Build an Area of Operations)

{{< bilibili id=BV1Zo4y1d7Jc p=14 >}}

## 创建新场景

1. 打开 STK 软件，点击创建新场景。

![](/img/STK_Tutorial/Lesson12/01.png)

2. 在新场景向导中：
* 设置场景名称为：STK_Volumetrics
* 保持默认的开始时间，设置结束时间为+1sec

3. 点击OK

![](/img/STK_Tutorial/Lesson12/02.png)

## 启用地形分析

在本实验中不需要用到时间线窗口。首先关掉时间线窗口，然后最大化3D地图窗口，点击保存场景。

![](/img/STK_Tutorial/Lesson12/03.png)

STK支持在联网和非联网条件下导入地形。
1. 在联网条件下
* 右键对象浏览器中的场景，单击属性。

![](/img/STK_Tutorial/Lesson12/04.png)

* 点击 Basic > Terrain。确保 Use terrain server for analyses 处于勾选状态。勾选 Azimuth/Elevation Mask 选项。单击 OK。

![](/img/STK_Tutorial/Lesson12/05.png)

2. 在非联网条件下
* 点击 View > Globe Manager

![](/img/STK_Tutorial/Lesson12/06.png)

* 在 Globe Manager 中点击 Add Terrain/Imagery 按钮

![](/img/STK_Tutorial/Lesson12/07.png)

* 更改文件夹路径为 <STK Install Folder>\AGI\STK11\Data\Resources\stktraining\imagery。点击StHelens_Training.pdtt，点击 Add。在新弹出的窗口中点击 Yes。

![](/img/STK_Tutorial/Lesson12/08.png)

## 定义操作区域

1. 点击 Insert > New
2. 插入对象选择 Area Target，插入方式选择 Area Target Wizard。点击 Insert。

![](/img/STK_Tutorial/Lesson12/09.png)

3. 设置名称为 OperationArea。将区域类型选择为椭圆形 (Ellipse)。将半长轴 (Semi-Major Axis) 更改为 1500 km。将半短轴 (Semi-Minor Axis) 更改为 1500 km。设置中心点纬度 (Latitude) 为 46.6，经度 (Longitude) 为-122.3。点击 OK。

![](/img/STK_Tutorial/Lesson12/10.png)

## 插入地点对象

1. 点击 Insert > New。插入对象选择 Place，插入方式选择 From City Database。

![](/img/STK_Tutorial/Lesson12/11.png)

2. 在数据库中，输入名称为 morton，点击 Search。在返回的结果中，选择位于 Washington 的 Morton。点击 Insert。

![](/img/STK_Tutorial/Lesson12/12.png)

3. 关闭之前的窗口。在对象浏览器中右键 Morton，点击属性。

![](/img/STK_Tutorial/Lesson12/13.png)

4. 点击 Basic > Position。确保 Use terrain data 处于选中状态。设置离地高度为 20 ft。点击 Apply。

![](/img/STK_Tutorial/Lesson12/14.png)

5. 点击 Basic > AzEIMask。使用 Terrain Data，勾选 Use Mask for Access Constraint 选项。点击 Apply。点击 OK。此时可以聚焦 (zoom to) 到 Morton，查看该区域的地形情况。

![](/img/STK_Tutorial/Lesson12/15.png)

## 插入传感器

1. 点击 Insert > New。插入对象选择 Sensor，插入方式选择 Insert Default。点击 Insert。

![](/img/STK_Tutorial/Lesson12/16.png)

2. 在选择对象窗口中，点击 Morton。点击 OK。

![](/img/STK_Tutorial/Lesson12/17.png)

3. 打开传感器对象的属性。右键 Sensor1，点击 Properties。

![](/img/STK_Tutorial/Lesson12/18.png)

4. 修改传感器类型为 Complex Conic。将圆锥外半角修改为 180 deg。点击 Apply。

![](/img/STK_Tutorial/Lesson12/19.png)

5. 点击 Constraints > Basic。勾选 Az-EI Mask 选项，点击 Apply。

![](/img/STK_Tutorial/Lesson12/20.png)

6. 点击 2D Graphics > Projection。在视野栏中勾选 Use Constraints，选中 AzEIMask。点击 Apply。

![](/img/STK_Tutorial/Lesson12/21.png)

7. 点击 3D Graphics > Projection。将空间投影 (Space Projection) 修改为 50 km。点击 OK。

![](/img/STK_Tutorial/Lesson12/22.png)

在 3D 地图中调整视角，可查看传感器的形态。

![](/img/STK_Tutorial/Lesson12/23.png)

# Lesson 12-2 Volumetrics Task2

对应官方文档：[STK - Build a Volumetric Object (agi.com)](https://help.agi.com/stk/11.6.1/index.htm#training/StartVolume.htm%3FTocPath%3DTraining%7CLevel%25202%2520-%2520Advanced%2520Training%7C_____5)

本节任务：为体积对象创建组件 (Create Components for the Volumetric Object)

## 插入体积对象

点击 Insert > New。插入对象选择 Volumetric，插入方式选择 Insert Default。

![](/img/STK_Tutorial/Lesson12/24.png)

## 创建地图网格参考 (Cartographic Grid Reference)

1. 在对象浏览器中，右键场景，点击 Analysis Workbench。

![](/img/STK_Tutorial/Lesson12/25.png)

2. 点击 Spatial Analysis，选中 OperationArea。点击中间的 Create new Volume Grid 按钮。

![](/img/STK_Tutorial/Lesson12/26.png)

3. 修改名称为 SimpleCartographic。保持 Constrain active grid points within Area Target 处于选中状态。点击 Set Grid Values。

![](/img/STK_Tutorial/Lesson12/27.png)

4. 修改最低海拔为 160 km，最高海拔为 2000 km。步长设置为 20。点击 OK。此窗口退出后，继续点击上一个窗口的 OK。记得时常保存场景。

![](/img/STK_Tutorial/Lesson12/28.png)

## 可视化简单地图组件 (Simple Cartographic component)

1. 在对象浏览器中右键体积对象，点击属性。

![](/img/STK_Tutorial/Lesson12/29.png)

2. 点击 Volume Grid 后的省略号按钮。

![](/img/STK_Tutorial/Lesson12/30.png)

3. 点击 OperationArea。为其选择刚刚创建的网格组件 SimpleCartographic。点击 OK。在上一级窗口中点击 Apply。

![](/img/STK_Tutorial/Lesson12/31.png)

4. 在 3D 地图中，可以在目标区域查看到体积网格。

![](/img/STK_Tutorial/Lesson12/32.png)

## 创建约束网格

1. 在对象浏览器中右键场景，点击 Analysis Workbench。

![](/img/STK_Tutorial/Lesson12/33.png)

2. 点击 Spatial Analysis，选中 OperationArea。点击中间的 Create new Volume Grid 按钮。

![](/img/STK_Tutorial/Lesson12/34.png)

3. 修改组件类型。点击 Select。

![](/img/STK_Tutorial/Lesson12/35.png)

4. 选中 Constrained，点击 OK。

![](/img/STK_Tutorial/Lesson12/36.png)

5. 名称修改为SensorFOV (传感器视野)。点击省略号选中刚刚创建的参考网格。

![](/img/STK_Tutorial/Lesson12/37.png)

6. 点击 OperationArea。为其选择刚刚创建的网格组件 SimpleCartographic。点击 OK。

![](/img/STK_Tutorial/Lesson12/38.png)

7. 选择空间条件，点击右侧的省略号按钮。

![](/img/STK_Tutorial/Lesson12/39.png)

8. 点击 Sensor1。为其选择 Visibility 的空间条件。点击 OK。并且在上一级窗口中点击 OK。

![](/img/STK_Tutorial/Lesson12/40.png)

## 观察带约束网格的体积对象

1. 在对象浏览器中右键 Volumetric1，点击属性。

![](/img/STK_Tutorial/Lesson12/41.png)

2. 在 Basic > Definition 界面中，点击 Volume Grid 右侧的省略号按钮。

![](/img/STK_Tutorial/Lesson12/42.png)

3. 点击 OperationArea。为其选择刚刚创建的网格组件 SensorFOV。点击 OK。

![](/img/STK_Tutorial/Lesson12/43.png)

4. 回到刚才的属性页面。选中 Spatial Calculation，点击右侧的省略号按钮。

![](/img/STK_Tutorial/Lesson12/44.png)

5. 点击 OperationArea，在右侧空间计算组件中选择 Altitude。点击 OK。在返回窗口中点击 Apply。别忘了时常保存场景。

![](/img/STK_Tutorial/Lesson12/45.png)

在对象浏览器中选中 Volumetric1。点击工具栏上的 Volumetric 选项，点击 Compute。此时窗口右下角会显示计算的进度条。计算结束后，进度条消失。

![](/img/STK_Tutorial/Lesson12/46.png)

## 可视化体积网格

1. 回到体积对象的属性界面。点击 3D Graphics > Grid。禁用 Show Grid 选项。

![](/img/STK_Tutorial/Lesson12/47.png)

此时在 3D 地图中，可以看到计算的结果。

![](/img/STK_Tutorial/Lesson12/48.png)

2. 回到体积对象的属性界面。点击 3D Graphics > Volume。选中 Spatial Calculation Levels，点击 Insert Evenly Spaced Values 按钮。

![](/img/STK_Tutorial/Lesson12/49.png)

3. 设置起始值为 160，终止值为 2000。步长为 200。点击 Create Values。在返回的属性窗口中，点击 Apply 应用修改。

![](/img/STK_Tutorial/Lesson12/50.png)

4. 选中 3D Graphics > Legends。为体积对象添加图例，勾选 Show Legend 选项。修改文字题目为 Altitude (km)。不需要显示小数，因此将小数位数改为 0。修改色块宽度为 60。点击 OK。

![](/img/STK_Tutorial/Lesson12/51.png)

此时在 3D 地图中，移动视角，查看体积网格效果。

![](/img/STK_Tutorial/Lesson12/52.png)

## 生成报告

1. 在对象浏览器中右键体积对象，点击 Report & Graph Manager。

![](/img/STK_Tutorial/Lesson12/53.png)

2. 确保 Show Reports 选项处于选中状态。报告类型选择 Satisfaction Volume。点击 Generate。

![](/img/STK_Tutorial/Lesson12/54.png)

报告的计算结果表明，在创建的 160 km 到 2000 km 范围内的体积区域内，有 96.41% 的区域满足了覆盖的要求。

![](/img/STK_Tutorial/Lesson12/55.png)


