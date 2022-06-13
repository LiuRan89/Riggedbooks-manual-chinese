# 整体移动、旋转、缩放
!!! Note
	由于绑定约束的限制，不能直接使用控制器进行变换。需要特殊的方法。  
	  
首先先将书本集合关闭。

![](image/exclude.png "")

再在视图按shift+a，找到最下面Collection Instance ，创建一个集合的实例。

![](image/addinstance.png "")

场景中会出现一个实例对象

![](image/instance.png "")

对该实例进行移动选择缩放的操作即可。该实例将继承原集合的材质的动画。

![](image/moveins.png "")