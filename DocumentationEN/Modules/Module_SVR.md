# Module_SVR

The `Module_SVR` module is specifically responsible for interacting with the underlying SLAM and obtaining SLAM data



## Using Module_SVR module

**This module belongs to the core module of SDK. The SDK is used by default and is placed under the SDKSystem prefab. Developers do not need to modify it**
This module provides developers with some API interfaces for developers to use. Some APIs are listed below. For details, please refer to the API documentation
This module provides the following API interfaces：

* `SetTrackMode`：Set whether the glasses enter mode is 3Dof or 6Dof
* `IsSvrRunning`：Get whether the Svr system is running
* `IsSvrInitialized`：Get whether the Svr system is initialized
* `AddInitializedCallBack`：Set the callback when Svr initialization is complete
* `RemoveInitialzedCallBack`：Remove the callback when Svr initialization is complete
* `SetRenderFrame`：Set the rendering frame rate
* `GetEyeCameras`：Get left and right eye cameras
* `GetHead`：Get the head object, if you want to get the head rotation and other data, call it in the LateUpdate method
* `SetPD`：Set the interpupillary distance, called when Awake
* `RecenterTracking`：Repositioning, only effective on glasses

**Note: **This SVR module only interacts with the SLAM algorithm on the glasses equipment.

