# deepwaters
Unity VR Project - UI/Interaction for Three-dimensional space.


Game objects under VR Lobby (the main VR scene):

Main Camera: Its the point through which the user would enter in to the VR space. 

Main Camera > GvrReticlePointer: The Google Cardboard cursor/pointer for the VR. The pointer expands/contracts depending on its collision with the physical objects (including the interface).

Directional Light: The global light position for the VR scene.

Title & sub-title: The TextMesh labels used to display the title of this project.

Canvas Center, Left, Right: Each canvas includes its respective UI Panels and its contents. The UI elements are wrapped inside their respective canvas because it forms a layer, which helps us to overlap on each other through their z-axis positions. The panel and its child elements are attached with their respective components (C# scripts, audio file) to serve its purpose.

EventSystem: The default input module script for Google VR SDK in Unity.

InputManager: The custom-made input module to launch progress bar and trigger the action when the user clicks on the UI panel to launch the video. The timer set to complete the progress bar is 2 secs.

ObjectFocusManager: To enable Input Manager game object when the UI elements are in center of users’ vision. The user can trigger actions through click only if the UI is in the center of the field of vision. The click availability is indicated by an audio and a text called “press & hold to dive” beneath the reticle pointer.

SceneLoader: A game object attached with Scene Loader script to load 360 degree-videos in their respective VR scenes.

GameObject: To test Game pad inputs (optional).

XRManager: To re-center the VR scene in the camera when it’s launched.



 Directory:

Assets/Google VR: It contains the Google VR SDK assets. I’ve utilized it to incorporate GVR reticle pointer for raycasting in Unity. Raycasting is used to add interactions with physical objects in the space. The unnecessary elements have been removed from the Google VR directory to reduce the file size. Feel free to import the new SDK, if any problem occurs.

Assets/Materials: It contains the material preferences, for example, color for the objects, VR scene background, etc.

Assets/Prefabs: It contains game object & its set preferences, which could be applied to multiple game objects sharing same attributes. Prefab is efficient way to set preferences or add components to the objects sharing same functionality.

Assets/Resources: It contains 360 degree-videos and audio files. Note: The video files have been removed due to heavy space utilization. 

Assets/Scenes: It contains VR scenes. Each scene includes game objects, which is played when the app on the smartphone is running. The scenes could be switched from one to other.

Assets/Scripts: C# scripts that adds functionality and executes the whole VR project. The directory also includes the scripts to support the third-party joystick hardware. Refer to the scripts attached to the respective game objects. They are the ones which are currently being used to run this project.

Assets/TextMesh Pro: It’s a standard Unity package import for using TextMesh game object, for example text labels.

Assets/Textures: It contains images/sprites incorporated in VR 360 background, UI elements and game objects, for example, Shark image in the center UI panel. 
