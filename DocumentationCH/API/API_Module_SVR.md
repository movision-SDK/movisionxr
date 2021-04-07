# API_GSXR_Slam

```csharp
Class: public class API_GSXR_Slam
```

**API_GSXR_Slam**模块是专门用于提供与底层SLAM进行交互，获取SLAM数据等API接口。

## TrackMode

定义Svr Slam模式


#### Declaration

```csharp
 public enum TrackMode
```

#### Fields

```csharp
 Mode_3Dof, //3Dof模式
 Mode_6Dof, //6Dof模式
```



## GSXR_Set_TrackMode

设置XR设备Slam进入模式，运行过程中可修改

#### Declaration

```csharp
 public static void GSXR_Set_TrackMode(TrackMode mode)
```


#### Parameters
|  Type   | Name  | Description |
|  :----  | :----  | :----  |
| TrackMode  | mode |Slam模式，参见TrackMode|




## GSXR_Is_SlamRunning

Slam系统是否在运行

#### Declaration

```csharp
 public static bool GSXR_Is_SlamRunning()
```

#### Return
|  Type   | Description |
|  :----  |   :----  |
| bool  | True: Slam系统正在运行  False: Slam系统未运行|



## GSXR_Is_SlamInitialized

Slam系统是否初始化完成

#### Declaration

```csharp
 public static bool GSXR_Is_SlamInitialized()
```

#### Return
|  Type   | Description |
|  :----  |   :----  |
| bool  | True: Slam系统初始化完成  False: Slam系统未初始化|




## GSXR_Add_InitializedCallBack

设置Slam初始化完成时的回调


#### Declaration

```csharp
  public static void GSXR_Add_InitializedCallBack(Action action)
```


#### Parameters
|  Type   | Name  | Description |
|  :----  | :----  | :---- |
| Action  | action |Action类型回调function|






## GSXR_Remove_InitializedCallBack

移除Slam初始化完成时的回调


#### Declaration

```csharp
  public static void GSXR_Remove_InitializedCallBack(Action action)
```


#### Parameters
|  Type   | Name  | Description |
|  :----  | :----  | :---- |
| Action  | action |Action类型回调function|





## GSXR_Set_RenderFrame

设置渲染帧率,只能在Start中调用


#### Declaration

```csharp
public static void GSXR_Set_RenderFrame(int frameRate = -1)
```


#### Parameters
|  Type   | Name  | Description |
|  :----  | :----  | :---- |
| int  | frameRate |-1表示系统默认帧率，设置范围0-200|







## GSXR_Get_EyeCameras

获取左右眼渲染Camera


#### Declaration

```csharp
public static List<Camera> GSXR_Get_EyeCameras()
```


#### Returns

|  Type   | Description |
|  :----  |   :----  |
| List<Camera>  | List[0]左眼 List[1]右眼，空表示系统未启动完成|



## GSXR_Get_RenderTexure

获取左右眼渲染的画面，为获取当前帧的渲染结果，当前帧结束时调用


#### Declaration

```csharp
public static List<RenderTexture> GSXR_Get_RenderTexure()
```

#### Returns
|  Type   | Description |
|  :----  |   :----  |
| List<RenderTexture>  | List[0]左眼 List[1]右眼，空表示系统未启动完成|







## GSXR_Get_Head

获取头部物体，如果想获取头部的旋转移动等数据，在LateUpdate方法里调用

#### Declaration

```csharp
public static Transform GSXR_Get_Head()
```


#### Returns
|  Type   | Description |
|  :----  |   :----  |
| Transform  | Head对象的Transform组件，空表示系统未启动完成|







## GSXR_Set_PD

设置左右眼的间距


#### Declaration

```csharp
 public static void GSXR_Set_PD(float offset = 0)
```


#### Parameters
|  Type   | Name  | Description |
|  :----  | :----  |:----|
| float  | offset |设置瞳距，Awake时调用，Start后调用无效|





## GSXR_RecenterTracking

系统Slam重定位，若无效果，表示系统初始化未完成,且只有在眼镜上有效


#### Declaration

```csharp
public static void GSXR_RecenterTracking()
```







## GSXR_Start_Slam

开启设备的Slam


#### Declaration

```csharp
public static void GSXR_Start_Slam() 
```






## GSXR_Stop_Slam

关闭设备的Slam


#### Declaration

```csharp
public static void GSXR_Stop_Slam() 
```






## GSXR_Reset_Slam

重置设备的Slam


#### Declaration

```csharp
public static void GSXR_Reset_Slam() 
```





## GSXR_Is_SlamDataLost

判断设备的Slam数据是否丢失


#### Declaration

```csharp
public static void GSXR_Is_SlamDataLost() 
```





## GSXR_Get_LatestQVRCameraBinocularData

获取设备的双眼灰度数据。


#### Declaration

```csharp
public static int GSXR_Get_LatestQVRCameraBinocularData(ref bool outBUdate, ref uint outCurrFrameIndex, ref ulong outFrameExposureNano, byte[] outLeftFrameData, byte[] outRightFrameData)
```


