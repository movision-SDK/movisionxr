# Module_SDKConfiguration
**Module_SDKConfiguration**模块在于为开发者提供配置XR设备的输入方式功能。



## Module_SDKConfiguration的使用

此模块为开发者提供了一些API接口，供开发者使用，如下列部分API：
*  **HasKey**：判断SDK配置文件中是否有此配置项。
*  **GetInt**：获取此配置项的Int值。
*  **GetBool**：获取此配置项的Bool值。
*  **GetString**：获取此配置项的String值。
*  **GetFloat**：获取此配置项的Float值。

通过上列API可获取SDK配置表中配置数据。


## Module_SDKConfiguration的SDKConfiguration参数解析
可以动态的开启或者关闭某些InputDevice，按如下图，找到SDK配置文件 SDKConfiguration.asset文件，配置SDK的一些属性

![ControlInputDevice.png](../../Images/Gettingstartedtutorials/ControlInputDevice.png)

* **ActiveHead**的值为1 - 开启InputDeviceHead输入设备（头显方式）

* **ActiveGGT26Dof**的值为1 - 开启InputDeviceGGT26Dof输入设备（自由手势方式）

  > InputDeviceGGT26Dof 输入设备开启会自动关闭InputDeviceHead输入设备

* **ActiveBT3Dof** 的值为1- 开启InputDeviceBT3Dof输入设备（蓝牙手柄方式）

  > InputDeviceBT3Dof 输入设备开启会自动关闭InputDeviceHead输入设备

* **ActiveKS** 的值为1- 开启InputDeviceKS输入设备（游戏控制器方式）

  > InputDeviceKS 输入设备开启会自动关闭InputDeviceHead输入设备

* **KSMode6Dof**的值为1- 开启InputDeviceKS输入设备的6Dof模式


> 备注：属性值设置SDK的默认状态，应用运行过程中会生成配置文件，目录为/sdcard/Android/data/packagename/files/SDK_Configs.txt，覆写其中的值可以达到在不重新编译APP的情况下修改SDK的配置
