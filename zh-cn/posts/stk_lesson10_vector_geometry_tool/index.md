# 【STK11官方Tutorial学习笔记】Lesson10：向量几何工具


# Lesson 10 Vector Geometry Tool

对应官方文档：[STK - STK Analysis Workbench Tools (agi.com)](https://help.agi.com/stk/11.6.1/index.htm#training/STKAnalysisWorkbenchTools.htm%3FTocPath%3DTraining%7CLevel%25202%2520-%2520Advanced%2520Training%7C_____3)

本节课程用于讲解几何向量工具包。

在 Lesson 3 中，我们使用到了卫星模型的向量。本课程中，我们将使用几何向量工具包自定义向量模型。

由于本课程视频只有一半，所以以下教程根据上述官方文档顺序进行。

## 创建新场景

创建一个持续时长为两天的新场景。

1. 打开 STK 软件
2. 点击创建新场景按钮

![](/img/STK_Tutorial/Lesson10/01.png)

3. 在新场景向导中，修改场景名称为 STK_AnalysisWorkbench。结束时间改为 + 2 days。

![](/img/STK_Tutorial/Lesson10/02.png)

4. 点击 OK
5. 场景加载后，点击保存。

![](/img/STK_Tutorial/Lesson10/03.png)

6. 确认保存的路径和文件名。直接点击保存即可。

![](/img/STK_Tutorial/Lesson10/04.png)

## 禁用地形服务器
1. 打开场景属性。

![](/img/STK_Tutorial/Lesson10/05.png)

2. 点击 Basic>Terrain。
3. 取消勾选使用地形服务器。(Use terrain server for analysis)
4. 点击 OK。

![](/img/STK_Tutorial/Lesson10/06.png)

## 插入设施
插入设施对象用以跟踪卫星。
1. 使用 STK 对象工具插入设施对象，插入方式为默认插入。

![](/img/STK_Tutorial/Lesson10/07.png)

2. 将设施对象重命名为 Sat_Tracker。

![](/img/STK_Tutorial/Lesson10/08.png)

## 插入卫星
插入卫星作为设施跟踪的对象。
1. 使用 STK 对象工具箱插入卫星对象，插入方式选择轨道向导 (Orbit Wizard)。

![](/img/STK_Tutorial/Lesson10/09.png)

2. 设置卫星名称为 My_Sat，卫星高度为 700 km，颜色为白色。

![](/img/STK_Tutorial/Lesson10/10.png)

3. 点击 OK。

## 创建访问
创建设施对象和卫星对象之间的访问。
1. 在对象浏览器中，右键 Sat_Tracker，点击 Access。

![](/img/STK_Tutorial/Lesson10/11.png)

2. 在关联对象列表中选择 My_Sat。

![](/img/STK_Tutorial/Lesson10/12.png)

3. 点击 Compute。
4. 观察时间线视图，此时应该有多个连通的访问。

![](/img/STK_Tutorial/Lesson10/13.png)

5. 关闭访问工具窗口。

## 向量几何工具 (Vector Geometry Tool)
任务：创建两个向量之间的夹角。
1. 打开 3D 地图窗口。(默认已打开)
2. 聚焦到地面设施。

![](/img/STK_Tutorial/Lesson10/14.png)

3. 打开地面设施的属性。

![](/img/STK_Tutorial/Lesson10/15.png)

4. 点击 3D Graphics>Vector。

![](/img/STK_Tutorial/Lesson10/16.png)

### 太阳向量
太阳向量 (Sun Vector) 以设施 Sat_Tracker 的中心为锚点，指向太阳。
1. 选中太阳向量的 show 选项。
2. 点击 Apply。

![](/img/STK_Tutorial/Lesson10/17.png)

3. 返回 3D 地图窗口，调整视角以看清太阳向量。(注意调整时间。此时我的场景正值黑夜，太阳在地球背面，所以该向量指向设施下方)

![](/img/STK_Tutorial/Lesson10/18.png)

4. 点击动画工具栏的播放按钮，可以看到太阳向量会一致跟随着太阳进行运动。

![](/img/STK_Tutorial/Lesson10/19.png)

5. 结束观看后，不要忘记点击动画工具栏中的重置按钮。(上图中红色按钮)
6. 返回设施 Sat_Tracker 的属性窗口。

### 卫星向量
可以将场景中的对象添加到向量几何工具的向量列表之中。
1. 点击添加。这会打开向量几何工具。

![](/img/STK_Tutorial/Lesson10/20.png)

2. 在 Sat_Tracker 的组件列表中，展开 To Vectors 所在文件夹。
3. 选中 My_Sat 向量。
4. 点击 OK。

![](/img/STK_Tutorial/Lesson10/21.png)

5. 勾选 Show Magnitude 选项。
6. 点击 Apply。

![](/img/STK_Tutorial/Lesson10/22.png)

7. 返回 3D 地图窗口，调整视角。可以看到太阳向量和卫星向量。

![](/img/STK_Tutorial/Lesson10/23.png)

8. 点击动画工具栏中的播放按钮，会观察到 My_Sat 向量会一直指向卫星。Show Magnitude 使得地图中可以动态显示地面站到卫星之间的距离。
9. 播放完成后，点击动画工具栏中的重置按钮。
10. 返回 Sat_Tracker 的属性窗口。

### 自定义角
创建太阳向量和卫星向量之间的夹角。假设场景中有这样一个需求，当太阳向量与卫星向量之间的夹角小于 30 度时，则关闭卫星追踪系统。
1. 在对象浏览器中，右键 Sat_Tracker 并且选择 Analysis Workbench。

![](/img/STK_Tutorial/Lesson10/24.png)

2. 打开 Vector Geometry 标签页 选中 Sat_Tracker。

![](/img/STK_Tutorial/Lesson10/25.png)

3. 点击新建角 (Create New Angle) 按钮。

![](/img/STK_Tutorial/Lesson10/26.png)

4. 在弹出窗口中，做以下设置：
  * 类型 (Type)：Betweem Vectors
  * 名称 (Name)：Sun_Angle
  * 原向量 (From Vector)：Sat_Tracker My_Sat
  * 目标向量 (To Vector)：Sat_Tracker Sun
5. 点击 OK。

![](/img/STK_Tutorial/Lesson10/27.png)

### 导入自定义角
1. 返回 Sat_Tracker 的属性窗口。点击 3D Graphics>Vector。
2. 选择角 (Angles) 标签页。
3. 点击添加 (Add) 按钮。

![](/img/STK_Tutorial/Lesson10/28.png)

4. 选中 Sun_Angle。
5. 点击 OK。

![](/img/STK_Tutorial/Lesson10/29.png)

6. 选中展示角大小 (Show angle value) 选项。
7. 点击Apply。

![](/img/STK_Tutorial/Lesson10/30.png)

8. 返回 3D 地图窗口并调整视角，确保你能看到太阳向量、卫星向量以及它们之间的夹角。

![](/img/STK_Tutorial/Lesson10/31.png)

9. 点击动画工具栏中的播放按钮。在动画播放时，角度大小也会随之改变。
10. 播放完成后，点击动画工具栏中的重置按钮。

## 计算工具
任务：确认什么时间太阳角 (Sun_Angle) 的角度小于 30 度。

### 创建一个标量
1. 返回 Sat_Tracker 的分析工作台 (Analysis Workbench)。
2. 选择计算 (Calculation) 标签。

![](/img/STK_Tutorial/Lesson10/32.png)

3. 确保左侧对象列表中的 Sat_Tracker 处于选中状态。
4. 点击创建新标量计算 (Create new Scalar Calculation) 按钮。(位于工作台中间)

![](/img/STK_Tutorial/Lesson10/33.png)

5. 在添加计算组件 (Add Calculation Component) 窗口中，设置以下内容：
  * 类型 (Type)：角 (Angle)。
  * 名称 (Name)：Scalar_Sun_Angle
  * 输入角 (Input Angle)：Sat_Tracker Sun_Angle
6. 点击 OK。

![](/img/STK_Tutorial/Lesson10/34.png)

### 设置条件
1. 点击创建新条件 (Create new Condition) 按钮。

![](/img/STK_Tutorial/Lesson10/35.png)

2. 当计算组件窗口开启后，设置以下内容：
  * 类型 (Type)：Scalar Bounds
  * 名称 (Name)：Below_30_Degrees
  * 标量 (Scalar)：Sat_Tracker Scalar_Sun_Angle
  * 操作 (Operation)：Below Maximum
  * 最大值 (Maximum)：30 deg
3. 点击  OK。

![](/img/STK_Tutorial/Lesson10/36.png)

4. 在 Sat_Tracker 的组件列表中，展开 Below_30_Degrees 项。

![](/img/STK_Tutorial/Lesson10/37.png)

5. 右键 SatisfactionIntervals 选择 Report。

![](/img/STK_Tutorial/Lesson10/38.png)

在报告中可以看到太阳角在整个场景时间区间内，小于 30 度的时间。但是报告中没有说明这些时间与地面站和卫星处于连通状态的时间之间的关系。

![](/img/STK_Tutorial/Lesson10/39.png)

6. 关闭报告。
7. 使用鼠标直接将 SatisfactionIntervals 拖入时间线视图。

![](/img/STK_Tutorial/Lesson10/40.png)

观察时间线视图，可以看到太阳对地面站与空间站访问的干扰时间。(因为在场景中假设了当太阳角小于 30 度时，关闭卫星追踪系统)

## 时间工具
使用分析工具台中的时间工具可以创建和管理时间实例、区间和区间集合，将其命名作为可用于模型属性或计算对象的实体。

## 创建自定义区间集合用于确定追踪时机
### 区间列表
创建一个可融合太阳角小于 30 度的时间和地卫连通时间的时间列表。
1. 返回分析工作台。
2. 选择时间标签。
3. 确保对象列表中的 Sat_Tracker 处于选中状态。

![](/img/STK_Tutorial/Lesson10/41.png)

4. 点击创建新区间列表 (Create new Interval List) 按钮，设置如下内容：
  * 类型 (Type)：Merged
  * 名称 (Name)：Optimal_Tracking_Times。
  * 操作 (Operation)：MINUS (performing simple subtraction 相减)

![](/img/STK_Tutorial/Lesson10/42.png)

5. 移除时间组件列表中的任意时间组件，如果需要的话。(两个全移除掉)

![](/img/STK_Tutorial/Lesson10/43.png)

### 被减数
地面站与空间站之间的连通区间列表作为被减数 (Minuend)。
1. 点击 Add。

![](/img/STK_Tutorial/Lesson10/44.png)

2. 在选择时间区间窗口中 (Select Time Intervales)，左侧选中 Facility-Sat_Tracker-To-Satellite-My_Sat。
3. 右侧选中 AccessIntervals。
4. 点击 OK。

![](/img/STK_Tutorial/Lesson10/45.png)

### 减数
将太阳角小于 30 度的时间区间作为减数。
1. 点击 Add。
2. 在选择时间区间窗口中 (Select Time Intervales)，左侧选中 Sat_Tracker。
3. 右侧选中 Below_30_Degrees 下的 SatisfactionIntervals。
4. 点击 OK。

![](/img/STK_Tutorial/Lesson10/46.png)

### 差
之前定义的 Optimal_Tracking_Times 作为上述两者的差 (Difference)。

被减数和减数定义好后点击 OK。

![](/img/STK_Tutorial/Lesson10/47.png)

1. 在 Sat_Tracker 的组件列表中，右键 Optimal_Tracking_Times 选择 Report。

![](/img/STK_Tutorial/Lesson10/48.png)

报告中显示了太阳角小于 30 度的系统可以工作的时间。

![](/img/STK_Tutorial/Lesson10/49.png)

2. 关闭报告。
3. 使用鼠标将 Optimal_Tracking_Times 拖入时间线视图。

![](/img/STK_Tutorial/Lesson10/50.png)

## 时间线视图
观察一个访问连接被干扰的实例。(由于本人的本次实验比较巧，两个时间没有重合的地方，所以差和被减数是相等的)

1. 在时间线视图中，右键被干扰的时间区间。
2. 点击 Center，在时间轴上平铺该时间段。

在时间线视图上，可以看到 Optimal_Tracking_Times 中去除了太阳角小于 30度的时间。

3. 在时间线视图工具栏中，点击刷新当前时间线视图 (Refresh Current Time View) 按钮来重置时间线视图。

![](/img/STK_Tutorial/Lesson10/51.png)

## 保存你的工作
1. 当你完成之后，关掉所有的报告。
2. 保存你的工作。
