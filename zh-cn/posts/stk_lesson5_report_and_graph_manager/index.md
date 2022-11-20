# 【STK11官方Tutorial学习笔记】Lesson5：报告和图表管理器


# Lesson 5 Report and Graph Manager

对应官方文档：[STK - Create Reports & Graphs](https://help.agi.com/stk/11.6.1/index.htm#training/StartReportGraph.htm%3FTocPath%3DTraining%7CLevel%25201%2520-%2520Beginner%2520Training%7C_____5)

本节将带大家认识 报告和图表管理器 (Report and Graph Manager)。以 LLA positon (经度、维度和高度位置) 报告生成为例，使用管理器的功能。

{{< bilibili id=BV1Zo4y1d7Jc p=5 >}}

## 打开报告和图表管理器

点击数据栏中的 Report & Graph Manager 按钮。

![](/img/STK_Tutorial/Lesson5/01.png)

或者点击菜单栏当中的 Analysis>Report & Graph Manager。

![](/img/STK_Tutorial/Lesson5/02.png)

## 选择对象

在弹出窗口中，选择合适的对象类型。

![](/img/STK_Tutorial/Lesson5/03.png)

本例中，对象类型 (Object Type) 选择卫星 (Satelite)。

## 展示报告

在左侧栏中，选中想要查看报告的卫星。右侧栏中，仅勾选 Show Reports 选项。STK 中预置了很多的报告类型，展开 Installed Styles 以查看预置的报告。

![](/img/STK_Tutorial/Lesson5/04.png)

向下滚动找到 LLA Position，点击生成 (Generate)。

![](/img/STK_Tutorial/Lesson5/05.png)

新弹出的窗口即为 LLA Position 报告。同样的，我们可以使用 Lesson 4 中提到的方法保存报告快照。

![](/img/STK_Tutorial/Lesson5/06.png)

使用快照管理器 (Qucik Report Manager) 快速查看保存的报告快照。

![](/img/STK_Tutorial/Lesson5/07.png)

## 展示图表

上述信息也可使用图表进行展示。

回到报告和图表管理器，右侧栏仅勾选 Show Graphs 选项。在下方预置的图表中，选择 LLA Position，点击 Generate 生成。

![](/img/STK_Tutorial/Lesson5/08.png)

新弹出的窗口即为卫星的 LLA Position 数据图表。同样的，也可以为该图表保存报告快照。

![](/img/STK_Tutorial/Lesson5/09.png)

保存后，可通过快照管理器查看该报告。图表报告的图表会和数据报告略有不同。

![](/img/STK_Tutorial/Lesson5/10.png)

## 自定义报告样式
刚才，我们看到 STK 中已经预置了很多种报告样式。我们也可以自定义自己的报告样式。

返回图形和报告管理器。右侧栏点击 STK_Fundamentals Styles，以在该文件夹中生成自定义报告。点击上方的创建新报告样式 (Create new report style) 按钮。

![](/img/STK_Tutorial/Lesson5/11.png)

在 STK_Fundamentals Styles 下生成了一个新的报告样式，将其重命名为 Custom Report。

![](/img/STK_Tutorial/Lesson5/12.png)

在新弹出的窗口中，左侧显示当前的对象可用的数据。本例中想在报告中插入笛卡尔位置 (Catesian Position)。首先在搜索栏中输入 Catesian，点击 Filter 过滤可用数据。

![](/img/STK_Tutorial/Lesson5/13.png)

展开 Cartesion Posirion，接下来展开 Fixed 文件夹。鼠标左键点击 Time，按住 Shift 在点击 z 以勾选从 Time 到 z 的四个数据。点击右侧的蓝色箭头，将该字段数据加入自定义报告中。

点击 OK 保存该自定义报告。

![](/img/STK_Tutorial/Lesson5/14.png)

回到报告和图表管理器。依次点击刚保存的自定义报告和下方的生成按钮。

![](/img/STK_Tutorial/Lesson5/15.png)

笛卡尔坐标报告将在新弹出的窗口中展示。同样的，可以保存该报告的快照。

![](/img/STK_Tutorial/Lesson5/16.png)

## 修改报告单位

此时，上述报告中四个数据的单位在其表头中的括号里进行显示，时间单位为 UTCG，坐标单位为 km。我们可以更改该报告中各个量的单位。

点击报告上方的报告单位 (Report Units)。

![](/img/STK_Tutorial/Lesson5/17.png)

本例中修改时间单位。在弹出的窗口中选择时间格式 (DateFormat)，右侧选中 Epoch Seconds。点击 OK。

![](/img/STK_Tutorial/Lesson5/18.png)

## 导出CSV文件

为方便报告的后续使用，也可以将报告导出为CSV文件。

在报告窗口中点击 Save as .csv (最左侧红框)。在弹出窗口中选择保存的文件夹，修改文件名称，最终点击保存按钮。

![](/img/STK_Tutorial/Lesson5/19.png)
