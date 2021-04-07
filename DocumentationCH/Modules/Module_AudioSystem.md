# Module_AudioSystem
**AudioSystem**模块在于管理音效，SDK中所有组件的交互音效即用此模块管理

## AudioSystem的使用

SDK为开发者提供了`AudioSystem`脚本，位于`SDK\Modules\Module_Audio System\AudioSystem.cs`处，开发者可直接调用此单例的`PlayAudioOnShot`方法。

`  public void PlayAudioOneShot(GameObject target, SCAudiosConfig.AudioType audioType, float volumeScale = 1f) `

* 函数所需的参数`target`为发声物体，`audioType`为音效类型，`volumeScale`为音效的音量大小。
* 当开发者调用此函数方法成功时，此脚本将在场景中实例一个名为`AudioSystem`的游戏对象，此对象上带有`AudioSystem`脚本组件。

## AudiosConfig的自定义

* 若开发者需要自定义触发音效，可双击`SDK\Modules\Module_ AudioSystem \Resources\Configs\ScAudioConfig`，然后在Inspector视图中找到对应的`AudioType`，将自定义的触发音效拖拽进`AudioClip`中。

![AudioConfig](../../Images/Modules/AudioConfig.png)

* 若开发者需扩展交互事件的触发音效,可在`SDK\Modules\Module_ AudioSystem\ScAudioConfig.cs`处,在枚举`AudioType`中添加自定义命名,然后在SCAudioConfig处添加音效片段即可。


