# API_GSXR_Module_InputSystem


```csharp
Class: public class API_GSXR_Module_InputSystem
```






## GSXR_Get_Instance

获取InputSystem的单例，所有输入的管理类

#### Declaration

```csharp
 public static InputSystem GSXR_Get_Instance()
```


#### Return

| Type | Description                                 |
| :--- | :------------------------------------------ |
| InputSystem  | InputSystem的单例，注意有可能为null |




## GSXR_Is_Initialized

InputSystem是否初始化完成

#### Declaration

```csharp
public static bool GSXR_Is_Initialized()
```

#### Return

| Type | Description                                 |
| :--- | :------------------------------------------ |
| bool | True表初始化完成, False表示初始化未完成 |



## GSXR_Add_InitializedCallBack

InputSystem初始化完成时触发的回调

#### Declaration

```csharp
 public static void GSXR_Add_InitializedCallBack(Action action)
```
> 注意需要和GSXR_Remove_InitializedCallBack保持成对出现
#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| Action | action | Action类型回调function |



## GSXR_Remove_InitializedCallBack

删除InputSystem初始化完成时的回调

#### Declaration

```csharp
 public static GSXR_Remove_InitializedCallBack(Action action)
```
> 注意需要和GSXR_Add_InitializedCallBack保持成对出现
#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| Action | action | Action类型回调function |



## GSXR_Enable_InputDevice

开启InputSystem中的某个输入设备


#### Declaration

```csharp
public static void GSXR_Enable_InputDevice(InputDeviceType inputDevice)
```


#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| InputDeviceType | inputDevice | 输入设备类型，支持设备类型见InputDeviceType |
>InputDeviceType.Head：Head输入设备
InputDeviceType.BT3Dof：蓝牙手柄输入设备
InputDeviceType.KS：游戏控制器输入设备
InputDeviceType.GGT26Dof：灰度手势输入设备





## GSXR_Disable_InputDevice

关闭InputSystem中的某个输入设备


#### Declaration

```csharp
  public static void GSXR_Disable_InputDevice(InputDeviceType inputDevice)
```


#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| InputDeviceType | inputDevice | 输入设备类型，支持设备类型见InputDeviceType |
>InputDeviceType.Head：Head输入设备
InputDeviceType.BT3Dof：蓝牙手柄输入设备
InputDeviceType.KS：游戏控制器输入设备
InputDeviceType.GGT26Dof：灰度手势输入设备






## GSXR_Target

输入设备检测的目标，优先级为Head/BTRight/BTLeft/GGTRight/GGLeft


#### Declaration

```csharp
public static GameObject GSXR_Target
```


#### Returns

| Type         | Description                                   |
| :----------- | :-------------------------------------------- |
| GameObject | 返回输入设备检测的目标组件，目标有可能为null |



## GSXR_Gazer

输入设备的射线起点，优先级为Head/BTRight/BTLeft/GGTRight/GGLeft


#### Declaration

```csharp
public static GameObject GSXR_Gazer;
```

#### Returns

| Type                | Description                                   |
| :------------------ | :-------------------------------------------- |
| GameObject | 返回输入设备的射线起点的组件 |



## GSXR_Normal

输入设备的射线方向，优先级为Head/BTRight/BTLeft/GGTRight/GGLeft

#### Declaration

```csharp
public static Vector3 GSXR_Normal
```


#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| Transform | 返回输入设备的射线方向 |



## GSXR_Position

输入设备Cursor的位置，优先级为Head/BTRight/BTLeft/GGTRight/GGLeft


#### Declaration

```csharp
 public static Vector3 GSXR_Position
```


#### Returns

| Type                | Description          |
| :------------------ | :------------------- |
| Vector3 | 返回输入设备Cursor的位置，全局坐标 |




## GSXR_InputDeviceCurrent

获取当前输入设备，优先级为Head/BTRight/BTLeft/GGTRight/GGLeft


#### Declaration

```csharp
public static InputDevicePartBase GSXR_InputDeviceCurrent
```


#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| InputDevicePartBase | 返回当前输入设备组件 |



## GSXR_InputDeviceStatus

获取指定输入设备的状态


#### Declaration

```csharp
public static bool GSXR_InputDeviceStatus
```


#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| bool | 返回指定输入设备组件的状态 |




## GSXR_HeadDevice

获取Head的输入设备管理类


#### Declaration

```csharp
public static InputDeviceHead GSXR_HeadDevice
```


#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| InputDeviceHead | Head组件，注意有可能为null |




## GSXR_Head

获取Head组件


#### Declaration

```csharp
public static InputDeviceHeadPart GSXR_Head
```


#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| InputDeviceHeadPart | 返回Head组件，注意有可能为null|




## GSXR_HeadRotation

获取Head的四元数


#### Declaration

```csharp
public static Quaternion GSXR_HeadRotation
```


#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| Quaternion  | Head的四元数，全局坐标 |




## GSXR_HeadPosition

获取Head组件的位置


#### Declaration

```csharp
public static Vector3 GSXR_HeadPosition
```


#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| Vector3  | Head组件的位置，全局坐标 |




## GSXR_HeadPointerEventData

获取Head组件碰撞的信息集合

#### Declaration

```csharp
public static SCPointEventData GSXR_HeadPointerEventData
```


#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| SCPointEventData  | 碰撞的信息集合，注意有可能为null |




## GSXR_HeadHitTarget

获取Head组件碰撞的物体


#### Declaration

```csharp
public static GameObject GSXR_HeadHitTarget
```


#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| GameObject  | 空表示未有碰撞物体 |




## GSXR_HeadHitInfo

获取Head组件碰撞信息


#### Declaration

```csharp
public static RaycastResult GSXR_HeadHitInfo
```

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| RaycastResult  | 碰撞信息 |






## GSXR_HeadDragTarget

获取Head组件拖拽的物体


#### Declaration

```csharp
public static GameObject GSXR_HeadDragTarget
```


#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| GameObject  | 推拽的物体，注意有可能为null |






## GSXR_Is_HeadKeyDown

获取Head组件下某个按键是否Down，当前帧有效，下帧复位


#### Declaration

```csharp
public static bool GSXR_Is_HeadKeyDown(InputKeyCode inputKeyCode)
```


#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| InputKeyCode  | inputKeyCode | 指定按键，Head支持指定的按键为Enter/Back |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| bool  | False表示未Down，true表示Down |






## GSXR_Is_HeadKeyUp

获取Head组件下某个按键是否Up，当前帧有效，下帧复位


#### Declaration

```csharp
public static bool GSXR_Is_HeadKeyUp(InputKeyCode inputKeyCode)
```


#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| InputKeyCode  | inputKeyCode | 指定按键，Head支持指定的按键为Enter/Back |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| bool  | False表示未Up，true表示Up |




## GSXR_HeadKeyState

获取Head组件下某个按键的状态，参考UnityAPI:Input.GetKey


#### Declaration

```csharp
public static InputKeyState GSXR_HeadKeyState(InputKeyCode inputKeyCode)
```


#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| InputKeyCode  | inputKeyCode | 指定按键，Head支持指定的按键为Enter/Back |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| InputKeyState   | 指定按键的状态 |








## GSXR_HeadKeyCurrentState

获取Head组件下某个按键的实时状态，参考UnityAPI:Input.GetKey


#### Declaration

```csharp
public static InputKeyState GSXR_HeadKeyCurrentState(InputKeyCode inputKeyCode)
```


#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| InputKeyCode  | inputKeyCode | 指定按键，Head支持指定的按键为Enter/Back |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| InputKeyState   | 指定按键的状态 |




## GSXR_HeadAddKey

给Head组件模拟发送一个按键


#### Declaration

```csharp
public static void GSXR_HeadAddKey(InputKeyCode inputKeyCode, InputKeyState inputKeyState)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| InputKeyCode  | inputKeyCode | 指定按键，Head支持指定的按键为Enter/Back |
| InputKeyState  | inputKeyState | 按键状态（DOWN、UP、LONG和NULL）|

> 发送按键后，下一帧生效，注意发送按键最好需要Down/Up成对出现






## GSXR_Set_HeadRayCastDistance

设置Head组件的检测Collider的范围半径，默认30米


#### Declaration

```csharp
public static void GSXR_Set_HeadRayCastDistance(float distance)
```


#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| float  | distance | 检测Collider的范围半径，单位米 |






## GSXR_Set_HeadEndPointerDistance

设置Head组件的Cursor未碰撞到Collider时的距离，默认3米


#### Declaration

```csharp
public static void GSXR_Set_HeadEndPointerDistance(float distance)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| float  | distance | Cursor未碰撞到Collider时的距离，单位米 |






## GSXR_Get_HeadCursor

获取Head组件的Cursor光标对象


#### Declaration

```csharp
public static DefaultCursor GSXR_Get_HeadCursor
```


#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| DefaultCursor | Head组件的Cursor光标对象 |






##  GSXR_BTDevice

获取手柄输入设备管理类


#### Declaration

```csharp
public static InputDeviceBT3Dof  GSXR_BTDevice
```


#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| InputDeviceBT3Dof | 手柄输入设备，注意有可能为null |




##  GSXR_BTRight

获取第一个连接的手柄组件


#### Declaration

```csharp
public static InputDeviceBT3DofPart  GSXR_BTRight
```


#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| InputDeviceBT3DofPart | 第一个连接的手柄组件，注意有可能为null |




##  GSXR_BTLeft

获取第二个连接的手柄组件


#### Declaration

```csharp
public static InputDeviceBT3DofPart  GSXR_BTLeft
```


#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| InputDeviceBT3DofPart | 第二个连接的手柄组件，注意有可能为null |




##  GSXR_BTRotation

获取手柄组件的旋转


#### Declaration

```csharp
public static Quaternion  GSXR_BTRotation(BTType type = BTType.Right)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| BTType  | type | BTType.Right表示第一个连接的手柄组件(默认),BTType.Left表示第二个连接的手柄组件 |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| Quaternion | 手柄组件的旋转值的四元数，全局坐标 |






##  GSXR_BTPosition

获取手柄组件的位置


#### Declaration

```csharp
public static Vector3  GSXR_BTPosition(BTType type = BTType.Right)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| BTType  | type | BTType.Right表示第一个连接的手柄组件(默认),BTType.Left表示第二个连接的手柄组件 |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| Vector3 | 手柄组件的位置，全局坐标 |






## GSXR_Is_BTTpTouch

获取手柄组件的是否触摸了TouchPanel


#### Declaration

```csharp
public static bool GSXR_Is_BTTpTouch(BTType type = BTType.Right)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| BTType  | type | BTType.Right表示第一个连接的手柄组件(默认),BTType.Left表示第二个连接的手柄组件 |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| bool | True表示触摸，false表示未触摸 |






## GSXR_BTTpTouchInfo

获取手柄组件的触摸的位置信息（x,y）


#### Declaration

```csharp
public static Vector2 GSXR_BTTpTouchInfo(BTType type = BTType.Right)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| BTType  | type | BTType.Right表示第一个连接的手柄组件(默认),BTType.Left表示第二个连接的手柄组件 |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| Vector2 | 手柄组件的触摸的位置信息（x,y） |





## GSXR_BTName

获取手柄组件的名字


#### Declaration

```csharp
public static string GSXR_BTName(BTType type = BTType.Right)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| BTType  | type | BTType.Right表示第一个连接的手柄组件(默认),BTType.Left表示第二个连接的手柄组件 |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| string |手柄组件的名字，K02或K07 |





## GSXR_BTPointerEventData

获取手柄组件的碰撞信息集合


#### Declaration

```csharp
public static SCPointEventData GSXR_BTPointerEventData(BTType type = BTType.Right)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| BTType  | type | BTType.Right表示第一个连接的手柄组件(默认),BTType.Left表示第二个连接的手柄组件 |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| SCPointEventData | 手柄组件的碰撞信息集合，注意有可能为null |





## GSXR_BTHitTarget

获取手柄组件碰撞的Collider物体


#### Declaration

```csharp
public static GameObject GSXR_BTHitTarget(BTType type = BTType.Right)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| BTType  | type | BTType.Right表示第一个连接的手柄组件(默认),BTType.Left表示第二个连接的手柄组件 |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| GameObject | 返回手柄组件碰撞的Collider物体 |




## GSXR_BTHitInfo

获取手柄组件碰撞的Collider具体信息


#### Declaration

```csharp
public static RaycastResult GSXR_BTHitInfo(BTType type = BTType.Right)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| BTType  | type | BTType.Right表示第一个连接的手柄组件(默认),BTType.Left表示第二个连接的手柄组件 |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| RaycastResult | 手柄组件碰撞的Collider具体信息 |



## GSXR_BTDragTarget

获取手柄组件拖拽的物体


#### Declaration

```csharp
public static GameObject GSXR_BTDragTarget(BTType type = BTType.Right)
```


#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| GameObject | 手柄组件拖拽的物体 |






## GSXR_Is_BTKeyDown

获取手柄组件是否按下指定按键


#### Declaration

```csharp
public static bool GSXR_Is_BTKeyDown(InputKeyCode inputKeyCode, BTType type = BTType.Right)
```
#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| InputKeyCode  | inputKeyCode | 指定按键，HandShank支持Enter(Trigger)/Back/Funcion/Tp |
| BTType  | type | BTType.Right表示第一个连接的手柄组件(默认),BTType.Left表示第二个连接的手柄组件 |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| bool | True表示按下，false表示未按下 |






## GSXR_Is_BTKeyUp

获取手柄组件是否抬起指定按键


#### Declaration

```csharp
public static bool GSXR_Is_BTKeyUp(InputKeyCode inputKeyCode, BTType type = BTType.Right)
```
#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| InputKeyCode  | inputKeyCode | 指定按键，HandShank支持Enter(Trigger)/Back/Funcion/Tp |
| BTType  | type | BTType.Right表示第一个连接的手柄组件(默认),BTType.Left表示第二个连接的手柄组件 |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| bool | True表示触发，false表示未触发 |





## GSXR_BTKeyState

获取type手柄组件inputKeyCode键的状态


#### Declaration

```csharp
public static InputKeyState GSXR_BTKeyState(InputKeyCode inputKeyCode, BTType type = BTType.Right)
```
#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| InputKeyCode  | inputKeyCode | 指定按键，HandShank支持Enter(Trigger)/Back/Funcion/Tp |
| BTType  | type | BTType.Right表示第一个连接的手柄组件(默认),BTType.Left表示第二个连接的手柄组件 |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| InputKeyState | 手柄组件inputKeyCode键的状态 |






## GSXR_BTKeyCurrentState

获取手柄组件inputKeyCode键的实时状态


#### Declaration

```csharp
public static InputKeyState GSXR_BTKeyCurrentState(InputKeyCode inputKeyCode, BTType type = BTType.Right)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| InputKeyCode  | inputKeyCode | 指定按键，HandShank支持Enter(Trigger)/Back/Funcion/Tp |
| BTType  | type | BTType.Right表示第一个连接的手柄组件(默认),BTType.Left表示第二个连接的手柄组件 |


#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| InputKeyState  | 手柄组件inputKeyCode键的实时状态 |





## GSXR_BTKeyAddKey

模拟给手柄组件发送一个按键


#### Declaration

```csharp
public static void GSXR_BTKeyAddKey(InputKeyCode inputKeyCode, InputKeyState inputKeyState, BTType type = BTType.Right)
```
#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| InputKeyCode  | inputKeyCode | 指定按键，HandShank支持Enter(Trigger)/Back/Funcion/Tp |
| InputKeyState  | inputKeyState | 指定按键状态，注意发送按键最好需要Down/Up成对出现 |
| BTType  | type | BTType.Right表示第一个连接的手柄组件(默认),BTType.Left表示第二个连接的手柄组件 |





## GSXR_Set_BTRayCastDistance

设置手柄组件检测Collider的范围半径，默认30米


#### Declaration

```csharp
public static void GSXR_Set_BTRayCastDistance(float distance, BTType type = BTType.Right)
```
#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| float  | Distance | type手柄组件检测Collider的范围半径，单位米|
| BTType  | type | BTType.Right表示第一个连接的手柄组件(默认),BTType.Left表示第二个连接的手柄组件 |





## GSXR_Set_BTEndPointerDistance

设置手柄组件未检测到Collider光束的半径，默认3米


#### Declaration

```csharp
public static void GSXR_Set_BTEndPointerDistance(float distance, BTType type = BTType.Right)
```
#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| float  | Distance | type手柄组件检测Collider的范围半径，单位米|
| BTType  | type | BTType.Right表示第一个连接的手柄组件(默认),BTType.Left表示第二个连接的手柄组件 |





## GSXR_Get_BTCursor

获取手柄组件的Cursor光标对象


#### Declaration

```csharp
public static DefaultCursor GSXR_Get_BTCursor(BTType type = BTType.Right)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| BTType  | type | BTType.Right表示第一个连接的手柄组件(默认),BTType.Left表示第二个连接的手柄组件 |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| DefaultCursor  | 手柄组件的Cursor光标对象，注意有可能为null |





## GSXR_Get_BTLine

获取手柄组件的光束对象


#### Declaration

```csharp
public static LineRenderer GSXR_Get_BTLine(BTType type = BTType.Right)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| BTType  | type | BTType.Right表示第一个连接的手柄组件(默认),BTType.Left表示第二个连接的手柄组件 |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| LineRenderer  | 手柄组件的光束对象，注意有可能为null |





## GSXR_Enable_BT

开启手柄组件


#### Declaration

```csharp
public static void GSXR_Enable_BT(BTType type = BTType.Right)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| BTType  | type | BTType.Right表示第一个连接的手柄组件(默认),BTType.Left表示第二个连接的手柄组件 |






## GSXR_Disable_BT

关闭type手柄组件


#### Declaration

```csharp
public static void GSXR_Disable_BT(BTType type = BTType.Right)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| BTType  | type | BTType.Right表示第一个连接的手柄组件(默认),BTType.Left表示第二个连接的手柄组件 |





## GSXR_Get_Acc

获取手柄的ACC数据


#### Declaration

```csharp
public static int[] GSXR_Get_Acc(BTType type = BTType.Right)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| BTType  | type | BTType.Right表示第一个连接的手柄组件(默认),BTType.Left表示第二个连接的手柄组件 |




## GSXR_Get_Gyro

获取手柄的Gyro数据


#### Declaration

```csharp
public static int[] GSXR_Get_Gyro(BTType type = BTType.Right)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| BTType  | type | BTType.Right表示第一个连接的手柄组件(默认),BTType.Left表示第二个连接的手柄组件 |





## GSXR_GGT26DofDevice

获取手势输入设备管理类


#### Declaration

```csharp
public static InputDeviceHand GSXR_GGT26DofDevice
```


#### Returns

| Type                    | Description                    |
| :---------------------- | :----------------------------- |
| InputDeviceHand | 手势输入设备，注意有可能为null |




## GSXR_GGTLeft

获取手势左手组件


#### Declaration

```csharp
public static InputDeviceGGT26DofPart GSXR_GGTLeft
```


#### Returns

| Type                        | Description |
| :-------------------------- | :---------- |
| InputDeviceGGT26DofPart | 左手组件    |




## GSXR_GGTRight

获取手势右手组件


#### Declaration

```csharp
public static InputDeviceGGT26DofPart GSXR_GGTRight
```


#### Returns

| Type                        | Description |
| :-------------------------- | :---------- |
| InputDeviceGGT26DofPart | 右手组件    |




## GSXR_GGThandInfo

获取手势组件的handInfo结构，handInfo包含手势的各类数据


#### Declaration

```csharp
public static handInfo GSXR_GGThandInfo(GGestureType type = GGestureType.Right)
```

#### Parameters

| Type        | Name | Description                                                  |
| :---------- | :--- | :----------------------------------------------------------- |
| GGestureType | type | GGestureType.Right表示右手组件（默认值），GGestureType.Left表示左手组件 |

#### Returns

| Type     | Description            |
| :------- | :--------------------- |
| handInfo | 手势组件的handInfo结构 |






## GSXR_GGTPointerEventData

获取手势组件碰撞信息集合


#### Declaration

```csharp
public static SCPointEventData GSXR_GGTPointerEventData(GGestureType type = GGestureType.Right)
```

#### Parameters

| Type        | Name | Description                                                  |
| :---------- | :--- | :----------------------------------------------------------- |
| GGestureType | type | GGestureType.Right表示右手组件（默认值），GGestureType.Left表示左手组件 |

#### Returns

| Type             | Description          |
| :--------------- | :------------------- |
| SCPointEventData | 手势组件碰撞信息集合 |






## GSXR_GGTHitTarget

获取手势组件碰撞Collider物体


#### Declaration

```csharp
public static GameObject GSXR_GGTHitTarget(GGestureType type = GGestureType.Right)
```

#### Parameters

| Type        | Name | Description                                                  |
| :---------- | :--- | :----------------------------------------------------------- |
| GGestureType | type | GGestureType.Right表示右手组件（默认值），GGestureType.Left表示左手组件 |

#### Returns

| Type       | Description                  |
| :--------- | :--------------------------- |
| GameObject | 返回碰撞的物体，有可能为null |






## GSXR_GGTHitInfo

获取手势组件碰撞Collider的RaycastHit结构


#### Declaration

```csharp
public static RaycastResult GSXR_GGTHitInfo(GGestureType type = GGestureType.Right)
```

#### Parameters

| Type        | Name | Description                                                  |
| :---------- | :--- | :----------------------------------------------------------- |
| GGestureType | type | GGestureType.Right表示右手组件（默认值），GGestureType.Left表示左手组件 |

#### Returns

| Type       | Description                          |
| :--------- | :----------------------------------- |
| RaycastResult | 手势组件碰撞Collider的RaycastHit结构 |





## GSXR_GGTDragTarget

获取手势组件拖拽的物体


#### Declaration

```csharp
public static GameObject GSXR_GGTDragTarget(GGestureType type = GGestureType.Right)
```

#### Parameters

| Type        | Name | Description                                                  |
| :---------- | :--- | :----------------------------------------------------------- |
| GGestureType | type | GGestureType.Right表示右手组件（默认值），GGestureType.Left表示左手组件 |

#### Returns

| Type       | Description        |
| :--------- | :----------------- |
| GameObject | 手势组件拖拽的物体 |






## GSXR_Is_GGTKeyDown

判断手势组件是否触发某个Key Down


#### Declaration

```csharp
public static bool GSXR_Is_GGTKeyDown(InputKeyCode inputKeyCode, GGestureType type = GGestureType.Right)
```

#### Parameters

| Type         | Name         | Description                                                  |
| :----------- | :----------- | :----------------------------------------------------------- |
| InputKeyCode | inputKeyCode | inputKeyCode:指定按键,暂时只支持Enter按键                    |
| GGestureType  | type         | GGestureType.Right表示右手组件（默认值），GGestureType.Left表示左手组件 |

#### Returns

| Type | Description                   |
| :--- | :---------------------------- |
| bool | True表示触发，false表示未触发 |






## GSXR_Is_GGTKeyUp

判断手势组件是否触发某个Key Up


#### Declaration

```csharp
public static bool GSXR_Is_GGTKeyUp(InputKeyCode inputKeyCode, GGestureType type = GGestureType.Right)
```

#### Parameters

| Type         | Name         | Description                                                  |
| :----------- | :----------- | :----------------------------------------------------------- |
| InputKeyCode | inputKeyCode | 指定按键,暂时只支持Enter按键                                 |
| GGestureType  | type         | GGestureType.Right表示右手组件（默认值），GGestureType.Left表示左手组件 |

#### Returns

| Type | Description                   |
| :--- | :---------------------------- |
| bool | True表示触发，false表示未触发 |





## GSXR_GGTKeyState

获取手势组件某个Key的状态


#### Declaration

```csharp
public static InputKeyState GSXR_GGTKeyState(InputKeyCode inputKeyCode, GGestureType type = GGestureType.Right)
```

#### Parameters

| Type         | Name         | Description                                                  |
| :----------- | :----------- | :----------------------------------------------------------- |
| InputKeyCode | inputKeyCode | inputKeyCode:指定按键,暂时只支持Enter按键                    |
| GGestureType  | type         | GGestureType.Right表示右手组件（默认值），GGestureType.Left表示左手组件 |

#### Returns

| Type          | Description    |
| :------------ | :------------- |
| InputKeyState | 指定按键的状态 |






## GSXR_GGTKeyCurrentState

获取手势组件某个Key的实时状态


#### Declaration

```csharp
public static InputKeyState GSXR_GGTKeyCurrentState(InputKeyCode inputKeyCode, GGestureType type = GGestureType.Right)
```

#### Parameters

| Type         | Name         | Description                                                  |
| :----------- | :----------- | :----------------------------------------------------------- |
| InputKeyCode | inputKeyCode | inputKeyCode:指定按键,暂时只支持Enter按键                    |
| GGestureType  | type         | GGestureType.Right表示右手组件（默认值），GGestureType.Left表示左手组件 |

#### Returns

| Type          | Description                  |
| :------------ | :--------------------------- |
| InputKeyState | 指定按键,暂时只支持Enter按键 |





## GSXR_GGTKeyAddKey

模拟手势组件发送一个按键


#### Declaration

```csharp
public static void GSXR_GGTKeyAddKey(InputKeyCode inputKeyCode, InputKeyState inputKeyState, GGestureType type = GGestureType.Right)
```

#### Parameters

| Type          | Name          | Description                                                  |
| :------------ | :------------ | :----------------------------------------------------------- |
| InputKeyCode  | inputKeyCode  | 指定按键,暂时只支持Enter按键                                 |
| InputKeyState | inputKeyState | 指定按键状态，注意发送按键最好需要Down/Up成对出现            |
| GGestureType   | type          | GGestureType.Right表示右手组件（默认值），GGestureType.Left表示左手组件 |





## GSXR_Set_GGTRayCastDistance

设置手势组件检测Collider的半径范围，默认30米


#### Declaration

```csharp
public static void GSXR_Set_GGTRayCastDistance(float distance, GGestureType type = GGestureType.Right)
```

#### Parameters

| Type        | Name     | Description                                                  |
| :---------- | :------- | :----------------------------------------------------------- |
| float       | Distance | type手柄组件检测Collider的范围半径，单位米                   |
| GGestureType | type     | GGestureType.Right表示右手组件（默认值），GGestureType.Left表示左手组件 |





## GSXR_Set_GGTEndPointerDistance

设置手势组件未检测到Collider时，Cursor的位置半径，默认3米


#### Declaration

```csharp
public static void GSXR_Set_GGTEndPointerDistance(float distance, GGestureType type = GGestureType.Right)
```

#### Parameters

| Type        | Name     | Description                                                  |
| :---------- | :------- | :----------------------------------------------------------- |
| float       | Distance | type手柄组件检测Collider的范围半径，单位米                   |
| GGestureType | type     | GGestureType.Right表示右手组件（默认值），GGestureType.Left表示左手组件 |





## GSXR_Get_GGTCursor

获取手势组件的Cursor


#### Declaration

```csharp
public static DefaultCursor GSXR_Get_GGTCursor(GGestureType type = GGestureType.Right)
```

#### Parameters

| Type        | Name | Description                                                  |
| :---------- | :--- | :----------------------------------------------------------- |
| GGestureType | type | GGestureType.Right表示右手组件（默认值），GGestureType.Left表示左手组件 |

#### Returns

| Type  | Description     |
| :---- | :-------------- |
| DefaultCursor | 手势组件的Cursor |





## GSXR_Get_GGTLine

获取手势组件的光束


#### Declaration

```csharp
public static LineRenderer GSXR_Get_GGTLine(GGestureType type = GGestureType.Right)
```

#### Parameters

| Type        | Name | Description                                                  |
| :---------- | :--- | :----------------------------------------------------------- |
| GGestureType | type | GGestureType.Right表示右手组件（默认值），GGestureType.Left表示左手组件 |

#### Returns

| Type         | Description    |
| :----------- | :------------- |
| LineRenderer | 手势组件的光束 |





## GSXR_Enable_GGT

开启手势组件


#### Declaration

```csharp
public static void GSXR_Enable_GGT(GGestureType type = GGestureType.Right)
```

#### Parameters

| Type        | Name | Description                                                  |
| :---------- | :--- | :----------------------------------------------------------- |
| GGestureType | type | GGestureType.Right表示右手组件（默认值），GGestureType.Left表示左手组件 |






## GSXR_Disable_GGT

关闭手势组件


#### Declaration

```csharp
public static void GSXR_Disable_GGT(GGestureType type = GGestureType.Right)
```

#### Parameters

| Type        | Name | Description                                                  |
| :---------- | :--- | :----------------------------------------------------------- |
| GGestureType | type | GGestureType.Right表示右手组件（默认值），GGestureType.Left表示左手组件 |





## GSXR_Get_FingerUI

获取手势组件fingerUI的结构


#### Declaration

```csharp
public static Model26DofGesture.FingerUI[] GSXR_Get_FingerUI(GGestureType type = GGestureType.Right)
```
#### Parameters

| Type        | Name | Description                                                  |
| :---------- | :--- | :----------------------------------------------------------- |
| GGestureType | type | GGestureType.Right表示右手组件（默认值），GGestureType.Left表示左手组件 |

#### Returns

| Type                       | Description            |
| :------------------------- | :--------------------- |
| Model26DofGesture.FingerUI[] | 手势组件fingerUI的结构 |







## GSXR_KSDevice

获取游戏控制器输入设备管理类


#### Declaration

```csharp
public static InputDeviceKS GSXR_KSDevice
```


#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| InputDeviceKS | 游戏控制器输入设备，注意有可能为null |




## GSXR_KSRight

获取第一个连接的游戏控制器组件


#### Declaration

```csharp
public static InputDeviceKSPart GSXR_KSRight;
```


#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| InputDeviceKSPart | 第一个连接的游戏控制器组件，注意有可能为null |




## GSXR_KSLeft

获取第二个连接的游戏控制器组件


#### Declaration

```csharp
public static InputDeviceKSPart GSXR_KSLeft;
```


#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| InputDeviceKSPart | 第二个连接的游戏控制器组件，注意有可能为null |




## GSXR_KSRotation

获取游戏控制器组件的旋转


#### Declaration

```csharp
public static Quaternion  GSXR_KSRotation(GCType type = GCType.Right)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| GCType  | type | GCType.Right表示第一个连接的游戏控制器组件(默认),GCType.Left表示第二个连接的游戏控制器组件 |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| Quaternion | 游戏控制器组件的旋转值的四元数，全局坐标 |






## GSXR_KSPosition

获取游戏控制器组件的位置


#### Declaration

```csharp
public static Vector3 GSXR_KSPosition(GCType type = GCType.Right)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| GCType  | type | GCType.Right表示第一个连接的游戏控制器组件(默认),GCType.Left表示第二个连接的游戏控制器组件 |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| Vector3 | 游戏控制器组件的位置，全局坐标 |






## GSXR_KSTransform

获取游戏控制器的Transform组件


#### Declaration

```csharp
public static Transform GSXR_KSTransform(GCType type = GCType.Right)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| GCType  | type | GCType.Right表示第一个连接的游戏控制器组件(默认),GCType.Left表示第二个连接的游戏控制器组件 |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| Transform | 游戏控制器的Transform组件，全局坐标 |






## GSXR_KSName

获取游戏控制器组件的名字


#### Declaration

```csharp
public static string GSXR_KSName(GCType type = GCType.Right)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| GCType  | type | GCType.Right表示第一个连接的手柄组件(默认),GCType.Left表示第二个连接的手柄组件 |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| string |游戏控制器组件的名字，K11或K102 |





## GSXR_KSPointerEventData

获取游戏控制器组件的碰撞信息集合


#### Declaration

```csharp
public static SCPointEventData GSXR_KSPointerEventData(GCType type = GCType.Right)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| GCType  | type | GCType.Right表示第一个连接的游戏控制器组件(默认),GCType.Left表示第二个连接的游戏控制器组件 |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| SCPointEventData | 游戏控制器组件的碰撞信息集合，注意有可能为null |





## GSXR_KSHitTarget

获取游戏控制器组件碰撞的Collider物体


#### Declaration

```csharp
public static GameObject GSXR_KSHitTarget(GCType type = GCType.Right)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| GCType  | type | GCType.Right表示第一个连接的游戏控制器组件(默认),GCType.Left表示第二个连接的游戏控制器组件 |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| GameObject | 返回游戏控制器组件碰撞的Collider物体 |




## GSXR_KSHitInfo

获取游戏控制器组件碰撞的Collider具体信息


#### Declaration

```csharp
public static RaycastResult GSXR_KSHitInfo(GCType type = GCType.Right)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| GCType  | type | GCType.Right表示第一个连接的游戏控制器组件(默认),GCType.Left表示第二个连接的游戏控制器组件 |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| RaycastResult | 游戏控制器组件碰撞的Collider具体信息 |



## GSXR_KSDragTarget

获取游戏控制器组件拖拽的物体


#### Declaration

```csharp
public static GameObject GSXR_KSDragTarget(GCType type = GCType.Right)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| GCType  | type | GCType.Right表示第一个连接的游戏控制器组件(默认),GCType.Left表示第二个连接的游戏控制器组件 |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| GameObject | 游戏控制器组件拖拽的物体 |






## GSXR_Is_KSKeyDown

获取游戏控制器组件是否触发按下指定按键


#### Declaration

```csharp
public static bool GSXR_Is_KSKeyDown(InputKeyCode inputKeyCode, GCType type = GCType.Right)
```
#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| InputKeyCode  | inputKeyCode | 指定按键，HandShank支持Enter(Trigger)/Back/Funcion/Tp |
| GCType  | type | GCType.Right表示第一个连接的游戏控制器组件(默认),GCType.Left表示第二个连接的游戏控制器组件 |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| bool | True表示按下，false表示未按下 |






## GSXR_Is_KSKeyUp

获取游戏控制器组件是否触发抬起指定按键


#### Declaration

```csharp
public static bool GSXR_Is_KSKeyUp(InputKeyCode inputKeyCode, GCType type = GCType.Right)
```
#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| InputKeyCode  | inputKeyCode | 指定按键，HandShank支持Enter(Trigger)/Back/Funcion/Tp |
| GCType  | type | GCType.Right表示第一个连接的游戏控制器组件(默认),GCType.Left表示第二个连接的游戏控制器组件 |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| bool | True表示触发，false表示未触发 |





## GSXR_KSKeyState

获取游戏控制器组件inputKeyCode键的状态


#### Declaration

```csharp
public static InputKeyState GSXR_KSKeyState(InputKeyCode inputKeyCode, GCType type = GCType.Right)
```
#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| InputKeyCode  | inputKeyCode | 指定按键，HandShank支持Enter(Trigger)/Back/Funcion/Tp |
| GCType  | type | GCType.Right表示第一个连接的游戏控制器组件(默认),GCType.Left表示第二个连接的游戏控制器组件 |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| InputKeyState | 游戏控制器组件inputKeyCode键的状态 |






## GSXR_KSKeyCurrentState

获取游戏控制器组件inputKeyCode键的实时状态


#### Declaration

```csharp
public static InputKeyState GSXR_KSKeyCurrentState(InputKeyCode inputKeyCode, GCType type = GCType.Right)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| InputKeyCode  | inputKeyCode | 指定按键，HandShank支持Enter(Trigger)/Back/Funcion/Tp |
| GCType  | type | GCType.Right表示第一个连接的游戏控制器组件(默认),GCType.Left表示第二个连接的游戏控制器组件 |


#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| InputKeyState  | 游戏控制器组件inputKeyCode键的实时状态 |





## GSXR_KSKeyAddKey

模拟给游戏控制器组件发送一个按键


#### Declaration

```csharp
public static void GSXR_KSKeyAddKey(InputKeyCode inputKeyCode, InputKeyState inputKeyState, GCType type = GCType.Right)
```
#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| InputKeyCode  | inputKeyCode | 指定按键，HandShank支持Enter(Trigger)/Back/Funcion/Tp |
| InputKeyState  | inputKeyState | 指定按键状态，注意发送按键最好需要Down/Up成对出现 |
| GCType  | type | GCType.Right表示第一个连接的游戏控制器组件(默认),GCType.Left表示第二个连接的游戏控制器组件 |





## GSXR_Set_KSRayCastDistance

设置游戏控制器组件检测Collider的范围半径，默认30米


#### Declaration

```csharp
public static void GSXR_Set_KSRayCastDistance(float distance, GCType type = GCType.Right)
```
#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| float  | Distance | 游戏控制器组件检测Collider的范围半径，单位米|
| GCType  | type | GCType.Right表示第一个连接的游戏控制器组件(默认),BTType.Left表示第二个连接的游戏控制器件 |





## GSXR_Set_KSEndPointerDistance

设置游戏控制器组件未检测到Collider光束的半径，默认3米


#### Declaration

```csharp
public static void GSXR_Set_KSEndPointerDistance(float distance, GCType type = GCType.Right)
```
#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| float  | Distance | 游戏控制器组件检测Collider的范围半径，单位米|
| GCType  | type | GCType.Right表示第一个连接的游戏控制器组件(默认),GCType.Left表示第二个连接的游戏控制器组件 |





## GSXR_Get_KSCursor

获取游戏控制器组件的Cursor光圈对象


#### Declaration

```csharp
public static DefaultCursor GSXR_Get_KSCursor(GCType type = GCType.Right)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| GCType  | type | GCType.Right表示第一个连接的游戏控制器组件(默认),GCType.Left表示第二个连接的游戏控制器组件 |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| DefaultCursor  | 游戏控制器组件的Cursor光标对象，注意有可能为null |





## GSXR_Get_KSLine

获取游戏控制器组件的光束对象


#### Declaration

```csharp
public static LineRenderer GSXR_Get_KSLine(GCType type = GCType.Right)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| GCType  | type | GCType.Right表示第一个连接的游戏控制器组件(默认),GCType.Left表示第二个连接的游戏控制器组件 |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| LineRenderer  | 游戏控制器组件的光束对象，注意有可能为null |





## GSXR_Enable_KS

开启指定游戏控制器组件


#### Declaration

```csharp
public static void GSXR_Enable_KS(BTType type = BTType.Right)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| GCType  | type | GCType.Right表示第一个连接的游戏控制器组件(默认),GCType.Left表示第二个连接的游戏控制器组件 |






## GSXR_Disable_KS

关闭指定游戏控制器组件


#### Declaration

```csharp
public static void GSXR_Disable_KS(GCType type = GCType.Right)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| GCType  | type | GCType.Right表示第一个连接的游戏控制器组件(默认),GCType.Left表示第二个连接的游戏控制器组件 |






