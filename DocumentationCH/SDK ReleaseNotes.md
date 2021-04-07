# SDK Release Notes



## SDK4.1.2版本新功能



### 添加三种手势交互方式

- **FarPointer**：远处手势交互
- **TouchPointer**：近处手势交互
- **GrabPointer**：抓取手势交互


- **NearInteractionTouchable**：挂载该脚本的3D游戏对象可以被近处手势交互
- **NearInteractionTouchableUnityUI**：挂载该脚本的UGUI游戏对象可以被近处手势交互
- **NearInteractionGrabbable**：挂载该脚本的游戏对象可以被抓取手势交互



### UGUI事件系统支持

- **CanvasCollection**：需要向`Canvas`游戏对象挂载该脚本使SDK可以对UGUI游戏对象交互



### BoundingBox和ManipulationHandler

- [BoundingBox](../Modules/Module_Interaction/BoundingBox.md) - 组件用于物体的旋转和缩放
- [ManipulationHandler](../Modules/Module_Interaction/ManipulationHandler.md) - 组件用于物体的拖拽



### 新的3DUI组件

- [SCImage3D](../Modules/Module_Interaction/SCImage3D.md) - 用于创建3D版本Image组件
- [SCInputField](../Modules/Module_Interaction/SCInputField.md) - 弹出3D键盘的InputField组件
- [SCSlider3D](../Modules/Module_Interaction/SCSlider3D.md) - 基于`BoxCollider`的Slider组件
- [SCToggle3D](../Modules/Module_Interaction/SCToggle3D.md) - 基于`BoxCollider`的Toggle组件



### 额外的手势触摸事件

- [IPokeDownHandler](../Modules/Module_Interaction/HandTouch.md) - 食指进入`Collider`组件时触发的事件
- [IPokeUpHandler](../Modules/Module_Interaction/HandTouch.md) - 食指离开`Collider`组件时触发的事件
- [IPokeUpdateHandler](../Modules/Module_Interaction/HandTouch.md) - 食指在`Collider`组件中每一帧触发的事件





## SDK4.1.2已知问题



### Unity2019.3.x版本会有内存泄漏问题



### 近处手势点击方向目前只支持Z轴负方向

建议将需要手势操作的游戏对象的Z轴负方向面向操作者



### SCImage3D不支持Sprite

目前只支持Texture2D，对九宫格相关的图片不友好



### Drag影响点击的问题

由于射线相关操作的稳定性没有鼠标高，点击时轻微抖动可能会触发Drag事件，目前的临时解决方案是将`EventSystem`组件上的Drag Threhold值适当调大
