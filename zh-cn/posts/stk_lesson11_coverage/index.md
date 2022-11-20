# 【STK11官方Tutorial学习笔记】Lesson11：覆盖


# Lesson 11-1 STK Coverage

对应官方文档：[STK - STK Analysis Workbench Tools (agi.com)](https://help.agi.com/stk/11.6.1/index.htm#training/StartCoverage.htm%3FTocPath%3DTraining%7CLevel%25202%2520-%2520Advanced%2520Training%7C_____4)

本教程将讲解如何使用 STK 计算覆盖 (Coverage)。

{{< bilibili id=BV1Zo4y1d7Jc p=12 >}}

## 创建新场景

1. 打开 STK 软件，点击创建新场景。

![](/img/STK_Tutorial/Lesson11/01.png)

2. 在新场景向导中，做以下设置：
  * 场景名称 (Name)：STK_Coverage
  * 定义场景开始和结束时间，这里选用默认配置即可

3. 点击 OK。

![](/img/STK_Tutorial/Lesson11/02.png)

## 插入区域目标

1. 菜单栏中点击 Insert>New。

![](/img/STK_Tutorial/Lesson11/03.png)

2. 插入对象选择区域目标 (Area Target)，插入方式点击选择美国或其他国家 (Select Countries and US States)。点击 Insert。

![](/img/STK_Tutorial/Lesson11/04.png)

3. 在左侧列表中选择美国 (United_States)，点击插入。

![](/img/STK_Tutorial/Lesson11/05.png)

4. 点击 Close 关闭插入对象窗口。

## 插入飞机
1. 菜单栏点击 Insert>New。
2. 插入对象选择飞机 (Aircraft)，插入方式选择默认插入 (Inset Default)。

![](/img/STK_Tutorial/Lesson11/06.png)

3. 在 3D 对象工具栏中点击开始对象编辑 (Object Edit Start/Accept)

![](/img/STK_Tutorial/Lesson11/07.png)

4. 使用 Lesson 2 中提到的航线绘制方法 (按住 shift 点击鼠标左键)，绘制一条跨越美国地图的飞机航线。

![](/img/STK_Tutorial/Lesson11/08.png)

## 在飞机上创建传感器
1. 在菜单栏中点击 Insert>New。
2. 插入对象选择传感器，插入方式选择默认插入。
3. 点击 Insert。

![](/img/STK_Tutorial/Lesson11/09.png)

4. 选择飞机作为对象。
5. 点击 OK。

![](/img/STK_Tutorial/Lesson11/10.png)

## 插入覆盖定义
1. 点击 Insert>New。插入对象选择覆盖定义 (Coverage Definition)，插入方式选择定义属性 (Define Properties)。点击插入。

![](/img/STK_Tutorial/Lesson11/11.png)

2. 使用区域目标 (area target) 定义网格 (grid)。
  * 点击 Basic>Grid。类型选择自定义区域 (Custom Regions)。
  * 点击选择区域 (Select Regions) 按钮。
  * 使用右箭头按钮将区域目标 (United_States) 移至右侧选中的区域。
  * 点击 OK。
  * 点击 Apply。

![](/img/STK_Tutorial/Lesson11/12.png)

3. 定义网格点粒度
  * 在 Basic>Grid 窗口右侧网格点粒度区域，将经纬度粒度设为 0.25 deg。
  * 点击 Apply。

![](/img/STK_Tutorial/Lesson11/13.png)

4. 定义网格点高度
  * 依旧在当前窗口，找到格点高度 (Point Altitude) 区域。
  * 在下拉列表中选中 Altitude above Terrain。
  * 保持海拔为 0 km 的默认选项不变。
  * 点击 Apply。

![](/img/STK_Tutorial/Lesson11/14.png)

5. 指定飞机作为资产 (Assets)
  * 点击 Basic>Assets。
  * 点击飞机对象，然后点击 Assign。
  * 点击 Apply。

![](/img/STK_Tutorial/Lesson11/15.png)

6. 禁用重新计算访问的选项
  * 点击 Basic>Advanced。
  * 禁用自动重算访问 (Automatically Recompute Access) 选项。
  * 点击 OK。窗口自动关闭。

![](/img/STK_Tutorial/Lesson11/16.png)

7. 在对象浏览器中右击覆盖定义对象，选中 CoverageDefinition 菜单，点击 compute Accesses。

![](/img/STK_Tutorial/Lesson11/17.png)

# Lesson 11-2 Coverage Quality

对应官方文档：[STK - Compute Coverage Over Regions (agi.com)](https://help.agi.com/stk/11.6.1/index.htm#training/StartCoverage.htm%3FTocPath%3DTraining%7CLevel%25202%2520-%2520Advanced%2520Training%7C_____4)

本节任务：测量覆盖质量 (Measure the Quality of Coverage)

{{< bilibili id=BV1Zo4y1d7Jc p=13 >}}

## 创建简单的覆盖率指标
1. 为覆盖定义附加一个默认指标 (default Figure of Merit)。
  * 点击 Insert>New。插入对象选择指标 (Figure of Merit)。
  * 插入方式选择默认 (Insert Default)。
  * 点击 Insert。

![](/img/STK_Tutorial/Lesson11/18.png)

  * 在选择对象对话框中选中 Coverage Definition 对象。
  * 点击 OK。

![](/img/STK_Tutorial/Lesson11/19.png)

2. 在对象浏览器中右击 Figure of Merit，将其重命名为 FOM_SimpleCoverage

![](/img/STK_Tutorial/Lesson11/20.png)

3. 仅显示静态图形
  * 右键 Figure of Merit 选中属性。

![](/img/STK_Tutorial/Lesson11/21.png)

  * 点击 2D Graphics>Animation。
  * 禁用 Show Animation Graphics 选项。
  * 点击 OK。

![](/img/STK_Tutorial/Lesson11/22.png)

4. 生成一个覆盖率满意度百分比指标报告
  * 右键对象浏览器中的 Figure of Merit，点击 Report & Graph Manager。

![](/img/STK_Tutorial/Lesson11/23.png)

  * 禁用展示图表 (Show Graphs) 选项。
  * 展开已安装的样式 (Installed Styles) 找到满意度百分比 (Percent Satisfied)。
  * 点击生成 (Generate) 按钮。

![](/img/STK_Tutorial/Lesson11/24.png)

报告展示了满意百分比和覆盖地区的面积。

![](/img/STK_Tutorial/Lesson11/25.png)

5. 展示动画图
  * 右键 Figure of Merit，选择属性。
  * 点击 2D Graphics>Static。
  * 禁用展示静态图 (Show Static Graphics) 选项。

![](/img/STK_Tutorial/Lesson11/26.png)

  * 点击 2D Graphics>Animation。
  * 勾选展示动态图 (Show Animation Graphics) 选项。
  * 在累积 (Accumulation) 栏的下拉列表中选择直至当前时间 (Up to Current Time)。
  * 修改满意区域颜色为绿色。
  * 点击 OK。

![](/img/STK_Tutorial/Lesson11/27.png)

  * 在动画工具栏中点击播放按钮，观察飞机经过地点之后的变化。

![](/img/STK_Tutorial/Lesson11/28.png)

## 创建访问量指标
1. 插入默认指标
  * 点击 Insert>New。选中指标 (Figure of Merit)。
  * 插入方式选择默认插入 (Insert Default)。
  * 点击插入 (Insert)。
  * 在对话框中选中覆盖定义 (Coverafe Definition) 对象。
  * 点击 OK。

2. 右键刚插入的指标对象，将其重命名为 FOM_NumAccesses。
3. 定义指标。
  * 右键访问量指标 (FOM_NumAccesses)，点击属性。
  * 点击 Basic>Definition。
  * 选择指标类型 (Type) 为访问量 (Number of Accesses)。
  * 计算方式选择全量 (Total)。
  * 点击 Apply。

![](/img/STK_Tutorial/Lesson11/29.png)

4. 仅展示静态图
  * 点击 2D Graphics>Animation。
  * 禁用展示动画图 (Show Animation Graphics) 选项。默认情况下，动画图和静态图都会展示。

![](/img/STK_Tutorial/Lesson11/30.png)

  * 点击 2D Graphics>Static。
  * 勾选展示轮廓 (Show Contours) 选项。
  * 点击去除所有 (Remove All) 按钮，去除等级属性区域中的默认值。
  * 在左侧输入想要的开始 (Start)、结束 (Stop) 等级和步长 (Step)。点击添加等级 (Add Levels)。这里的开始值应该设为网格报告 (该报告将在步骤 5 提到) 中的最小值，结束值设为最大值，这样动画演示时会更清晰一些。
  * 点击 OK。

![](/img/STK_Tutorial/Lesson11/31.png)

5. 生成指标的网格状态报告
  * 右键访问量指标，点击 Report & Graph Manager。

![](/img/STK_Tutorial/Lesson11/32.png)

  * 禁用展示图表 (Show Graphs) 选项。
  * 展开已安装样式 (Installed Styles) 选中网格状态 (Grid Stats)。
  * 点击生成。

![](/img/STK_Tutorial/Lesson11/33.png)

报告如下图所示。

![](/img/STK_Tutorial/Lesson11/34.png)

6. 播放动画图形
  * 右键覆盖定义中的访问量指标，选中属性。
  * 点击 2D Graphics>Static。
  * 禁用展示静态图像 (Show Static Graphics) 选项。

![](/img/STK_Tutorial/Lesson11/35.png)

  * 点击 2D Graphics>Animation。
  * 启用展示动画图形 (Show Animation Graphics) 选项。
  * 在累积 (Accumulation) 栏的下拉列表中选择直至当前时间 (Up to Current Time)。
  * 勾选展示轮廓 (Show Contours) 选项。
  * 点击复制静态等级 (Copy Static Levels) 按钮。
  * 点击 OK。

![](/img/STK_Tutorial/Lesson11/36.png)

  * 点击动画工具栏中的播放按钮，观察实验结果。

![](/img/STK_Tutorial/Lesson11/37.png)
