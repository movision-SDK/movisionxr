# SDK Release Notes



## New Features in SDK4.1.2



### Three hand tracking interaction methods added

- `FarPointer`  - remote hand interactions
- `TouchPointer`  -  near-touch hand  interactions
- `GrabPointer`  - grab hand  interactions


- `NearInteractionTouchable`  - the 3D game object with this mounted script can be interacted by near-touch hand
- `NearInteractionTouchableUnityUI`  - the UGUI game object with this mounted script can be interacted by near-touch hand
- `NearInteractionGrabbable`  -  the game object with this mounted script can be interacted by grab hand



### UGUI event system support

- `CanvasCollection`  - this script needs to be mounted to the Canvas game object so that SDK can interact with the UGUI game object



### BoundingBox和ManipulationHandler

- [BoundingBox](./Modules/Module_Interaction/BoundingBox.html) - a component used for rotation and scaling of the object
- [ManipulationHandler](./Module_Interaction/ManipulationHandler.html) - a component used for drag and drop of the object



### New 3DUI components

- [SCImage3D](./Modules/Module_Interaction/SCImage3D.html) - an Image component used to create a 3D version of Image components
- [SCInputField](./Modules/Module_Interaction/SCInputField.html) - an InputField component that pops up a 3D keyboard
- [SCSlider3D](./Modules/Module_Interaction/SCSlider3D.html) - a Slider component based on BoxCollider
- [SCToggle3D](./Modules/Module_Interaction/SCToggle3D.html) - a Toggle component based on BoxCollider



### Additional Hand touch events

- IPokeDownHandler - the event that is triggered when the index finger enters the Collider component
- IPokeUpHandler - the event that is triggered when the index finger leaves the Collider component
- IPokeUpdateHandler - the event that is triggered by every frame when the index finger is in the Collider component





## Known issues in SDK4.1.2



### Version Unity2019.3.x will have issues with memory leaks

It is therefore recommended to use Unity2019.2.3f1



### The click direction of the near-touch hand currently only supports the negative direction of the Z axis

It is recommended to face the negative direction of the Z axis of the game object to the operator if using hand operations



### SCImage3D does not support Sprite

Currently it only supports Texture2D. Images using three by three grids cannot be supported properly



### Drag may affect clicks

Since the stability of the raycaster /laserpointer related operations is not as high as a mouse, a slight jitter when clicking may trigger the Drag event. Currently the temporary solution is to increase the value of Drag Threshold on the EventSystem component.
