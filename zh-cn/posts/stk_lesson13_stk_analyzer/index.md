# 【STK11官方Tutorial学习笔记】Lesson13：STK 分析工具包


# Lesson 13 STK Analyzer

对应官方文档：[STK - Perform Trade Studies with Analyzer (agi.com)](https://help.agi.com/stk/11.6.1/index.htm#training/StartAnalyzer.htm%3FTocPath%3DTraining%7CLevel%25202%2520-%2520Advanced%2520Training%7C_____6)

STK Analyzer：
STK Analyzer()模块是一个集成的软件解决方案，通过将Phoenix Integration, Inc.的ModelCenter的工程分析功能与STK混合，可以自动化STK权衡研究和参数分析。

Analyzer使您能够轻松地执行权衡和优化研究，以及后处理功能。Analyzer模块通过易于使用的GUI风格界面提供了工具来理解系统的设计空间，消除了对脚本或编程的需要。STK Analyzer提供了一组分析工具，包括:
* 使您能够得到系统富余的设计空间
* 使您能够轻松地在STK中执行分析，而不涉及编程或脚本
* 介绍权衡研究和后处理能力

本节任务：进行权衡研究 (Perform a Trade Study)

{{< bilibili id=BV1Zo4y1d7Jc p=16 >}}

## 创建新场景

1. 打开 STK，点击创建新场景按钮。

![](/img/STK_Tutorial/Lesson13/01.png)

2. 场景名称输入 STK_Analyzer，时间默认即可。点击 OK。

![](/img/STK_Tutorial/Lesson13/02.png)

3. 插入设施对象。

  * 点击 Insert > New

  ![](/img/STK_Tutorial/Lesson13/03.png)

  * 插入对象选择设施，插入方式选择默认。点击 Insert。插入后在对象浏览器将其重命名为 Exton。

  ![](/img/STK_Tutorial/Lesson13/04.png)

4. 插入卫星对象。

  * 点击 Insert > New。

  * 插入对象选择卫星，插入方式选择定义属性。

  ![](/img/STK_Tutorial/Lesson13/05.png)

  * 在 Basic > Orbit 界面。将倾角 (Inclination) 修改为 40 deg。点击 OK。

  ![](/img/STK_Tutorial/Lesson13/06.png)

  * 在对象浏览器中，将 Satellite1 重命名为 Analyzer。

5. 在卫星上创建传感器。

  * 点击 Insert > New。

  * 插入对象选择传感器，插入方式选择默认插入。点击 Insert。

  ![](/img/STK_Tutorial/Lesson13/07.png)

  * 在对象选择窗口中，选中 Analyzer，点击 OK。

  ![](/img/STK_Tutorial/Lesson13/08.png)

## 生成接入报告

1. 打开接入工具。点击 Analysis > Access。

![](/img/STK_Tutorial/Lesson13/09.png)

2. 选择接入对象。

  * 点击选择对象。(Select Object...)

  ![](/img/STK_Tutorial/Lesson13/10.png)

  * 选中传感器，点击 OK。

  ![](/img/STK_Tutorial/Lesson13/11.png)

3. 选择地面站作为计算接入的对象。

  * 点击地面设施 Exton。点击计算 (Compute)

  ![](/img/STK_Tutorial/Lesson13/12.png)

  * 计算后，设施图标会出现对号，且字体变为粗体。

  ![](/img/STK_Tutorial/Lesson13/13.png)

4. 生成接入报告。

  * 在报告栏 (Reports) 点击 接入 (Access...)。

  ![](/img/STK_Tutorial/Lesson13/14.png)

  * 得到的报告如图所示。可看到接入的总持续时间为 178s。

  ![](/img/STK_Tutorial/Lesson13/15.png)

5. 在时间线视图中查看

  * 在时间线视图中，点击添加时间组件 (Add Time Components) 按钮。

  ![](/img/STK_Tutorial/Lesson13/16.png)

  * 在左侧选中接入的对象，右侧选择组件为 AccessIntervals。点击 OK。

  ![](/img/STK_Tutorial/Lesson13/17.png)

  * 放大 2D 地图，从地图中可以看到成功接入时。卫星轨道所在的位置（蓝线位置）。在时间线视图中调整当前时间到接入时刻，可以看到卫星轨迹，和卫星覆盖区域呈现的圆形。

  ![](/img/STK_Tutorial/Lesson13/18.png)

  * 注：在 STK 11.3 版本中，计算接入后会自动在时间线视图生成与接入相关的时间组件。所以上一步添加时间组件其实是不用做的。但是在老版本当中，需要进行手动操作。

## 定义分析变量 (Analyzer Variables)

1. 打开分析工具。

  * 分别点击工具栏中的 Analysis > Analyzer > Analyzer...

  ![](/img/STK_Tutorial/Lesson13/19.png)

  * 或者右键工具栏，勾选 Analyzer

  ![](/img/STK_Tutorial/Lesson13/20.png)

  * 勾选后，出现如下图所示工具栏，点击该图标进入 Analyzer。

  ![](/img/STK_Tutorial/Lesson13/21.png)

  * 进入后界面如图所示。

  ![](/img/STK_Tutorial/Lesson13/22.png)

2. 选择一个或多个输入变量

  * 在 STK 变量栏中，选中卫星。

  ![](/img/STK_Tutorial/Lesson13/23.png)

  * 双击轨道预报模型 Propagator (TwoBody)，将该属性下的所有变量导入到分析变量中。

  ![](/img/STK_Tutorial/Lesson13/24.png)

3. 选择一个或多个输出变量

  * 在 STK 变量栏中，展开接入选项卡。选中之前创建的卫星和设施间的接入。

  ![](/img/STK_Tutorial/Lesson13/25.png)

  * 在数据提供变量（Data Provider Variables）一栏中，展开接入数据文件夹。

  ![](/img/STK_Tutorial/Lesson13/26.png)

  * 展开持续时间（Duartion）一栏，双击 sum，将其添加至待分析的输出变量中。

  ![](/img/STK_Tutorial/Lesson13/27.png)

## 设计一个参数权衡研究(Design a Parametric trade study)

1. 点击左上角的参数研究按钮，以开启参数研究对话框。

![](/img/STK_Tutorial/Lesson13/28.png)

2. 定义输入变量

  * 点击并拖拽想要的输入参数（例如半长轴 SemiMajorAxis）。将其拖入右侧的变量栏中。

  ![](/img/STK_Tutorial/Lesson13/29.png)

  * 在文本框中，输入想要的参数值。如起始值设为 6878.14，终止值设为 7078.14，采样数设为5，此时步长自动变为50。

  ![](/img/STK_Tutorial/Lesson13/30.png)

3. 定义输出响应

  * 点击并拖拽想要的响应变量，到右侧的响应栏中（如之前定义的输出变量 sum）

  ![](/img/STK_Tutorial/Lesson13/31.png)

4. 点击 Run 按钮运行分析。执行过程中，可以在 2D/3D 地图和时间线视图中看到每次迭代的变化情况。

![](/img/STK_Tutorial/Lesson13/32.png)

运行结束后，可以看到分析工具的输出结果，如下图所示。右侧即为设置的采样点半长轴（SemiMajorAxis）与接入持续时间（sum）的对应情况。

![](/img/STK_Tutorial/Lesson13/33.png)

## 创建地毯图权衡研究（Carpet Plot trade study）

参数研究实验给出了一个输入参数对输出相应结果的影响。要研究多个输入对输出的影响，需要创建地毯图权衡研究。

1. 点击 地毯图 Carpet Plot... 按钮，打开地毯图工具对话框。

![](/img/STK_Tutorial/Lesson13/34.png)

2. 在变量设计一栏中，填入所需的变量取值空间。例如：将 SemiMajorAxis 和 Inclination 拖入右侧变量栏，并设置其取值范围，采样数和步长如下图所示。

![](/img/STK_Tutorial/Lesson13/35.png)

3. 定义输出相应。将之前定义的持续时间总和 sum 拖入响应栏。

![](/img/STK_Tutorial/Lesson13/36.png)

4. 点击 Run...

  * 运行结束后，得到 Analyzer 的输出结果，点击 Add View 可以以不同的形式绘制该图像。

  ![](/img/STK_Tutorial/Lesson13/37.png)

  * 右键 sum 最大的结果一栏点击 Restore Run Values，将该结果对应的输入参数传回 Carpet Plot 工具。

  ![](/img/STK_Tutorial/Lesson13/38.png)

  * 回到 Carpet Plot tool，可以看到此时输入参数，变为刚才使 sum 最大时的输入参数值。点击 Sync to STK，将该参数同步给 STK 场景中。

  ![](/img/STK_Tutorial/Lesson13/39.png)

  * 同步后，相应的场景参数（对应此实验是卫星的半长轴和倾角）会发生变化。

  ![](/img/STK_Tutorial/Lesson13/40.png)
