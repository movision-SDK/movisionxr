# Module_QVRCamera
**Module_QVRCamera**模块在于为开发者提供获取XR设备的灰度相机数据功能。


## Module_QVRCamera的使用



* SDK为开发者提供了 `Module_QVRCamera` 脚本,位于`SDK\Modules\Module_QVRCamera\Scripts\ShowQVRCamera.cs`处。
* 在任意游戏对象上挂载ShowQVRCamera脚本组件后，将灰度相机返回的数据分别赋予RawImage组件。


## Module_QVRCamera组件的参数解析

![QVRCamera.png](../../Images/Modules/QVRCamera.png)

此组件的参数如下：
* **Show Left Image**：显示左眼灰度相机的图像。
* **Show Right Image**：显示右眼灰度相机的图像。

## 设备灰度相机数据获取注意事项

此组件在获取设备的灰度相机数据时须注意：

- 应用确保开启相机权限开关。
- 在设备的svrapi_config.txt配置文件开头添加`gUseQVRCamera = true`属性。
- > **svrapi_config.txt**配置文件在设备中的路径为**/persist/qvr/svrapi_config.txt**和**/vendor/etc/qvr/svrapi_config.txt**处。设备优先读取/persist/qvr/路径下的配置文件。