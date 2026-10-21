# The modelling process for the objects

The rough process looked this:

Model the stick
model the trees (background obj)
Model the campfire (background obj)
Assemble everything into a scene

Detailed breakdowns for each folder, to show incremental progress can be found below


# Blender_Project_Files_V1
The initial outline of the stick was first created, using a plane, with a skin modifier being used to give the outline geometry
https://www.youtube.com/watch?v=4aDbM9Tpp1M

# Blender_Project_Files_V2
The wrapping around the stick handle was created, by creating a cylinder around the profile of the stick.
Loop cuts were manually created in order to ensure the object did not have large gaps in the wrapping
These gaps were then removed, and the remaining parts were shrinkwrapped to the handle, then subdivided and solidified
https://www.youtube.com/shorts/gaHBzs-_Zzg

At this stage, a marshmallow was also created, which is a cylinder with a simple bevel

# Blender_Project_Files_V3
THe stick was then textured, using this tutorial
https://www.artstation.com/blogs/jsabbott/3ZXjq/how-do-you-create-a-procedural-tree-bark-material-in-blender-51

The marshmallow was also textured, following this tutorial
https://www.youtube.com/watch?v=CI2MjV2u6PY

The stick cloth wrapping was also textured, using a prefabricated cloth texture (this was removed and replaced in V6)
https://ambientcg.com/view?id=Fabric066

# Blender_Project_Files_V4
The leaves were created, then attached to the stick.

Note the pink textures for the wrapping, Blender kept crashing on my laptop so I decided to do the rest of the modelling on my home PC, which is significantly more powerful.

# Blender_Project_Files_V5
The background objects were created

These consisted of low poly trees, which are several hexagons stacked on top of each other, with the "top" scaled to be a smaller size than the base.
the bottom of these hexagons were also inset, so when the hexagons are stacked on top of each other, they can be slightly rotated to add some flair.
https://www.youtube.com/watch?v=p-9pgZI3inI

The campfire was also created,
these consisted of 6 logs, and then surrounded by some rocks

Low poly fire was created using particle emitters and cubes, and then placed inside the logs with a light object
https://www.youtube.com/watch?v=UJvZli5bVs8

Grass was also added with particle effects, following this guide.
https://www.youtube.com/watch?v=vif_oBwkQBM

The scene was then assembled together.

# Blender_Project_Files_V6
This version refines the scene, adding more textures, as well as making the logs look more natural.

The wood texture from the stick was edited so it is much more visibile, and this was applied to the stick, trees, and logs.

A wave texture was also added to the logs, to make them more natural and visually interesting
https://www.youtube.com/watch?v=S_cVg3umc6A

The logs were also recreated to have a higher vertice count.

The cloth wrapping texture was changed to be more visible, getting rid of the prefabricated materials.

The rocks and tree leaves also made use of some voronoi, noise, bump textures to make the more interesting.

Another light object was placed high above to replicate the moonlight, and the camera was carefully positioned to create a cosy scene.
