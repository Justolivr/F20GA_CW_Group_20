My main object is the campfire in the centre of the entire scene. This involved having to create a log and rock pile, and then a flame that is animated in a low-poly design. Below, for each Version, I give information about what I created, what techniques I used, and if I followed any relevant tutorials.

# Blender_Project_V1

This project contains Tent_Model_V1, a basic outline of the tent, alongside two screenshots documenting the modelling process for the Tent Inner Layer and Tent Doors.

The initial concept was developed using a Microsoft Paint sketch to visualise the intended design. This was combined with open-source reference images found online and a YouTube tutorial (view tutorial) to establish the basic structure of the tent as a background asset. At this stage, the model was still in its early development phase, and no materials had been applied.

The tent doors were created as a separate mesh and mirrored along the Y-axis using Blender's Mirror modifier, with the Tent Inner Layer object serving as the reference for the mirroring operation. To create the decorative lining along the doors, I added a loop cut to the face and adjusted the vertices to follow the diagonal contours of the tent. The doors were then extruded and given additional thickness using a Solidify modifier, providing greater depth and a more defined shape.

# Blender_Project_V2

This project contains Tent_Model_V2, a more complete iteration of the original tent model, incorporating additional geometry, materials and smaller details to improve its overall appearance.

The bed and pillow were created from two basic cubes. These were scaled and flattened to achieve the desired shapes, then bevelled to soften their edges and create a smoother appearance.

The zipper was modelled by adding loop cuts to divide the geometry into three sections. The central face was then extruded outward to create a raised, triangular shape, forming the main body of the zipper detail. Its material was created by increasing the Metallic value of the Principled BSDF shader to 1, giving it a metallic appearance.

The outer tent layer, which acts as a protective windbreaker, was created by duplicating the upper faces of the inner layer and positioning them over the existing geometry. A bevel was then applied to soften the edges and improve the overall finish.
I developed a custom nylon material for this outer layer using Blender's procedural shader system. The material incorporates two Wave Textures oriented in different directions: one following the Z-axis and the other running diagonally. Combining these textures produced a crosshatched lattice pattern resembling woven nylon fabric. A Bump node was also incorporated into the shader to introduce subtle surface variation, creating the illusion of fine fabric texture and adding depth to the material without requiring additional geometric detail.

The tent pegs were modelled using cylinders as a starting point, which were then shaped to achieve the desired form.

The ropes were created using Blender's curve system, allowing them to follow the required paths between the tent and the pegs. A Solidify modifier was applied to give the curves additional thickness and a more realistic, rope-like appearance. The curves were then carefully adjusted to position them accurately within the scene.

The sections wrapping around the tent pegs were created by duplicating a ring-shaped section with a central opening and stacking the duplicates to build up the form. These components were subsequently joined into a single object.

To enhance the appearance of the ropes, I created a procedural material using a Voronoi Texture. This introduced surface variation intended to resemble the fibrous texture of rope. Although the material provided a basic textured appearance, a more advanced version could incorporate additional geometric grooves or finer surface detail to improve realism.
# Blender_Project_V3

# Blender_Project_V4

# Blender_Project_V5

# Blender_Project_V6

# Blender_Project_V7
