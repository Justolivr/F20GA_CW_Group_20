\# Unreal\_Project\_V1
Exported the blender scene as an FBX, then loaded it to unreal, with no changes

\# Unreal\_Project\_V2
Agonizingly baked all materials into the objects (including colours, roughness, normal maps) with this tutorial since I was too lazy to recreate the materials (but probably would have been faster)
https://www.youtube.com/watch?v=eE7FedDW2AI

Recreated the fire using a simple niagra emitter
https://www.youtube.com/watch?v=iHoxMCLLGG0

No grass, unfortunately



\# Unreal\_Project\_V3

A simple dark skybox was added, (sort of) completing the migration from blender to unreal (still no grass, annoyingly)
https://www.youtube.com/watch?v=26tx3sW5VnU

This is the beginning of the actual animation section, which will be split into 3 parts:

The camera panning from the moon into the "outside" of the scene, a rig rail which carries the camera from the outside to the main object itself, and the actual object itself moving around.

Currently, the rig rail has been created created.
https://www.youtube.com/watch?v=htS5XBFm2w0



\# Unreal\_Project\_V4



This implements the panning scene of the animation, this was done by using a second camera, with tracking disabled (the other camera tracks the stick). This was done as a separate sequence



The scenes were then combined together

https://www.youtube.com/watch?v=Ry53u3zpSGI



Camera cuts were then added to ensure the correct cameras were being used at all times

https://www.youtube.com/watch?v=MhU29e5SMNA



(To ensure the cameras were perfectly aligned, I copied the camera from the start of the rig rail track, and then renamed it, this took forever)

