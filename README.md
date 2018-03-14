# SLCurveChartDemo
A Easy Way to draw a curve chart for iOS!

## Cocoapod集成
>pod 'SLCurveChartLib', '~> 1.0.2'

## 应网友要求，再一张图上绘制多个曲线
由于本人觉的一张图绘制多个曲线，一来每个项目需求不同，二来本身不同的数据绘制同一个图上，必然会有有些单位的不平均，以及点数X坐标的差异等等诸多问题
所以在本gitHub上新建了一个mulcurDev的分支，仅仅考虑了，两个曲线单位无差别处理，X轴是一致的情况。有需要绘制这种曲线的网友请，checkout该分支，tag 1.0.3版本。
应用该多图绘制是，注意保证两个曲线X轴数据相同，且点数一致即可。（以下有效果图展示）

## 框架逻辑说明
近日从网友反映来看，可能代码注释不多，大家可能不知道从何下手，比如绘制多条曲线，如何自定义对应坐标的刻度显示，所以附上对应的框架逻辑图。
还有该框架的封装的基本结构很大参考了Charts框架的封装形式，内部实现机制不一致，也是作为Charts框架的致敬吧！
近日从网友反映来看，可能代码注释不多，大家可能不知道从何下手，比如绘制多条曲线，如何自定义对应坐标的刻度显示，所以附上对应的框架逻辑图。
1. 整个图表的整体框架组件
![image](https://github.com/cslmark/SLCurveChartLib/blob/master/CurveShowPics/%E6%A1%86%E6%9E%B6%E6%B5%81%E7%A8%8B%E5%9B%BE/SLChartLib%E6%95%B4%E4%BD%93%E7%BB%93%E6%9E%84%E4%BD%93.png)
2. 图表组件各个类的继承关系图谱
![image](https://github.com/cslmark/SLCurveChartLib/blob/master/CurveShowPics/%E6%A1%86%E6%9E%B6%E6%B5%81%E7%A8%8B%E5%9B%BE/%E5%9B%BE%E5%BD%A2%E5%9F%BA%E6%9C%AC%E7%B1%BB%E5%85%B3%E7%B3%BB%E5%9B%BE.png)
3. 图标中各个数据源的继承关系以及框架预留拓展部分
![image](https://github.com/cslmark/SLCurveChartLib/blob/master/CurveShowPics/%E6%A1%86%E6%9E%B6%E6%B5%81%E7%A8%8B%E5%9B%BE/%E6%95%B0%E6%8D%AE%E7%B1%BB%E5%9E%8B%E7%9A%84%E6%B5%81%E7%A8%8B%E5%9B%BE.png)

## 效果展示
使用该库可以非常灵活的配置曲线颜色，曲线样式，对应X轴和自定义的Y轴配置，动态纵坐标，是否使能缩放X轴，以及对应网格等等。效果如下图所示：
* 显示左侧Y轴以及Y轴网格
![image](https://github.com/cslmark/SLCurveChartDemo/blob/master/CurveShowPics/WX20170614-171819@2x.png
)
* 不显示任何坐标轴以及对应的网格 
![image](https://github.com/cslmark/SLCurveChartDemo/blob/master/CurveShowPics/WX20170614-172019@2x.png
)
* 显示X轴和对应的网格
![image](https://github.com/cslmark/SLCurveChartDemo/blob/master/CurveShowPics/WX20170614-172152@2x.png
)
* 显示正常的左测Y轴和X轴和对应的网格
![image](https://github.com/cslmark/SLCurveChartDemo/blob/master/CurveShowPics/WX20170614-172343@2x.png
)
* 同时显示X轴，左右两侧的Y轴以及对应的网格
![image](https://github.com/cslmark/SLCurveChartDemo/blob/master/CurveShowPics/WX20170614-172500@2x.png
)
* 一张图表中显示多个曲线，主要需要同步的是mulcurDev分支
![image](https://github.com/cslmark/SLCurveChartLib/blob/master/CurveShowPics/WX20170620-162326%402x.png
)
## 使用说明
Lib文件夹如下：
![image](https://github.com/cslmark/SLCurveChartDemo/blob/master/CurveShowPics/WX20170614-173616@2x.png
)

API的调用和具体参照DEMO，如果通过代码创建的UIView还是通过Xib、Storyboard来创建。只需要改View的类是BaseCurveView就能轻松实现作图的功能，其中曲线颜色，线宽，X轴，Y轴的字体，颜色，网格的实线，虚线均可以灵活配置。
使用的时候引入总头文件**#import "SLCurveChartLib.h"**即可.




