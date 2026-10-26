My main object is the campfire in the centre of the entire scene. This involved having to create a log and rock pile, and then a flame that is animated in a low-poly design. Below, for each Version, I give information about what I created, what techniques I used, and if I followed any relevant tutorials.


# Blender_Project_V1 - Initial Tent Model

This project contains Tent_Model_V1, a basic outline of the tent, alongside two screenshots documenting the modelling process for the Tent Inner Layer and Tent Doors.

The initial concept was developed using a Microsoft Paint sketch to visualise the intended design. This was combined with open-source reference images found online and a YouTube tutorial (view tutorial) to establish the basic structure of the tent as a background asset. At this stage, the model was still in its early development phase, and no materials had been applied.

The tent doors were created as a separate mesh and mirrored along the Y-axis using Blender's Mirror modifier, with the Tent Inner Layer object serving as the reference for the mirroring operation. To create the decorative lining along the doors, I added a loop cut to the face and adjusted the vertices to follow the diagonal contours of the tent. The doors were then extruded and given additional thickness using a Solidify modifier, providing greater depth and a more defined shape.

Tutorial for initial tent shape: https://www.youtube.com/watch?v=-EZ6owvtbH8

# Blender_Project_V2 - Details to Tent Model

This project contains Tent_Model_V2, a more complete iteration of the original tent model, incorporating additional geometry, materials and smaller details to improve its overall appearance.

The bed and pillow were created from two basic cubes. These were scaled and flattened to achieve the desired shapes, then bevelled to soften their edges and create a smoother appearance.

The zipper was modelled by adding loop cuts to divide the geometry into three sections. The central face was then extruded outward to create a raised, triangular shape, forming the main body of the zipper detail. Its material was created by increasing the Metallic value of the Principled BSDF shader to 1, giving it a metallic appearance.

The outer tent layer, which acts as a protective windbreaker, was created by duplicating the upper faces of the inner layer and positioning them over the existing geometry. A bevel was then applied to soften the edges and improve the overall finish.
I developed a custom nylon material for this outer layer using Blender's procedural shader system. The material incorporates two Wave Textures oriented in different directions: one following the Z-axis and the other running diagonally. Combining these textures produced a crosshatched lattice pattern resembling woven nylon fabric. A Bump node was also incorporated into the shader to introduce subtle surface variation, creating the illusion of fine fabric texture and adding depth to the material without requiring additional geometric detail.

The tent pegs were modelled using cylinders as a starting point, which were then shaped to achieve the desired form.

The ropes were created using Blender's curve system, allowing them to follow the required paths between the tent and the pegs. A Solidify modifier was applied to give the curves additional thickness and a more realistic, rope-like appearance. The curves were then carefully adjusted to position them accurately within the scene.

The sections wrapping around the tent pegs were created by duplicating a ring-shaped section with a central opening and stacking the duplicates to build up the form. These components were subsequently joined into a single object.

To enhance the appearance of the ropes, I created a procedural material using a Voronoi Texture. This introduced surface variation intended to resemble the fibrous texture of rope. Although the material provided a basic textured appearance, a more advanced version could incorporate additional geometric grooves or finer surface detail to improve realism.
# Blender_Project_V3 - Backpack and Log Piles

This project focuses on creating two additional background assets for the campsite scene: a backpack and a pile of logs. Although the log pile underwent significant changes in later iterations, this version is included to document my initial design decisions and modelling process.

The backpack was modelled by following a YouTube tutorial (view backpack modelling tutorial). While the tutorial provided guidance for the modelling process, I created the materials myself, allowing me to customise the backpack's appearance to suit the overall aesthetic of the campsite.

The log pile was created by first modelling a single log, which was then duplicated and arranged into a stack. I began with a cylinder and used the extrusion and scaling tools on both ends to create smaller inner circles surrounded by additional faces. This formed the basis for the cut ends of the log.To make the logs appear more natural, I adjusted individual faces along the length of the cylinder, introducing irregularities and reducing the uniformity of the shape. I also extruded the faces surrounding the inner circle to create the appearance of remaining bark around the cut ends. Once the initial log was complete, I duplicated it several times and arranged the copies into a pile.

Two separate procedural materials were created for the logs: one for the outer bark and another for the exposed wood on the cut ends.

The bark material used a Noise Texture to introduce surface variation, helping to create a less uniform appearance.

For the cut ends, I used a Random Per Island geometry node to generate variation between disconnected mesh islands. Its output was connected to a Math Add node to modify the resulting values before feeding them into a Wave Texture set to the Rings profile along the Z-axis. This produced the concentric pattern needed to represent the tree rings.

Although the initial material achieved the desired appearance, the log pile was substantially revised in a later iteration to improve the overall result.

The tutorial (Backpack) - https://www.youtube.com/watch?v=upbLsVptfSE&t=4210
# Blender_Project_V4 - Campfire (Main Object) Development.

This was the start of the creation for my main object, which is the campfire. I was inspired by Breath of The Wild's Fire texture, and so I wanted to recreate the type of flame.

I modelled the firepit before creating the flames. To add variety to the arrangement, I created four different rock variations using a combination of random extrusions, scaling and bevel cuts along different axes. These techniques allowed me to alter the silhouettes of the rocks, creating irregular shapes that more closely resembled natural stone. I also applied a Displace modifier to introduce additional surface irregularities and create the appearance of cracks and uneven edges between the stones. This helped break up the uniformity of the geometry and gave the firepit a more natural appearance.

The rock material was created using a procedural shader network consisting of three parallel Noise Textures, each connected to a corresponding Voronoi Texture. Colour Ramp nodes were used to control the colours and contrast produced by these texture combinations. By making outputs into a single material, I was able to create variations in colour and surface detail without relying on image textures. This gave the rocks a more complex, stone-like appearance while keeping the material fully procedural.

The logs surrounding the campfire were created by reusing the log model developed in Project V3. I duplicated the original log, adjusted its scale and rotated the copies around the firepit to create the arrangement.
I tried to join the logs into a single object, but this caused the procedural tree-ring patterns to converge towards a common centre rather than remaining centred on each individual log. As a result, I kept the logs as separate objects to preserve their intended appearance and maintain the correct positioning of the tree rings.
The logs retained the same procedural bark and cut-wood materials developed in Project V3.

To create the flame geometry, I started with an Icosphere and increased its level of geometric detail. I then moved one of its faces upward to create an elongated, teardrop-like silhouette. The shape was smoothed and modified using a Displace modifier. I changed the displacement texture type to Marble, which introduced subtle surface irregularities while retaining the overall smooth appearance of the flame. This helped create a stylised flame shape rather than a perfectly uniform mesh. To introduce movement, I added a driver that rotated the flame between keyframes. This provided a basic animation effect, giving the fire a sense of movement rather than leaving it as a static object.

The flame material was developed using two Gradient Textures to create distinct inner and outer flame layers. Each gradient was connected to its own Colour Ramp, allowing me to control the colour transitions and create variation between the two layers. An Emission shader was used to give the flames their bright, luminous appearance. I also incorporated a Layer Weight node using its Facing output to control the blending between the inner and outer layers, helping define the separation between them.To further refine the colour blending, I used Blender's Mix Color node with the Color Dodge blend mode. This brightening operation was incorporated into the colour-processing network alongside two Colour Ramp nodes to adjust the resulting colours and contrast. 
Finally, a Mix Shader was used to combine the two gradient-based flame layers, with the Layer Weight output controlling the blending factor. This produced the original campfire material, creating a stylised flame with layered colours, a bright centre and a more defined outer edge.

# Blender_Project_V5 - Log Pile V2

For this version, I focused on improving the appearance and realism of the logs, particularly their surface texture and level of detail. I began by using the Random Select tool to select and extrude faces on the cylinder, creating an irregular shape that more closely resembled a natural log. I then used Blender’s Sculpting tools to create lines running along the length of the cylinder, representing the texture and grooves of tree bark. I also sculpted the circular ends of the logs to introduce additional detail to the tree rings.

Next, I used Texture Paint to work with the log’s UV layout. I applied a plain texture and painted selected areas lighter or darker to create greater variation in the surface colour. This helped add depth and made the logs look more realistic than the previous version.

I retained the existing procedural materials, including the material used to create the tree rings, but adjusted several of their values to achieve a more natural appearance. Overall, I was much happier with the result, as the additional sculpting and texture painting gave the logs more character and detail. Once the new models were complete, I replaced the previous logs in both the log pile and the campfire arrangement with the improved versions.

# Blender_Project_V6 - Initial Scene Creation

I began constructing the environment by creating a large ground plane and subdividing it to provide additional geometry. I then extruded individual faces upwards and downwards to produce an uneven terrain. Using the scroll wheel to increase the smoothing during this process helped create a more natural, bumpy surface.

To add grass, I used a Hair Particle System with a Particle Emitter. I configured the particles to use Newtonian physics and introduced a Brownian force to create random movement and variation in their orientations. This helped the grass appear more naturally distributed rather than uniformly placed across the ground.

I then brought the previously created assets into the scene, including the tent, backpack, campfire, logs and other campsite objects. I also modelled the trees by following the tutorial linked below. These trees used relatively simple materials, as the main focus at this stage was to establish the overall environment and composition. After assembling the main assets, I began positioning the camera and considering how the scene would be lit and rendered. This allowed me to start evaluating the composition and identify areas that would need further development.

Finally, I added zipper rows to the tent to improve its level of detail. I created a single zip component and used an Array modifier to duplicate it along the tent lining. I then positioned the duplicated geometry against the lining to create a more convincing and detailed finish.

Tree tutorial - https://www.youtube.com/watch?v=p-9pgZI3inI

# Blender_Project_V7 - Full Scene Creation

In this stage, I focused on refining the overall scene composition, improving the lighting and atmosphere, and adding small animated details to make the environment feel more alive.

I first adjusted the camera angle to achieve a more effective composition for the final render. My initial test renders relied almost entirely on the emission from the campfire flame. However, the scene appeared too dark, so I decided to introduce additional lighting around the fire.

I added a Point Light inside the flame and set its power to 800 W. I gave it an orange colour to match the fire and increased its radius to produce softer illumination across the nearby objects. I also adjusted the light’s falloff to help create a more natural transition between the illuminated area and the surrounding darkness. This significantly improved the visibility of the campsite and created a more convincing campfire lighting effect.

To improve the background atmosphere, I added a cube surrounding the area behind the trees to act as a fog volume. I removed the surface appearance to make the volume transparent and configured its material with a dark blue colour, anisotropy and density. This introduced a layer of atmospheric fog behind the trees, helping create a greater sense of depth and giving the scene a more cinematic nighttime appearance.

Finally, I wanted to add small glowing particles around the campfire to create the effect of fireflies. I followed a Geometry Nodes tutorial that demonstrated how to generate and animate these particles procedurally.
When using Cycles, these emissive particles can also contribute light to the surrounding scene.

Overall, these additions helped transform the individual models into a more complete environment. The improved lighting, background fog and animated glowing particles gave the campsite greater atmosphere and visual interest, bringing the scene closer to the intended cinematic style.

# Rendering

I used Cycles instead of EEVEE because I just preferred the way the light reflects. As I was trying to go for a bit more realism, I thought using it would make the ambience of my scene look fleshed out. I was using GPU Compute. I was denoising using Nvidia's OptiX. The render had 256 max samples. I also had the colour Tranform Property to Standard as I preferred the colours compared to other ones like RGBx.
