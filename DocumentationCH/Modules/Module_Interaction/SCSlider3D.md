# SCSlider3D
![SCSlider3D.png](../../../Images/Module_Interaction/SCSlider3D.png)

**SCSlider3D**模块为开发者提供基于Collider的滑动条，在需要带有立体效果Slider的场景中使用。

## 如何创建SCSlider组件

SDK为开发者提供了两种类型为SCSlider3DType1和SCSlider3DType2的SCSlider组件。
SCSlider3DType1和SCSlider3DType2除了模型有一定差别之外，SCSlider3DType1的值为整数，SCSlider3DType2的值为小数。

**SCSlider3DType1的创建**
* SCSlider3DType1的预制体组件位于`SDK\Modules\Module_Interaction\SCSlider3D\Resources\Prefabs\SCSlider3DType1.prefab`处，将此预制体组件拖拽进场景即可。
* 通过在Hierarchy面板右键`SC3DUI/SCSlider3DType1`创建，在场景中生成SCSlider3DType1组件。

**SCSlider3DType2的创建**
* SCSlider3DType2的预制体组件位于
  `SDK\Modules\Module_Interaction\SCSlider3D\Resources\Prefabs\SCSlider3DType2.prefab`处，将此预制体组件拖拽进场景即可。
* 通过在Hierarchy面板右键`SC3DUI/SCSlider3DType2`创建，在场景中生成SCSlider3DType2组件。


## SCSlider的参数解析

![SCSlider3DInspector.png](../../../Images/Module_Interaction/SCSlider3DInspector.png)

此组件的参数如下：

* **Min Value**：滑动条的最小值。
* **Max Value**：滑动条的最大值。
* **Whole Numbers**：是否使用整数值。
  
  >`Whole Numbers`勾选时，拖动滚动条或者直接赋值只能赋值整数。
>`Whole Numbers`未勾选时，可以拖动或者直接赋值`Min Value`和`Max Value`之间的任何值。
  
* **On Value Change **：事件在值发生更改时触发。
* **On Pointer Down**：事件在滑动条被点击按下触发。
* **On Pointer Up**：事件在滑动条被点击抬起时触发。
* **Handler**：滑动条被拖动时的圆点，在`Handler Container`的`BoxCollider`组件`Size`属性上的X轴范围内移动。
  
  >目前只支持在`BoxCollider`的`Size`属性的X轴方向上移动。
