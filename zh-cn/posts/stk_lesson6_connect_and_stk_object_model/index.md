# 【STK11官方Tutorial学习笔记】Lesson6：STK功能拓展


# Lesson 6 Connect and STK Object Model

对应官方文档：[STK - Extend STK Capabilities (agi.com)](https://help.agi.com/stk/11.6.1/index.htm#training/StartAutomate.htm%3FTocPath%3DTraining%7CLevel%25201%2520-%2520Beginner%2520Training%7C_____6)

STK 提供了广泛的编程接口，本节将做一些简单的演示。

{{< bilibili id=BV1Zo4y1d7Jc p=6 >}}

## HTML 接口演示
### 打开 HTML API 示例程序

点击菜单栏中的 View>HTML Viewer。

![](/img/STK_Tutorial/Lesson6/01.png)

在弹出窗口中选择本地安装的 HTML 示例。点击上方的 Broswer 以选择本地文件夹。点击 Example HTML Utilities，进入 STK Automation 文件夹。

![](/img/STK_Tutorial/Lesson6/02.png)

然后进入 API Demo 文件夹。

![](/img/STK_Tutorial/Lesson6/03.png)

选中 API Demo Utility.htm，点击打开按钮。

![](/img/STK_Tutorial/Lesson6/04.png)

API 示例程序将展示在屏幕中间。为了更方便的观看演示，重新平铺上方的地图窗口。

![](/img/STK_Tutorial/Lesson6/05.png)

### 演示新增设施
点击示例 (Examples) 中的新增设施 (Add facility)。右侧代码沙盒 (Code Sandbox) 中将显示该示例对应的命令代码。点击 Run Code 运行代码。可以在对象浏览器中看到新增了一个名为 MyFacility_Con 的设施。

![](/img/STK_Tutorial/Lesson6/06.png)

### 演示修改设施
点击示例 (Examples) 中的修改设施 (Modify facility)。右侧代码沙盒 (Code Sandbox) 中将显示该示例对应的命令代码。点击 Run Code 运行代码。可以在对象浏览器中看 MyFacility_Con 设施下多了一个传感器。

![](/img/STK_Tutorial/Lesson6/07.png)

### 查看编程接口帮助
点击菜单栏中的 Help>Programming Interface Help。

![](/img/STK_Tutorial/Lesson6/08.png)

将会弹出 STK 编程接口帮助的网站。

点击 Library Reference>Connect Command Library 以查看全部指令。

![](/img/STK_Tutorial/Lesson6/09.png)

点击 Alphabetical Listing，将以字母顺序列出全部指令。

![](/img/STK_Tutorial/Lesson6/10.png)

也可以按照接口类型列出指令。

![](/img/STK_Tutorial/Lesson6/11.png)

如果我想查找所有的 new 指令。首先以字母顺序列出所有指令。然后点击上方的 N 字母。文档中将会显示 N 开头的全部指令。

![](/img/STK_Tutorial/Lesson6/12.png)

点击 New 以查看 New 指令的详细用法。

![](/img/STK_Tutorial/Lesson6/13.png)

新窗口中将显示该指令的语法、相关指令、描述和示例用法等。

![](/img/STK_Tutorial/Lesson6/14.png)


