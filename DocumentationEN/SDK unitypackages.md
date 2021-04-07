# SDK unitypackages

SDK is a collection of multiple unitypackages. These unitypackages support the development of Android Applications for  XR devices

- [SDK.Foundation.unitypackage](https://github.com//UnitySDK/releases)
- [SDK.Examples.unitypackage](https://github.com//UnitySDK/releases)

This article provides detailed descriptions of these unitypackages.


## SDK.Foundation.unitypackage

SDK.Foundation.unitypackage provides the main modules of SDK.

| Folder | Component | Description |
| :--- | :--- | :--- |
| SDK/Common | | Public resources |
|  | Base | Base classes required by the Modules of the SDK |
| | Plugins | Commonly used third-party plugins |
|  | StandardAssets           | Some public resource files |
| SDK/Modules |  | The Modules provided by the SDK |
| | Module_InputSystem | The input system Module that manages all input devices (head-mounted display/game controller/hand tracking) |
| | Module_SDKSystem | The Module that manages the core Modules in SDK |
|  | Module_Interaction       | The Module that contains all the components needed for interactions |
|  | Module_SVR | The Module that interacts with the bottom layer of the system, responsible for obtaining SLAM data |
| | Module_AudioSystem | The Module that manages all Audio resources |
| | Module_AndroidPermission | The Module that manages Android permissions |
| | Module_FPS | The Module that displays FPS |
| | Module_InputControl | The Module that simulates the behaviors of XR devices in the Editor mode |
|  | Module_Follower | The Module of the game object Follower’s perspective |
| | Module_GridCollection | The Module that provides methods for arranging any number of 3D objects for developers |
| | Module_VRMode | The VRMode control Module |
| | Module_AudioSpatial | The Module that provides spatial audio effect for developers |
| | Module_AutoClick | The Module that provides gaze click related features for developers |
| | Module_Device | The Module that provides information of supported devices for developers |
| | Module_Notice | The Module that provides pop-up information for developers |
| | Module_QVRCamera | The Module that provides developers  stereo mono-camera images through QVR service |
| | Module_RGBCamera | The Module that provides images by the RGB camera for developers |
| | Module_SDKConfiguration | The Module that provides configuration for the input modes and hand tracking related settings of the device |
| | Module_SDKVersion | The Module that provides the version number of the SDK |
| | Module_SkyBox | The Module that provides Skybox background images and textures for developers |
| | Module_Vuforia | The Module that provides compatibility with third-party Vuforia plugins |



## SDK.Examples.unitypackage

SDK.Examples.unitypackage contains examples of developing with the SDK

> SDK.Examples.unitypackage depends on SDK.Foundation.unitypackage

| Folder | Component | Description |
| :--- | :--- | :--- |
| SDK/Examples | |  |
| | HandTracking | Examples of using Hand Tracking  interactions in SDK |
| | StandardAssets | Public resources used by the examples |


