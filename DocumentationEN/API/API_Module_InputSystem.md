# API_GSXR_Module_InputSystem


```csharp
Class: public class API_GSXR_Module_InputSystem
```






## GSXR_Get_Instance

Get a singleton of InputSystem. This is the manager class of all inputs.

#### Declaration

```csharp
 public static InputSystem GSXR_Get_Instance()
```


#### Return

| Type | Description                                 |
| :--- | :------------------------------------------ |
| InputSystem  | Singleton of InputSystem, note that it can be null |




## GSXR_Is_Initialized

Whether the InputSystem initialization has been completed

#### Declaration

```csharp
public static bool GSXR_Is_Initialized()
```

#### Return

| Type | Description                                 |
| :--- | :------------------------------------------ |
| bool | True: initialization has been completedFalse: initialization has not been completed|



## GSXR_Add_InitializedCallBack

Callback triggered by the completion of the InputSystem initialization

#### Declaration

```csharp
 public static void GSXR_Add_InitializedCallBack(Action action)
```
#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| Action | action | Action type callback function |



## GSXR_Remove_InitializedCallBack

Delete the callback triggered by the completion of the InputSystem initialization

#### Declaration

```csharp
 public static GSXR_Remove_InitializedCallBack(Action action)
```
#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| Action | action | Action type callback function |



## GSXR_Enable_InputDevice

Enable an InputSystem device


#### Declaration

```csharp
public static void GSXR_Enable_InputDevice(InputDeviceType inputDevice)
```


#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| InputDeviceType | inputDevice | Enable the device, see the supported devices in InputDeviceType |
>InputDeviceType.Head: Head-Mounted Display input device
InputDeviceType.BT3Dof : Bluetooth 3Dof controller input device
InputDeviceType.GGT26Dof:  Hand Tracking input device





## GSXR_Disable_InputDevice

Disable an InputSystem device


#### Declaration

```csharp
  public static void GSXR_Disable_InputDevice(InputDeviceType inputDevice)
```


#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| InputDeviceType | inputDevice | Disable the device, see the supported devices in InputDeviceType |
>InputDeviceType.Head: Head-Mounted Display input device
InputDeviceType.BT3Dof : Bluetooth 3Dof controller input device
InputDeviceType.GGT26Dof:  Hand Tracking input device






## GSXR_Target

Target of the input device detection. The priority is set as Head/BTRight/BTLeft/GGTRight/GGTLeft.


#### Declaration

```csharp
public static GameObject GSXR_Target
```


#### Returns

| Type         | Description                                   |
| :----------- | :-------------------------------------------- |
| GameObject | Return the target component of the input device detection, note that the target can be null |



## GSXR_Gazer

The ray start point of the input device. The priority is set as Head/BTRight/BTLeft/GGTRight/GGTLeft.


#### Declaration

```csharp
public static GameObject GSXR_Gazer
```

#### Returns

| Type                | Description                                   |
| :------------------ | :-------------------------------------------- |
| GameObject |Return the ray start point component of the input device|



## GSXR_Normal

The ray direction of the input device. The priority is set as Head/BTRight/BTLeft/GGTRight/GGLeft

#### Declaration

```csharp
public static Vector3 GSXR_Normal
```


#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| Transform | Return the ray direction of the input device |



## GSXR_Position

The Cursor position of the input device. The priority is set as Head/BTRight/BTLeft/GGTRight/GGLeft


#### Declaration

```csharp
 public static Vector3 GSXR_Position
```


#### Returns

| Type                | Description          |
| :------------------ | :------------------- |
| Vector3 | Return the Cursor position of the input device, global coordinates |




## GSXR_InputDeviceCurrent

Get the current input device. The priority is set as Head/BTRight/BTLeft/GGTRight/GGLeft


#### Declaration

```csharp
public static InputDevicePartBase GSXR_InputDeviceCurrent
```


#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| InputDevicePartBase | Return the current input device component |


## GSXR_InputDeviceStatus

Get the specified input device status


#### Declaration

```csharp
public static bool GSXR_InputDeviceStatus
```


#### Returns

| Type | Description                |
| :--- | :------------------------- |
| bool | Return the specified input device status |





## GSXR_HeadDevice

Get the manager class of the Head input device


#### Declaration

```csharp
public static InputDeviceHead GSXR_HeadDevice
```


#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| InputDeviceHead |Return the Head component, note that it can be null |




## GSXR_Head

Get the Head component


#### Declaration

```csharp
public static InputDeviceHeadPart GSXR_Head
```


#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| InputDeviceHeadPart | Return the Head component, note that it can be null|




## GSXR_HeadRotation

Get the Quaternion of Head


#### Declaration

```csharp
public static Quaternion GSXR_HeadRotation
```


#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| Quaternion  | Return the Quaternion of Head, global coordinates |




## GSXR_HeadPosition

Get the position of the Head component


#### Declaration

```csharp
public static Vector3 GSXR_HeadPosition
```


#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| Vector3  | Return the position of the Head component, global coordinates |




## GSXR_HeadPointerEventData

Get the hit information collection of the Head component

#### Declaration

```csharp
public static SCPointEventData GSXR_HeadPointerEventData
```


#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| SCPointEventData  | Return the hit information collection of the Head component, note that it can be null |




## GSXR_HeadHitTarget

Get the hit object of the Head component


#### Declaration

```csharp
public static GameObject GSXR_HeadHitTarget
```


#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| GameObject  | Null: no hit object |




## GSXR_HeadHitInfo

Get the hit information of the Head component


#### Declaration

```csharp
public static RaycastResult GSXR_HeadHitInfo
```

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| RaycastResult  | Return the hit information |






## GSXR_HeadDragTarget

Get the draggable object of the Head component


#### Declaration

```csharp
public static GameObject GSXR_HeadDragTarget
```


#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| GameObject  | Return the draggable object, note that it can be null |






## GSXR_Is_HeadKeyDown

Get information on whether a designated key of the Head component is down, valid for the current frame, and reset for the next frame 


#### Declaration

```csharp
public static bool GSXR_Is_HeadKeyDown(InputKeyCode inputKeyCode)
```


#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| InputKeyCode  | inputKeyCode | Designated key, the designated keys supported by Head are Enter/Back |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| bool  | Ture: down; False: not down |






## GSXR_Is_HeadKeyUp

Get information on whether a designated key of the Head component is up, valid for the current frame, and reset for the next frame


#### Declaration

```csharp
public static bool GSXR_Is_HeadKeyUp(InputKeyCode inputKeyCode)
```


#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| InputKeyCode  | inputKeyCode | Designated key, the designated keys supported by Head are Enter/Back |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| bool  | True:  up; False: not up |




## GSXR_HeadKeyState

Get the  state of a designated key of the Head component. Please refer to UnityAPI: Input.GetKey


#### Declaration

```csharp
public static InputKeyState GSXR_HeadKeyState(InputKeyCode inputKeyCode)
```


#### Parameters

| Type         | Name         | Description                              |
| :----------- | :----------- | :--------------------------------------- |
| InputKeyCode | inputKeyCode | Designated key, the designated keys supported by Head are Enter/Back |

#### Returns

| Type          | Description    |
| :------------ | :------------- |
| InputKeyState | State of the designated key |




## GSXR_HeadKeyCurrentState

Get the real-time state of a designated key of the Head component. Please refer to UnityAPI: Input.GetKey


#### Declaration

```csharp
public static InputKeyState GSXR_HeadKeyCurrentState(InputKeyCode inputKeyCode)
```


#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| InputKeyCode  | inputKeyCode | Designated key, the designated keys supported by Head are Enter/Back |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| InputKeyState   | State of the designated key |




## GSXR_HeadAddKey

Simulate sending a key to the Head component


#### Declaration

```csharp
public static void GSXR_HeadAddKey(InputKeyCode inputKeyCode, InputKeyState inputKeyState)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| InputKeyCode  | inputKeyCode | Designated key, the designated keys supported by Head are Enter/Back |
| InputKeyState  | inputKeyState | State of the key （DOWN, UP, LONG or NULL）|

> After sending a key, the next frame will take effect. Note that sending a key preferably appears as a pair of Down/Up.






## GSXR_Set_HeadRayCastDistance

Set the raycast distance of Collider detected by the Head component. The default value is 30 meters.


#### Declaration

```csharp
public static void GSXR_Set_HeadRayCastDistance(float distance)
```


#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| float  | distance | Set the raycast distance of Collider, unit in meter |






## GSXR_Set_HeadEndPointerDistance

Set the distance when the Focus of the Head component does not hit Collider. The default value is 3 meters.


#### Declaration

```csharp
public static void GSXR_Set_HeadEndPointerDistance(float distance)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| float  | distance |The distance when Focus does not hit Collider, unit in meter |






## GSXR_Get_HeadCursor

Get the  Cursor object of the Head component


#### Declaration

```csharp
public static DefaultCursor GSXR_Get_HeadCursor
```


#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| DefaultCursor | Return the Cursor object of the Head component |






## GSXR_BTDevice

Get the manager class for Bluetooth input devices (Controller)


#### Declaration

```csharp
public static InputDeviceBT3Dof GSXR_BTDevice
```


#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| InputDeviceBT3Dof | Return a Bluetooth 3Dof controller to the input device, note that it can be null |




## GSXR_BTRight

Get the first connected controller device.


#### Declaration

```csharp
public static InputDeviceBT3DofPart GSXR_BTRight
```


#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| InputDeviceBT3DofPart | Return the first connected game controller device, note that it can be null |




## GSXR_BTLeft

Get the second connected controller device.


#### Declaration

```csharp
public static InputDeviceBT3DofPart GSXR_BTLeft
```


#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| InputDeviceBT3DofPart | Return the second connected game controller device, note that it can be null |




## GSXR_BTRotation

Get the rotation of the controller device


#### Declaration

```csharp
public static Quaternion GSXR_BTRotation(BTType type = BTType.Right)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| BTType  | type | BTType.Right:  the first connected controller device (default); BTType.Left: the second connected controller device |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| Quaternion | Return the four elements of the rotation value of the controller device, global coordinates |






## GSXR_BTPosition

Get the position of the controller device


#### Declaration

```csharp
public static Vector3 GSXR_BTPosition(BTType type = BTType.Right)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| BTType  | type | BTType.Right: the first connected controller device (default); BTType.Left: the second connected controller device |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| Vector3 | Return the position of the controller device, global coordinates |






## GSXR_Is_BTTpTouch

Indicates whether the Bluetooth TouchPanel of the given controller device is touched


#### Declaration

```csharp
public static bool GSXR_Is_BTTpTouch(BTType type = BTType.Right)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| BTType  | type | BTType.Right: the first connected controller device (default);BTType.Left: the second connected controller device |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| bool | True: touched；False: not touched |






## GSXR_BTTpTouchInfo

Get the touch position information of the 3Dof GameController component (x,y)


#### Declaration

```csharp
public static Vector2 GSXR_BTTpTouchInfo(BTType type = BTType.Right)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| BTType  | type |BTType.Right: the first connected controller device (default);BTType.Left: the second connected controller device |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| Vector2 | Return the touch position information of the controller device (x,y) |





## GSXR_BTName

Get the name of the controller device


#### Declaration

```csharp
public static string GSXR_BTName(BTType type = BTType.Right)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| BTType  | type |BTType.Right: the first connected controller device(default);BTType.Left: the second connected controller device|

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| string |Return the name of the controller device, K02 or K07|





## GSXR_BTPointerEventData

Get the hit information collection of the controller device


#### Declaration

```csharp
public static SCPointEventData GSXR_BTPointerEventData(BTType type = BTType.Right)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| BTType  | type | BTType.Right: the first connected controller device(default);BTType.Left: the second connected controller device |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| SCPointEventData | Return the hit information collection of the controller device, note that it can be null |





## GSXR_BTHitTarget

Get the Collider object hit by the controller device


#### Declaration

```csharp
public static GameObject GSXR_BTHitTarget(BTType type = BTType.Right)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| BTType  | type | BTType.Right: the first connected controller device (default);BTType.Left: the second connected controller device |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| GameObject | Return the Collider object hit by the controller device |




## GSXR_BTHitInfo

Get the specific information of Collider hit by the controller device


#### Declaration

```csharp
public static RaycastResult GSXR_BTHitInfo(BTType type = BTType.Right)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| BTType  | type | BTType.Right: the first connected controller device (default);BTType.Left: the second connected controller device |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| RaycastResult | Return the specific information of Collider hit by the controller device |



## GSXR_BTDragTarget

Get the draggable object of the controller device


#### Declaration

```csharp
public static GameObject GSXR_BTDragTarget(BTType type = BTType.Right)
```


#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| GameObject |Return the draggable object of the controller device |






## GSXR_Is_BTKeyDown

Get whether the controller device has pressed any key


#### Declaration

```csharp
public static bool GSXR_Is_BTKeyDown(InputKeyCode inputKeyCode, BTType type = BTType.Right)
```
#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| InputKeyCode  | inputKeyCode | Designated key, HandShank supports Enter (Trigger)/Back/Funcion/Tp |
| BTType  | type |BTType.Right: the first connected controller device (default);BTType.Left: the second connected controller device  |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| bool | True: pressed; False: not pressed |






## GSXR_Is_BTKeyUp

Get whether the controller device has triggered any Key Up


#### Declaration

```csharp
public static bool GSXR_Is_BTKeyUp(InputKeyCode inputKeyCode, BTType type = BTType.Right)
```
#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| InputKeyCode  | inputKeyCode | Designated key, HandShank supports Enter (Trigger)/Back/Funcion/Tp |
| BTType  | type | BTType.Right: the first connected controller device (default);BTType.Left: the second connected controller device |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| bool | True: triggered ; False: not triggered |





## GSXR_BTKeyState

Get the state of the inputKeyCode key of the controller device


#### Declaration

```csharp
public static InputKeyState GSXR_BTKeyState(InputKeyCode inputKeyCode, BTType type = BTType.Right)
```
#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| InputKeyCode  | inputKeyCode | Designated key, HandShank supports Enter (Trigger)/Back/Funcion/Tp |
| BTType  | type | BTType.Right: the first connected controller device (default);BTType.Left: the second connected controller device |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| InputKeyState | Return the state of the inputKeyCode key of the controller device |






## GSXR_BTKeyCurrentState

Get the real-time state of the inputKeyCode key of the controller device


#### Declaration

```csharp
public static InputKeyState GSXR_BTKeyCurrentState(InputKeyCode inputKeyCode, BTType type = BTType.Right)
```


#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| InputKeyState  | Return the real-time state of the inputKeyCode key of the controller device |





## GSXR_BTKeyAddKey

Simulate sending a key to the controller device


#### Declaration

```csharp
public static void GSXR_BTKeyAddKey(InputKeyCode inputKeyCode, InputKeyState inputKeyState, BTType type = BTType.Right)
```
#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| InputKeyCode  | inputKeyCode | Designated key, HandShank supports Enter (Trigger)/Back/Funcion/Tp |
| InputKeyState  | inputKeyState | The state of the designated key, note that sending a key preferably appears as a pair of Down/Up） |
| BTType  | type | BTType.Right: the first connected controller device (default);BTType.Left: the second connected controller device |





## GSXR_Set_BTRayCastDistance

Set the raycast distance of Collider detected by the controller device. The default value is 30 meters.


#### Declaration

```csharp
public static void GSXR_Set_BTRayCastDistance(float distance, BTType type = BTType.Right)
```
#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| float  | Distance | The raycast distance of Collider detected by controller device, unit in meter |
| BTType  | type |BTType.Right: the first connected controller device (default);BTType.Left: the second connected controller device |





## GSXR_Set_BTEndPointerDistance

Set the beam distance when the controller device does not detect Collider. The default value is 3 meters.


#### Declaration

```csharp
public static void GSXR_Set_BTEndPointerDistance(float distance, BTType type = BTType.Right)
```
#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| float  | Distance | The raycast distance of Collider detected by the controller device, unit in meter |
| BTType  | type | BTType.Right: the first connected controller device (default);BTType.Left: the second connected controller device |





## GSXR_Get_BTCursor

Get the Cursor object of the controller device


#### Declaration

```csharp
public static DefaultCursor GSXR_Get_BTCursor(BTType type = BTType.Right)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| BTType  | type | BTType.Right: the first connected controller device (default);BTType.Left: the second connected controller device |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| DefaultCursor  | Return the Cursor object of the controller device, note that it can be null |





## GSXR_Get_BTLine

Get the beam object of the controller device


#### Declaration

```csharp
public static LineRenderer GSXR_Get_BTLine(BTType type = BTType.Right)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| BTType  | type | BTType.Right: the first connected controller device (default);BTType.Left: the second connected controller device |

#### Returns

| Type      | Description                                   |
| :-------- | :-------------------------------------------- |
| LineRenderer  | Return the beam object of the controller device, note that it can be null |





## GSXR_Enable_BT

Enable the controller device


#### Declaration

```csharp
public static void GSXR_Enable_BT(BTType type = BTType.Right)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| BTType  | type | BTType.Right: the first connected controller device (default);BTType.Left: the second connected controller device |






## GSXR_Disable_BT

Disable the controller device


#### Declaration

```csharp
public static void GSXR_Disable_BT(BTType type = BTType.Right)
```

#### Parameters

| Type   | Name   | Description            |
| :----- | :----- | :--------------------- |
| BTType  | type | BTType.Right: the first connected controller device (default);BTType.Left: the second connected controller device |




## GSXR_Get_Acc

Get   the controller device  of  the accelerometer data 


#### Declaration

```csharp
public static int[] GSXR_Get_Acc(BTType type = BTType.Right)
```

#### Parameters

| Type   | Name | Description                                                  |
| :----- | :--- | :----------------------------------------------------------- |
| BTType  | type | BTType.Right: the first connected controller device (default);BTType.Left: the second connected controller device  |




## GSXR_Get_Gyro

Get   the controller device  of  the Gyroscope data


#### Declaration

```csharp
public static int[] GSXR_Get_Gyro(BTType type = BTType.Right)
```

#### Parameters

| Type   | Name | Description                                                  |
| :----- | :--- | :----------------------------------------------------------- |
| BTType  | type | BTType.Right: the first connected controller device (default);BTType.Left: the second connected controller device |








## GSXR_GGT26DofDevice

Get the manager class of the Hand Tracking input device


#### Declaration

```csharp
public static InputDeviceHand GSXR_GGT26DofDevice
```


#### Returns

| Type                    | Description                    |
| :---------------------- | :----------------------------- |
| InputDeviceHand | Return the Hand Tracking input device, note that it can be null |




## GSXR_GGTLeft

Get the left-hand component of the hand tracking device


#### Declaration

```csharp
public static InputDeviceGGT26DofPart GSXR_GGTLeft
```


#### Returns

| Type                        | Description |
| :-------------------------- | :---------- |
| InputDeviceGGT26DofPart | Return the left-hand component    |




## GSXR_GGTRight

Get the right-hand component of the hand tracking device


#### Declaration

```csharp
public static InputDeviceGGT26DofPart GSXR_GGTRight
```


#### Returns

| Type                        | Description |
| :-------------------------- | :---------- |
| InputDeviceGGT26DofPart | Return the right-hand component    |




## GSXR_GGThandInfo

Get the handInfo structure of the hand tracking device. handInfo contains various data of the hand tracking.


#### Declaration

```csharp
public static handInfo GSXR_GGThandInfo(GGestureType type = GGestureType.Right)
```

#### Parameters

| Type        | Name | Description                                                  |
| :---------- | :--- | :----------------------------------------------------------- |
| GGestureType | type | GestureType.Right : the right-hand component (default value); GestureType.Left:  the left-hand component |

#### Returns

| Type     | Description                                               |
| :------- | :-------------------------------------------------------- |
| handInfo | Return the handInfo structure of the hand tracking device |






## GSXR_GGTPointerEventData

Get the hit information collection of the hand tracking device


#### Declaration

```csharp
public static SCPointEventData GSXR_GGTPointerEventData(GGestureType type = GGestureType.Right)
```

#### Parameters

| Type        | Name | Description                                                  |
| :---------- | :--- | :----------------------------------------------------------- |
| GGestureType | type | GestureType.Right : the right-hand component (default value); GestureType.Left:  the left-hand component  |

#### Returns

| Type             | Description                                                  |
| :--------------- | :----------------------------------------------------------- |
| SCPointEventData | Return the hit information collection of the hand tracking device |






## GSXR_GGTHitTarget

Get the Collider object hit by the hand tracking device

#### Declaration

```csharp
public static GameObject GSXR_GGTHitTarget(GGestureType type = GGestureType.Right)
```

#### Parameters

| Type        | Name | Description                                                  |
| :---------- | :--- | :----------------------------------------------------------- |
| GGestureType | type | GestureType.Right : the right-hand component (default value); GestureType.Left:  the left-hand component  |

#### Returns

| Type       | Description                  |
| :--------- | :--------------------------- |
| GameObject | Return the hit object, note that it can be null |






## GSXR_GGTHitInfo

Get the RaycastHit structure of Collider hit by the gesture component


#### Declaration

```csharp
public static RaycastResult GSXR_GGTHitInfo(GGestureType type = GGestureType.Right)
```

#### Parameters

| Type        | Name | Description                                                  |
| :---------- | :--- | :----------------------------------------------------------- |
| GGestureType | type | GestureType.Right : the right-hand component (default value); GestureType.Left:  the left-hand component  |

#### Returns

| Type       | Description                          |
| :--------- | :----------------------------------- |
| RaycastResult | Return the RaycastHit structure of Collider hit by the hand tracking device |





## GSXR_GGTDragTarget

Get the draggable object of the hand tracking device


#### Declaration

```csharp
public static GameObject GSXR_GGTDragTarget(GGestureType type = GGestureType.Right)
```

#### Parameters

| Type        | Name | Description                                                  |
| :---------- | :--- | :----------------------------------------------------------- |
| GGestureType | type |GestureType.Right : the right-hand component (default value); GestureType.Left:  the left-hand component  |

#### Returns

| Type       | Description                                             |
| :--------- | :------------------------------------------------------ |
| GameObject | Return the draggable object of the hand tracking device |






## GSXR_Is_GGTKeyDown

Determine whether the hand tracking device has triggered a Key Down


#### Declaration

```csharp
public static bool GSXR_Is_GGTKeyDown(InputKeyCode inputKeyCode, GGestureType type = GGestureType.Right)
```

#### Parameters

| Type         | Name         | Description                                                  |
| :----------- | :----------- | :----------------------------------------------------------- |
| InputKeyCode | inputKeyCode | inputKeyCode: designated key, only support the Enter key currently                |
| GGestureType  | type         | GestureType.Right : the right-hand component (default value); GestureType.Left:  the left-hand component  |

#### Returns

| Type | Description                   |
| :--- | :---------------------------- |
| bool | True: triggered; False: not triggered |






## GSXR_Is_GGTKeyUp

Determine whether the hand tracking device has triggered a Key Up


#### Declaration

```csharp
public static bool GSXR_Is_GGTKeyUp(InputKeyCode inputKeyCode, GGestureType type = GGestureType.Right)
```

#### Parameters

| Type         | Name         | Description                                                  |
| :----------- | :----------- | :----------------------------------------------------------- |
| InputKeyCode | inputKeyCode | inputKeyCode: designated key, only support the Enter key currently                        |
| GGestureType  | type         | GestureType.Right : the right-hand component (default value); GestureType.Left:  the left-hand component  |

#### Returns

| Type | Description                   |
| :--- | :---------------------------- |
| bool | True: triggered; False: not triggered  |





## GSXR_GGTKeyState

Get the state of a designated key of the hand tracking device


#### Declaration

```csharp
public static InputKeyState GSXR_GGTKeyState(InputKeyCode inputKeyCode, GGestureType type = GGestureType.Right)
```

#### Parameters

| Type         | Name         | Description                                                  |
| :----------- | :----------- | :----------------------------------------------------------- |
| InputKeyCode | inputKeyCode | inputKeyCode: designated key, only support the Enter key currently                  |
| GGestureType  | type         | GestureType.Right : the right-hand component (default value); GestureType.Left:  the left-hand component |

#### Returns

| Type          | Description    |
| :------------ | :------------- |
| InputKeyState | State of the designated key|






## GSXR_GGTKeyCurrentState

et the real-time state of a designated key of the hand tracking device


#### Declaration

```csharp
public static InputKeyState GSXR_GGTKeyCurrentState(InputKeyCode inputKeyCode, GGestureType type = GGestureType.Right)
```

#### Parameters

| Type         | Name         | Description                                                  |
| :----------- | :----------- | :----------------------------------------------------------- |
| InputKeyCode | inputKeyCode | inputKeyCode: designated key, only support the Enter key currently                    |
| GGestureType  | type         |GestureType.Right : the right-hand component (default value); GestureType.Left:  the left-hand component  |

#### Returns

| Type          | Description                  |
| :------------ | :--------------------------- |
| InputKeyState | State of the designated key |





## GSXR_GGTKeyAddKey

Simulate sending a key to the hand tracking device


#### Declaration

```csharp
public static void GSXR_GGTKeyAddKey(InputKeyCode inputKeyCode, InputKeyState inputKeyState, GGestureType type = GGestureType.Right)
```

#### Parameters

| Type          | Name          | Description                                                  |
| :------------ | :------------ | :----------------------------------------------------------- |
| InputKeyCode  | inputKeyCode  | inputKeyCode: designated key, only support the Enter key currently                         |
| InputKeyState | inputKeyState | State of the designated key, note that sending a key  preferably appears as a pair of  Down/Up           |
| GGestureType   | type          | GestureType.Right : the right-hand component (default value); GestureType.Left:  the left-hand component |





## GSXR_Set_GGTRayCastDistance

Set the raycast distance of Collider detected by the hand tracking device. The default value is 30 meters.


#### Declaration

```csharp
public static void GSXR_Set_GGTRayCastDistance(float distance, GGestureType type = GGestureType.Right)
```

#### Parameters

| Type        | Name     | Description                                                  |
| :---------- | :------- | :----------------------------------------------------------- |
| float       | Distance | The raycast distance of Collider detected by the hand tracking device, unit in meter |
| GGestureType | type     | GestureType.Right : the right-hand component (default value); GestureType.Left:  the left-hand component |





## GSXR_Set_GGTEndPointerDistance

Set the Focus distance when the hand tracking device does not detect Collider. The default value is 3 meters.


#### Declaration

```csharp
public static void GSXR_Set_GGTEndPointerDistance(float distance, GGestureType type = GGestureType.Right)
```

#### Parameters

| Type        | Name     | Description                                                  |
| :---------- | :------- | :----------------------------------------------------------- |
| float       | Distance | The raycast distance of Collider detected by the type of Hand Tracking component, unit in meter      |
| GGestureType | type     | GestureType.Right : the right-hand component (default value); GestureType.Left:  the left-hand component  |





## GSXR_Get_GGTCursor

Get Cursor of the hand tracking device


#### Declaration

```csharp
public static DefaultCursor GSXR_Get_GGTCursor(GGestureType type = GGestureType.Right)
```

#### Parameters

| Type        | Name | Description                                                  |
| :---------- | :--- | :----------------------------------------------------------- |
| GGestureType | type | GestureType.Right : the right-hand component (default value); GestureType.Left:  the left-hand component  |

#### Returns

| Type  | Description     |
| :---- | :-------------- |
| DefaultCursor | Return Cursor of the hand tracking device |





## GSXR_Get_GGTLine

Get the beam of the hand tracking device


#### Declaration

```csharp
public static LineRenderer GSXR_Get_GGTLine(GGestureType type = GGestureType.Right)
```

#### Parameters

| Type        | Name | Description                                                  |
| :---------- | :--- | :----------------------------------------------------------- |
| GGestureType | type |GestureType.Right : the right-hand component (default value); GestureType.Left:  the left-hand component  |

#### Returns

| Type         | Description                                 |
| :----------- | :------------------------------------------ |
| LineRenderer | Return the beam of the hand tracking device |





## GSXR_Enable_GGT

Enable the hand tracking device


#### Declaration

```csharp
public static void GSXR_Enable_GGT(GGestureType type = GGestureType.Right)
```

#### Parameters

| Type        | Name | Description                                                  |
| :---------- | :--- | :----------------------------------------------------------- |
| GGestureType | type | GestureType.Right : the right-hand component (default value); GestureType.Left:  the left-hand component  |






## GSXR_Disable_GGT

Disable the hand tracking device


#### Declaration

```csharp
public static void GSXR_Disable_GGT(GGestureType type = GGestureType.Right)
```

#### Parameters

| Type        | Name | Description                                                  |
| :---------- | :--- | :----------------------------------------------------------- |
| GGestureType | type | GestureType.Right : the right-hand component (default value); GestureType.Left:  the left-hand component  |





## GSXR_Get_FingerUI

Get the fingerUI structure of the hand tracking device


#### Declaration

```csharp
public static Model26DofGesture.FingerUI[] GSXR_Get_FingerUI(GGestureType type = GGestureType.Right)
```
#### Parameters

| Type        | Name | Description                                                  |
| :---------- | :--- | :----------------------------------------------------------- |
| GGestureType | type | GestureType.Right : the right-hand component (default value); GestureType.Left:  the left-hand component  |

#### Returns

| Type                       | Description            |
| :------------------------- | :--------------------- |
| Model26DofGesture.FingerUI[] | Return the fingerUI structure of the hand tracking device |

