# Module_SDKConfiguration
Module_SDKConfiguration provides developers with the function of configuring SDK.



## Property description
You can dynamically turn on or turn off some InputDevices, as shown below, find the SDK configuration file SDKConfiguration.asset file, and configure some properties of the SDK

![ControlInputDevice.png](D:/01_works/01_Unity/00_UnitySDK/ShadowSDKwebpage/Images/Gettingstartedtutorials/ControlInputDevice.png)

* **ActiveHead=1** - Turn on the head-mounted display mode

* **ActiveGGT26Dof=1** - Turn on the hand tracking mode

  > The InputDeviceGGT26Dof input device will automatically close the InputDeviceHead input device when the input device is turned on

* **ActiveBT3Dof=1** - Turn on the InputDeviceBT3Dof input device

  > The InputDeviceBT3Dof input device is turned on and the InputDeviceHead input device will be automatically closed

* **ActiveKS=1** - Turn on the InputDeviceKS input device

  > The InputDeviceKS input device is turned on and the InputDeviceHead input device will be automatically closed

* **KSMode6Dof=1**- Turn on the 6Dof mode of InputDeviceKS input device


> Note: The attribute value sets the default state of the SDK. The configuration file will be generated during Runtime at /sdcard/Android/data/packagename/files/SDK_Configs.txt，Overwriting the value can modify the SDK configuration without recompiling the APP