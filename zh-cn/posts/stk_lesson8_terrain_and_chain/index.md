# 【STK11官方Tutorial学习笔记】Lesson8：地形分析和链对象


# Lesson 8-1 Analytical and Visual Terrain

对应官方文档：[STK - Add Fidelity with STK Pro (agi.com)](https://help.agi.com/stk/11.6.1/index.htm#training/StartTerrainImagery.htm%3FTocPath%3DTraining%7CLevel%25202%2520-%2520Advanced%2520Training%7C_____1)

本节课程将演示如何将自己的地形和图像添加到场景中。

新建一个名为 Lesson 8 的场景。

{{< bilibili id=BV1Zo4y1d7Jc p=8 >}}

## 地形图导入及转换

在对象浏览器中右键场景，点击属性 (Properties)。

![](/img/STK_Tutorial/Lesson8/01.png)

在新弹出的属性窗口中，点击 Basic>Terrain，点击右侧的 Add 导入本地地形文件。

![](/img/STK_Tutorial/Lesson8/02.png)

在本地文件中寻找 hoquiam-e.dem。该文件位于 <STK Install Folder>\Data\Resources\stktraining\samples。比如我的文件位于 D:\Program Files\AGI\STK 11\Data\Resources\stktraining\samples

点击打开进行导入。

![](/img/STK_Tutorial/Lesson8/03.png)

导入成功后如下图所示。在该窗口中依次点击 Apply 和 OK。

![](/img/STK_Tutorial/Lesson8/04.png)

地形文件需要转化为 PDT 格式文件才可以使用。点击菜单栏 Utilities>Imagery and Terrain Converter。

![](/img/STK_Tutorial/Lesson8/05.png)

在图像和地形转换器中，点击地形区域 (Terrain Region)。在地形源 (Terrain Source) 中，选择刚才导入的 hoquiam-e.dem。

数据输出文件夹选择为当前场景所在文件夹。

因为该地形文件是圣海伦斯 (St.Helens) 山周围的地形图，因此将其重命名为 MtStHelens。 

点击转换 (Convert) 按钮。

![](/img/STK_Tutorial/Lesson8/06.png)

## 在 3D 地图中添加地形

在 3D 地图的工具栏中点击地球管理器 (Globe Manager)。

![](/img/STK_Tutorial/Lesson8/07.png)

在左侧会弹出地球管理器。点击添加地形 (Add Terrain/Imagery) 按钮。

![](/img/STK_Tutorial/Lesson8/08.png)

点击 Add Terrain/Imagery。

![](/img/STK_Tutorial/Lesson8/09.png)

在弹出的窗口中打开刚才保存转换地形文件的输出文件夹，勾选地形文件。点击下方的 Add 按钮。

![](/img/STK_Tutorial/Lesson8/10.png)

此时弹出窗口，询问是否要用此地形进行分析。点击确定 (Yes) 即可。

![](/img/STK_Tutorial/Lesson8/11.png)

在地球管理器中右击刚导入的地形文件，点击 Zoom To。此时，3D 地图将会聚焦于地形所在位置。

调整地图视角，可以观察到此地形的立体结构。

![](/img/STK_Tutorial/Lesson8/12.png)

在地球管理器中右击刚导入的地形文件，点击 Toggle Extents。查看导入地形图的轮廓。再次点击可以取消轮廓显示。

![](/img/STK_Tutorial/Lesson8/13.png)

## 在场景中添加地点

在搜索栏中输入圣海伦斯山 (st helens)，双击搜索到的合适的地点。

![](/img/STK_Tutorial/Lesson8/14.png)

在对象浏览器中将会导入刚才双击的地点。聚焦 (Zoom to) 到该地点，确认地点选择无误。

![](/img/STK_Tutorial/Lesson8/15.png)

不过此时地点标记可能会被山体挡住。

点击 3D 地图工具栏中的属性 (Properties) 按钮。

![](/img/STK_Tutorial/Lesson8/16.png)

勾选标签调整栏 (Label Declutter) 中的使能 (Enable) 选项。点击 OK。

![](/img/STK_Tutorial/Lesson8/17.png)

此时就能确保地点标签不被挡住了。

![](/img/STK_Tutorial/Lesson8/18.png)

## 为地点添加地形约束

为了后续访问计算时能够考虑地形因素，我们需要为地点对象添加地形约束。

在对象浏览器中右击该地点，点击属性 (Properties)。

![](/img/STK_Tutorial/Lesson8/19.png)

点击 Basic>AzEIMask。使用地形数据 (Terrain Data) 作为 Mask 遮罩，并且勾选使用遮罩作为访问计算的约束 (Use Mask for Access Constraint)。

![](/img/STK_Tutorial/Lesson8/20.png)

点击 2D Graphics>AzEIMask。勾选距离栏 (At Range) 中的显示 (Show) 选项，设置最大距离 (Maximum Range) 为 10 km。以显示 10 km 范围内的遮罩。点击 OK。

![](/img/STK_Tutorial/Lesson8/21.png)

设置成功后，EzEI遮罩 (EzEIMask) 将在 3D 地图中显示。红色遮罩的上方就是地点 (图中小黄点) 可以直视到的范围。

![](/img/STK_Tutorial/Lesson8/22.png)

## 引入对象演示访问计算

菜单栏点击 Insert>New。

![](/img/STK_Tutorial/Lesson8/23.png)

插入对象为地面车辆 (Ground Vehicle)，方式为自定义属性 (Define Properties)，点击插入 (Insert)。

![](/img/STK_Tutorial/Lesson8/24.png)

海拔参考栏配置为：

* 粒度 (Granularity)：设置为 0.01 km。
* 插值方式 (Interp Method)：设置为地形高度 (Terrain Height)。

位置配置：

* 点击 Insert Point 以插入点
* 由于车辆所在海拔已经设置为参考地形高度，我们配置车辆的经纬度即可。
* 设置维度 (Latitude) 为 46.23，经度 (Longitude) 为 -122.23。(设置该经纬度只是为了其位置在山的位置附近，其具体运动轨迹还要在后续调整)

点击 OK，插入车辆对象。

![](/img/STK_Tutorial/Lesson8/25.png)

在 3D 对象编辑栏中，选择编辑对象为车辆。

![](/img/STK_Tutorial/Lesson8/26.png)

接下来我们要绘制车辆的运动轨迹。调整 3D 地图视角到火山口正上方。

点击下图中框出的 Object Edit Start 按钮。

![](/img/STK_Tutorial/Lesson8/27.png)

接下来，开始绘制车辆的运动轨迹。

轨迹绘制方式与 Lesson 2 中提到的航线绘制方式相同。

* 添加 (Add)：按住 Shift 点击鼠标左键。
* 调整 (Modify)：使用鼠标左键按住并移动需要调整的节点。
* 删除 (Remove)：按住 Shift，鼠标左键点击需要删除的节点。

![](/img/STK_Tutorial/Lesson8/28.png)

最后，不要忘记删除在属性定义时引入的右下角的点。

点击 Object Edit Accept 按钮以保存该路线。

![](/img/STK_Tutorial/Lesson8/29.png)

## 计算访问

为了了解地形如何影响 Access，我们可以计算地点和车辆之间的访问存在的时间。 (此访问指的就是车辆与地点坐标间的连线。如果被山体遮挡，则没有访问)

在对象浏览器中右击车辆对象，点击 Access。

![](/img/STK_Tutorial/Lesson8/30.png)

此时访问起点已选择为车辆。点击下方的地点 (Mount_St_Helens_WA)，将其设置为访问终点。点击 Compute。

![](/img/STK_Tutorial/Lesson8/31.png)

计算结束后，点击 Access 查看结果。

![](/img/STK_Tutorial/Lesson8/32.png)

从报告中可以看出，访问存在的时间是不连续的。说明汽车在运动过程中，存在访问被山体遮挡的情况。

![](/img/STK_Tutorial/Lesson8/33.png)

如下图所示。此时车辆所在位置，与地点坐标间没有访问。(访问被山体遮挡)

![](/img/STK_Tutorial/Lesson8/34.png)

而下图时刻，车辆与地点坐标间存在访问。图中白线即为所示。

![](/img/STK_Tutorial/Lesson8/35.png)

## 访问的时间线视图

计算访问后，访问的连通时间已被自动加入时间线视图。

![](/img/STK_Tutorial/Lesson8/36.png)

但是由于连通时间比较短，我们加入车辆运动的持续时间方便对比。

点击时间线视图中的添加时间组件 (Add Time Components) 按钮。

![](/img/STK_Tutorial/Lesson8/37.png)

选中车辆，可用持续时间 (AvailabilityTimeSpan)。点击 OK。

![](/img/STK_Tutorial/Lesson8/38.png)

右键车辆存在的时间轨道，点击 Center。

![](/img/STK_Tutorial/Lesson8/39.png)

现在可以很方便的观察访问存在的时间了。第二条轨道橙色的部分即为访问存在的时间。也可以通过动画播放来动态观察车辆与地点坐标间的访问连通情况。

![](/img/STK_Tutorial/Lesson8/40.png)

# Lesson 8-2 Chain Objects

对应文档：[STK - Add Fidelity with STK Pro (agi.com)](https://help.agi.com/stk/11.6.1/index.htm#training/StartTerrainImagery.htm%3FTocPath%3DTraining%7CLevel%25202%2520-%2520Advanced%2520Training%7C_____1)
文档与 8-1 相同

{{< bilibili id=BV1Zo4y1d7Jc p=9 >}}

## 插入链对象
菜单栏点击 Insert>New。

![](/img/STK_Tutorial/Lesson8/41.png)

点击 Chain>Insert Default>Insert。

![](/img/STK_Tutorial/Lesson8/42.png)

链对象可以满足需要多跳转发才能连通的情景。

## 插入卫星
点击菜单栏 Insert>New。

插入对象选择卫星，插入方式选择轨道向导 (Orbit Wizard)。点击插入 (Insert)。

![](/img/STK_Tutorial/Lesson8/43.png)


设置卫星类型为地球同步卫星 (Geosynchronous)。卫星名称为 GeoSat。星下点 (Subsatellite Point) 设为-120 deg。倾角 (Inclination) 设为 50 deg。

点击 OK。

![](/img/STK_Tutorial/Lesson8/44.png)

## 定义链中的对象

右键链对象，点击属性。

![](/img/STK_Tutorial/Lesson8/45.png)

在定义链属性时，需要按顺序添加对象。在左侧框中选择要添加的对象，点击红框里的蓝色箭头将该对象添加进链。

在链中依次添加地点 (Mount_St_Helens_WA)、同步卫星 (GeoSat) 和 车辆 (GroundVehicle1)。

点击 OK。

![](/img/STK_Tutorial/Lesson8/46.png)

## 计算链的连通情况

右击对象浏览器中的链。点击 Chain>Compute Access。

![](/img/STK_Tutorial/Lesson8/47.png)

计算完成后，点击 Report & Graph Manager 查看计算报告。

![](/img/STK_Tutorial/Lesson8/48.png)

如果想查看该链的连通情况，在弹出窗口中依次点击连通数据 (Access Data) 和 生成 (Generate)。

![](/img/STK_Tutorial/Lesson8/49.png)

连通数据为空，该链的连通存在一些问题导致没有连接。有可能是空间站无法连接地面站导致。

![](/img/STK_Tutorial/Lesson8/50.png)

观察 3D 地图可知，此时空间站位于红色 Mask 区域的下方，这意味着地面站无法直射到空间站。我们可以调整地面站位置以解决此问题。

![](/img/STK_Tutorial/Lesson8/51.png)

## 调整地面站位置

在 3D 对象编辑栏中选中地面站，点击左侧的对象编辑按钮。

![](/img/STK_Tutorial/Lesson8/52.png)

按住鼠标左键拖动，以改变地面站点的位置。

![](/img/STK_Tutorial/Lesson8/53.png)

调整好后点击对象编辑确认。

![](/img/STK_Tutorial/Lesson8/54.png)

如果此时图中出现了两条线，则说明线路连接成功。 (要注意此时时间轴是否位于小车存在的时间，如果不是先将时间轴拉到小车存在的时间)

![](/img/STK_Tutorial/Lesson8/55.png)

移动视角将看到该两条路径相交于远处的空间站。

![](/img/STK_Tutorial/Lesson8/56.png)

## 重新计算链的连通情况

打开链的 Report & Graph Manager。

![](/img/STK_Tutorial/Lesson8/57.png)

点击 Complete Chain Access，查看完整链的连通报告。点击 Generate 生成。

![](/img/STK_Tutorial/Lesson8/58.png)

在报告中可以看到完整链的连通的开始时间、结束时间和连通时长。

![](/img/STK_Tutorial/Lesson8/59.png)
