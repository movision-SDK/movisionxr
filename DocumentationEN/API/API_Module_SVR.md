# API_GSXR_Slam

```csharp
Class: public class API_GSXR_Slam
```



## TrackMode

Define the SLAM mode


#### Declaration

```csharp
 public enum TrackMode
```

#### Fields

```csharp
 Mode_3Dof
 Mode_6Dof
```



## GSXR_Set_TrackMode

Set the entry mode of the XR device SLAM, which can be modified during Runtime

#### Declaration

```csharp
 public static void GSXR_Set_TrackMode(TrackMode mode)
```


#### Parameters
|  Type   | Name  | Description |
|  :----  | :----  | :----  |
| TrackMode  | mode |SLAM mode, refer to TrackMode|




## GSXR_Is_SlamRunning

Whether the SLAM system is running

#### Declaration

```csharp
 public static bool GSXR_Is_SlamRunning()
```

#### Return
|  Type   | Description |
|  :----  |   :----  |
| bool  | True: the SLAM system is running; False: the SLAM system is not running|



## GSXR_Is_SlamInitialized

Whether the SLAM system initialization has been completed

#### Declaration

```csharp
 public static bool GSXR_Is_SlamInitialized()
```

#### Return
|  Type   | Description |
|  :----  |   :----  |
| bool  |True: the SLAM system initialization has been completed;False: the SLAM system is not initialized|




## GSXR_Add_InitializedCallBack

Add the callback that is triggered by the completion of the SLAM system initialization


#### Declaration

```csharp
  public static void GSXR_Add_InitializedCallBack(Action action)
```


#### Parameters
|  Type   | Name  | Description |
|  :----  | :----  | :---- |
| Action  | action |Action type callback function|






## GSXR_Remove_InitializedCallBack

Delete the callback that is triggered by the completion of the SLAM system initialization 


#### Declaration

```csharp
  public static void GSXR_Remove_InitializedCallBack(Action action)
```


#### Parameters
|  Type   | Name  | Description |
|  :----  | :----  | :---- |
| Action  | action |Action类型回调function|





## GSXR_Set_RenderFrame

Set the rendering frame rate, which can only be called during Start


#### Declaration

```csharp
public static void GSXR_Set_RenderFrame(int frameRate = -1)
```


#### Parameters
|  Type   | Name  | Description |
|  :----  | :----  | :---- |
| int  | frameRate |-1: the system default frame rate. The configurable range is 0-200|








## GSXR_Get_EyeCameras

Get left and right eye rendering cameras


#### Declaration

```csharp
public static List<Camera> GSXR_Get_EyeCameras()
```


#### Returns

|  Type   | Description |
|  :----  |   :----  |
| List<Camera>  | List[0]: left eye; List[1]: right eye; Null: the system has not been started |








## GSXR_Get_RenderTexure

Get the rendering picture of the left and right eyes. To get the rendering result of the current frame, call at the end of the current frame.


#### Declaration

```csharp
public static List<RenderTexture> GSXR_Get_RenderTexure()
```

#### Returns
|  Type   | Description |
|  :----  |   :----  |
| List<RenderTexture>  |List[0]: left eye; List[1]: right eye; Null: the system has not been started|







## GSXR_Get_Head

Get the Head object. To get the data of head rotation and movement and other related data, call it in the LateUpdate method.

#### Declaration

```csharp
public static Transform GSXR_Get_Head()
```


#### Returns
|  Type   | Description |
|  :----  |   :----  |
| Transform  | The Transform component of the Head object. Null means the system has not been started.|







## GSXR_Set_PD

Set left and right eye rendering of the cameras. 


#### Declaration

```csharp
 public static void GSXR_Set_PD(float offset = 0)
```


#### Parameters
|  Type   | Name  | Description |
|  :----  | :----  |:----|
| float  | offset |Set the pupillary distance (PD). This method should be called during Awake. The method is invalid after Start|







## GSXR_RecenterTracking

Reset the position/Relocalization. If there is no effect, it means the system initialization has not been completed and it is only valid on the glasses.


#### Declaration

```csharp
public static void GSXR_RecenterTracking()
```


## GSXR_Start_Slam

Open the SLAM for equiment


#### Declaration

```csharp
public static void GSXR_Start_Slam() 
```






## GSXR_Stop_Slam

Close the SLAM for equiment


#### Declaration

```csharp
public static void GSXR_Stop_Slam() 
```






## GSXR_Reset_Slam

Reset the SLAM for equiment


#### Declaration

```csharp
public static void GSXR_Reset_Slam() 
```





## GSXR_Is_SlamDataLost

Determine    whether the SLAM data for equiment  lost


#### Declaration

```csharp
public static void GSXR_Is_SlamDataLost() 
```





## GSXR_Get_LatestQVRCameraBinocularData

Access to equipment eyes gray data


#### Declaration

```csharp
public static int GSXR_Get_LatestQVRCameraBinocularData(ref bool outBUdate, ref uint outCurrFrameIndex, ref ulong outFrameExposureNano, byte[] outLeftFrameData, byte[] outRightFrameData)
```

