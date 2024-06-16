Vertex <-> Texture coordinate 

**Sampling** - Getting texture color from texture coordinate. I would imagine texture colors to be on a continuous spectrum, so sampling is the process of discretizing or picking up particular colors based on the texture coordinates

**Wrapping** - The process of repeating the texture outside the coordinate range. There are different methods of wrapping such as:
	* `GL_REPEAT` - Repeats the texture image as such
	* GL_MIRRORED_REPEAT - Repeats the image but mirrors it each time the wrapping function is called
	* GL_CLAMP_TO_EDGE - Repeats the edge of the texture image and extends it all the way through. It clamps the coordinates between 0 and 1 and those outside the range are clamped down to (0,1), causing the appearance of a stretched edge
	* GL_CLAMP_TO_BORDER - Coordinates outside the range are given a user-defined color

Texture axes -> s, t, r (corresponding to x, y, z)

**Filtering** - Texture interpolation. Textures are comprised of individual texture elements called texels. Texture filtering is the process of mapping texture coordinates to texels. Few types of texture filtering are:
	* GL_NEAREST - Also called nearest-neighbor or point filtering, this method chooses the texel whose center is closest to the given texture coordinate (which explains the "nearest neighbor" name)
	* GL_LINEAR - This method calculates a color for a given texel based on the distance-weighted combination/interpolation of all neigboring texels. The closest texel will have a larger contribution to the final color than the others. 

**Mipmaps** - Rendering high resolution textures on small object (especially when the object is far away in perspective) turns out to be a  waste of memory and is computationally expensive because OpenGL has to compute the right fragment from a large swath of the texture. Mipmaps solve the problem here. Essentially, mipmaps are collections of texture images where each is downsampled by half. So, if the object is small enough, OpenGL switches to a mipmap of the texture, thus saving computational resources and enabling correct fragment calculation