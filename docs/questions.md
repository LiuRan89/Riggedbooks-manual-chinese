# 常见问题
---
###❓<font color="#dd0000">关于调节书脊弯曲穿插的问题？</font><br />
问题描述：调节书脊深度时，书脊和书绑带和书内页穿插的问题
![](image/coverspineinter.gif "")
在书脊的模型中间，可以找到一个空物体，这个空物体是用来单独调整书绑带和书内页的深度的，这个空物体可以左右移动，可以解决部位的穿插问题。
![](image/coverspineintersolveA.png"")
![](image/coverspineintersolveB.png"")

---
###❓<font color="#dd0000">如何移动,旋转,缩放?</font><br />
参考页面：**[书本变换](transform.md)**
视频教程：[https://www.bilibili.com/video/BV1Af4y1Z7kJ?p=3](https://www.bilibili.com/video/BV1Af4y1Z7kJ?p=3)

---
###❓<font color="#dd0000">如何减少页数?</font><br />
视频教程:[https://www.bilibili.com/video/BV1Af4y1Z7kJ?p=4](https://www.bilibili.com/video/BV1Af4y1Z7kJ?p=4)

---
###❓<font color="#dd0000">如何调节凹槽的UV和形状?</font><br />
视频教程:[https://www.bilibili.com/video/BV1Af4y1Z7kJ?p=5](https://www.bilibili.com/video/BV1Af4y1Z7kJ?p=5)

---
###❓<font color="#dd0000">如何在封面添加立体字?</font><br />
视频教程:[https://www.bilibili.com/video/BV1Af4y1Z7kJ?p=6](https://www.bilibili.com/video/BV1Af4y1Z7kJ?p=6)

---
###❓<font color="#dd0000">如何批量调节书页材质的参数?</font><br />
视频教程:[https://www.bilibili.com/video/BV1Af4y1Z7kJ?p=7](https://www.bilibili.com/video/BV1Af4y1Z7kJ?p=7)
需要的代码：
```
import bpy
for obj in bpy.context.selected_objects:
    m=obj.data.materials[0]
    m.node_tree.nodes["Principled BSDF"].inputs['Specular'].default_value = 0.5    

```

---
###❓<font color="#dd0000">如何给封面厚度部分贴图?</font><br />
视频教程:[https://www.bilibili.com/video/BV1Af4y1Z7kJ?p=8](https://www.bilibili.com/video/BV1Af4y1Z7kJ?p=8)

---
###❓<font color="#dd0000">为什么只做了100页?</font><br />
可以做更多，但我觉得没必要，因为大部分时候CG制作只在乎书的厚度。

---

###❓<font color="#dd0000">适用EEVEE和Cycle吗?</font><br />
都适用。

---
###❓<font color="#dd0000">用到了几何节点吗？</font><br />
没有，都是基础的约束和代码.

---
###❓<font color="#dd0000">我可以用别的渲染器吗？</font><br />
可以，只要你会自己修改材质，这很简单，因为我没有设置复杂的材质系统。但是用了别的渲染器后，跟材质相关的边缘磨损效果参数就没有作用了。

---
	
###❓<font color="#dd0000">未来会有更多的更新吗？</font><br />
我现在还有一些想法，但实现起来很困难，如果问题都解决了，我很乐意更新新的功能。当然如果现在的版本有bug，将来一定会尽力修复。

---
	
###❓<font color="#dd0000">怎么转换成纯模型？</font><br />
选择控制器，点击最下面的convert to mesh 按钮。

---

###❓<font color="#dd0000">为什么第100页的动画控制器名称叫99p(100)？</font><br />
因为命名为100P会让排序打乱。

---

###❓<font color="#dd0000">如何在封面添加立体字？</font><br />
在书本闭合的情况下，找到大纲里书本集合下的Cover_Rot_ConD物体，在它下面又个Cover_Up_Null空物体，把文字作为它的子物体即可。你可以选择文字，按住shift键拖拽给Cover_Up_Null。

---

###❓<font color="#dd0000">如果不小心删除了关键帧怎么找回来?</font><br />
选择控制器，在控制器的自定义属性里，有所有参数，找到需要的参数给它打关键帧即可。
![](image/custompanel.png "")

---


###❓<font color="#dd0000">如何制作书页合上的动画?</font><br />
如果要制作书页打开后又合上的动画，可以把后面的关键帧都删掉，把前面的关键帧mirror一下。
![](image/close.png "")

---

###❓<font color="#dd0000">Blender播放翻书动画的时候崩溃了？</font><br />
在我目前得到的使用反馈中，当同时开启了wiggle bone这个插件的时候，播放动画，blender软件会直接崩溃。解决方法是，把wiggle bone禁用。
我还没有找到问题所在，找到的话会在下个版本更新。在这里先记录一下。

---
















