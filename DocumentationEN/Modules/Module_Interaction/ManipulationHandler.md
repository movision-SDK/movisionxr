# ManipulationHandler

![DragComponent.png](../../../Images/Module_Interaction/DragComponent.png)



## How to use ManipulationHandler

![DragComponentInspector.png](../../../Images/Module_Interaction/DragComponentInspector.png)

You need to at least mount the `BoxCollider` component, or the components inherited from `Graphic` in UGUI (such as `Image, RawImage, Text`, etc.) to the game object or or its child game objects with `ManipulationHandler` included. At the same time, you also need to mount the `NearInterationGrabbable` component, which is used for drag-and-drop operations by near-touch hand.
>To mount UGUI-related components, you need to mount the`CanvasCollection` component on the game object in which Canvas is located.

![DragComponent_Target.png](../../../Images/Module_Interaction/DragComponent_Target.png)

Sometimes you want to drag a child game object and then control the position of its parent game object.

![DragComponent_WithTarget.png](../../../Images/Module_Interaction/DragComponent_WithTarget.png)

In this case, you may mount this object to `Target`, to achieve that when dragging the child game object, its parent game object is also dragged.