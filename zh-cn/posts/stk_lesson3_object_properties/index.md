# 【STK11官方Tutorial学习笔记】Lesson3：对象属性


# Lesson 3 Object Properties

对应文档：[STK - Modify STK Object Properties (agi.com)](https://help.agi.com/stk/11.6.1/index.htm#training/StartModifyObjects.htm%3FTocPath%3DTraining%7CLevel%25201%2520-%2520Beginner%2520Training%7C_____3)

每一个 STK 对象都有与之相关的属性。本节中将以我们在 Lesson 2 中创建的 空中目标CircularSat 和地面目标 Bloomington 的 Sensor 为例，尝试修改其属性。

{{< bilibili id=BV1Zo4y1d7Jc p=3 >}}

## 修改卫星属性

为了方便观察，首先将地图中的视野聚焦到 CircularSat。右击对象浏览器中的 CircularSat，点击 zoom to，调整相机视角。然后将 3D 地图窗口移至右侧，方便接下来的属性编辑。

![](/img/STK_Tutorial/Lesson3/01.png)

右击对象浏览器中的 CircularSat，点击属性 (Properties)。

![](/img/STK_Tutorial/Lesson3/02.png)

调整弹出窗口的大小。

### 修改轨道参数

首先修改卫星的轨道 (orbit) 属性。点击属性窗口中的 Basic>Orbit 修改升交点 RAAN 值为 -60。点击下方的 Apply 以应用该修改。

![](/img/STK_Tutorial/Lesson3/03.png)

### 修改卫星姿态

接下来尝试修改卫星姿态 (Attitude)。点击 Basic>Attitude 修改姿态类型 (Type) 为 Nadir alignment with Sun constraint (卫星的Z轴指向天底，X轴的方向由太阳方向决定)。点击 Apply 应用该修改。

![](/img/STK_Tutorial/Lesson3/04.png)

### 修改轨道显示

修改轨道的颜色和线宽。点击 2D Graphics>Attributes。修改轨道颜色为黄色，线条宽度更宽一些。点击 Apply 应用。

![](/img/STK_Tutorial/Lesson3/05.png)

### 修改卫星3D模型

点击 3D Graphics>Model。点击 Model File 右侧按钮浏览文件夹以选择模型。 

![](/img/STK_Tutorial/Lesson3/06.png)

STK 预置了很多卫星的 3D 模型。选择 ikonos 模型，点击打开。

![](/img/STK_Tutorial/Lesson3/07.png)

回到属性窗口，点击 Apply 应用修改。

![](/img/STK_Tutorial/Lesson3/08.png)

### 显示 3D 模型中的向量

点击 3D Graphics>Vector。在 Vectors 标签中，勾选 Sun Vector 和 Moon Vector 以进行显示。

![](/img/STK_Tutorial/Lesson3/09.png)

接着，在 Angles 标签中勾选 SunMoon Angle。

![](/img/STK_Tutorial/Lesson3/10.png)

点击 Apply 应用。在 3D 地图中，可以看到指向太阳的向量，指向月亮的向量，以及两个向量之间的夹角。使用动画栏对场景播放进行控制时，相应的向量也会进行动态改变。

![](/img/STK_Tutorial/Lesson3/11.png)

### 显示数据

点击 3D Graphics>Data Display。勾选 Classical Orbit Elements，点击 Apply 应用。相应数据会在 3D 地图中显示。同样的，当使用动画功能时，相应的数据会随时间进行改变。

![](/img/STK_Tutorial/Lesson3/12.png)

在数据显示界面中。可以修改现实的颜色、字体、位置和对齐方式等。

![](/img/STK_Tutorial/Lesson3/13.png)

## 修改地面传感器属性

右击对象浏览器中 Bloomington 下的 Sensor，点击 Properties 以修改其属性。

![](/img/STK_Tutorial/Lesson3/14.png)

### 修改传感器定义

点击 Basic>Definition。保持其锥体 (Simple Conic) 形状不变，修改其锥半角 (Cone Half Angle) 为 90 度。点击 Apply 应用。

![](/img/STK_Tutorial/Lesson3/15.png)

应用后，传感器的感知范围扩大到传感器所在的整个平面的上方。

![](/img/STK_Tutorial/Lesson3/16.png)

### 增加约束

点击 Constraints>Basic。在距离 (Range) 约束中，将最大距离设置为 2000 km。点击 Apply 应用。

![](/img/STK_Tutorial/Lesson3/17.png)

应用后，可以在传感器周围地面上看到一个半球体，其半径即为 2000 km。

![](/img/STK_Tutorial/Lesson3/18.png)
