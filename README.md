# ReflectiveSurfaceTouchDesigner
A simple and cheap trick to fake reflective surfaces on geometry in TouchDesigner

Faking Reflective Surfaces in TouchDesigner
Rey Jarrell
reyjarrell@gmail.com
IG: @rey.nbows
www.reyjarrell.myportfolio.com

Welcome!

This is a cheap and simple trick to fake reflective surfaces - essentially it works by setting a camera within the geometry which we'd like to be reflective, going to that camera's "render," and adjusting the "Geometry" parameter to include only the geometry in the surrounding environment.

We've done that here by putting all the environmental geometry into one base ("Environment") and using "Environment/*" in the "reflection_material" render, instructing it to render all the geometry it finds within that base

Then, the "reflection_material" render is set as the color map for the material we're using on the reflective geometry. The "texture" sop is a great help here! It lets us choose how to map our texture to our geometry so we can get the most realistic-looking effect!

Finally, a second camera is created, and pointed to a final render top (here "render1"). The final render is set to render all the geometry in our scene (we write that by saying * Environment/*) in the "Geometry" parameter. 

Play around, and please reach out if you have any issues or questions!!
