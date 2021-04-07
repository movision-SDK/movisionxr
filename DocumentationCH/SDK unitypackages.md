# SDK unitypackages

SDK是多个unitypackage的集合，使用这些unitypackage可以开发运行于XR设备的Android Application

SDK包含的unitypackage如下，本文将介绍关于这些unitypackage的详细内容

- [SDK.Foundation.unitypackage](#foundation)
- [SDK.Examples.unitypackage](#examples)



## SDK.Foundation.unitypackage

SDK.Foundation.unitypackage 包含SDK最基本的一些模块

| Folder | Component | Description |
| :--- | :--- | :--- |
| SDK/Common | | SDK中公共资源 |
|  | Base | SDK中Modules所需的一些基类 |
| | Plugins | SDK中使用的一些常用第三方插件 |
|  | StandardAssets           | SDK中使用的一些公共资源文件 |
| SDK/Modules |  | SDK提供的模块 |
| | Module_InputSystem | SDK中的输入系统模块，负责管理所有的输入设备（头显/手柄/手势） |
| | Module_SDKSystem | SDK中的SDKSystem模块，负责管理SDK中核心模块 |
|  | Module_Interaction       | SDK中交互组件模块，包含所有交互所需要的组件 |
|  | Module_SVR | SDK中与系统底层交互的模块，负责Slam数据的获取 |
| | Module_AudioSystem | SDK中管理所有Audio资源的模块 |
| | Module_AndroidPermission | SDK中管理Android权限的模块 |
| | Module_FPS | SDK中显示FPS的模块 |
| | Module_InputControl | SDK中Editor模式下模拟XR设备行为的模块 |
|  | Module_Follower | SDK中游戏对象视角跟随的模块 |
| | Module_GridCollection | SDK中为开发者提供为任意数量的3D物体进行排列布局的模块 |
| | Module_VRMode | SDK中VR模块控制模块 |
| | Module_AudioSpatial | SDK中为开发者提供的空间3D音效的模块 |
| | Module_AutoClick | SDK中为开发者提供凝视触发点击功能的模块 |
| | Module_Device | SDK中为开发者提供SDK支持的相关设备基本信息的模块 |
| | Module_Notice | SDK中为开发者提供的消息提示弹框的模块 |
| | Module_QVRCamera | SDK中为开发者提供的获取设备的双目灰度相机图像的模块 |
| | Module_RGBCamera | SDK中为开发者提供的获取设备的单目RGB相机图像的模块 |
| | Module_SDKConfiguration | SDK中为开发者提供的配置设备的输入方式及手势输入相关设置的模块 |
| | Module_SDKVersion | SDK中为开发者提供此SDK版本号的模块 |
| | Module_SkyBox | SDK中为开发者提供配置天空盒背景材质球的模块 |
| | Module_Vuforia | SDK中为开发者提供适配第三方Vuforid插件的模块|


## SDK.Examples.unitypackage

SDK.Examples.unitypackage 包含SDK中模块使用的演示Example

> SDK.Examples.unitypackage依赖于SDK.Foundation.unitypackage

| Folder | Component | Description |
| :--- | :--- | :--- |
| SDK/Examples | | SDK提供的演示Demos |
| | HandTracking | SDK中手势交互使用的演示Example |
| | StandardAssets | SDK中Examples使用的公共资源 |


