# Module_SVR
**Module_SVR**模块用于专门负责与底层SLAM进行交互，获取SLAM数据等。

## Module_SVR模块的使用

**此模块属于SDK核心模块，SDK默认使用，放置于SDKSystem预制体下，开发者无需修改。**
此模块为开发者提供了一些API接口，供开发者使用，如下列举部分API，具体见API说明文档。
此模块提供了下列API接口：

* **SetTrackMode**：设置眼镜进入模式是3Dof还是6Dof
* **IsSvrRunning**：获取Svr系统是否在运行
* **IsSvrInitialized**：获取Svr系统是否初始化完成
* **AddInitializedCallBack**：设置Svr初始化完成时的回调
* **RemoveInitialzedCallBack**：移除Svr初始化完成时的回调，需与`AddInitializedCallBack`成对出现
* **SetRenderFrame**：设置渲染帧率，只能在Start中调用
* **GetEyeCameras**：获取左右眼摄像头
* **GetHead**：获取头部物体，如果想获取头部的旋转移动等数据，在LateUpdate方法里调用
* **SetPD**：设置瞳间距，Awake时调用
* **RecenterTracking**：系统Slam重新定位，只有在XR眼镜设备上有效

**注意：**此SVR模块只与支持的XR眼镜设备上的SLAM算法交互。