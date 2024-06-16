**Date:** 12-06-2024 00-58
**Tags:** #wiki/sw 
**Uplink:** [[MOC - Programming]]

# Blitting

>[!Definition]
>Blitting is the process of rendering sprite graphics on a background by performing a bitwise operation on the sprite with a mask and pasting them on the background image at a specified spot

Blitting can be computationally expensive due to a two-step process involving VRAM (Video RAM)
- Replacing the changes made to the background as blitting destroys the part of the background where the sprite was drawn
- Blitting the sprite at the new location. The patterns to be replicated are stored in VRAM. This can quickly become suboptimal. In the source code for Doom (1993), the `noblit` command line parameter is provided to disable blitting in order to save computational power