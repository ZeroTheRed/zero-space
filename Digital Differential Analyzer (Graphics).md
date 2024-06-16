>[!Definition]
>The Digital Differential Analyzer (DDA) is an algorithm in computer graphics that interpolates between variables in a given interval

DDA is primarily used to rasterize images

Wolfenstein 3D used DDA in ray-casting algorithms for LoS calculations and visual perspectives. In other words, DDA is used to calculate the size of the wall as the player would see it depending on how far they are from it. The closer the player is to the wall, the longer and wider the wall would appear. These calculations are done in 2D 

If $x_k$ and $y_k$ are the $k$th points on a line of slope $m$, then each subsequent point can be calculated as follows in a linear DDA:

$x_{k+1} = x_k + 1$
$y_{k+1} = y_k + m$

This method is for when 0 <= $m$ <= 1. For slopes greater than 1, the equations are reversed as follows:

$x_{k+1} = x_k + \frac{1}{m}$
$y_{k+1} = y_k + 1$

In Doom 1993, DDA was rejected as the game was more realistically 3D than Wolf3D and it made use of more powerful REJECT and BLOCKMAP lumps for LoS perspective calculations and collision/hitbox detection
