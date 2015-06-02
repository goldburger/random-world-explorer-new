# Random World Explorer

## Final project for CS 174A, Introduction to Computer Graphics, UCLA Spring 2015
### Created by Matthew Goldberg, Zoe (Zhaoyuan) Xi, Shobhit Garg, Neil Bedi

- The proposal described intended advanced topics of generating terrain height using noise function, along with implementing collision detection for cannon shots with terrain. Fully implemented advanced features were terrain height using noise, and environment mapping using a cube map, collision detection. We also attempted object loading capability for 3-D objects but did not fully debug it, so we are leaving it out of this version.

Additional Comments: 
- Project works best on current versions of Firefox or Chrome.
- Our advanced topics include: terrains generated by noise, environmental mapping via a skybox (cube map), collision detection, and 3-D object loading.

### Individual Contributions + Additional Notes:

#### Matt Goldberg
* creation of texture images for cannon
* creation of HUD as an orthographic projection of a texture on top of scene
* code to initialize textures on different texture units
* skeleton for switching between buffers
* cone class for generating cone geometry
* creation of cannon from multiple cone instances and mapped textures
* cannon tracking mouse motion over canvas
* camera controls via mouse pointing for azimuth and altitude
* addition of Phong lighting on cannon from directional source
* debugging of skybox code

#### Zoe (Zhaoyuan) Xi
* in charge of all things environmental
* generated the terrain + skybox
* created the triangle strips mesh used to generate the terrain
* randomly generated the terrain's height using Ken Perlin's simplex noise algorithm. Resources used: ([1](http://staffwww.itn.liu.se/~stegu/simplexnoise/simplexnoise.pdf)) and ([2](https://gist.github.com/banksean/304522))
* texturized the environment via linear and mipmap filters
* implemented the surrounding skybox to encompass the player, camera, and terrain
* created the skybox via cube mapping (environmental mapping); kudos to Matt for helping me debug the cubebox code
* found the [images](http://www.custommapmakers.org/skyboxes.php) used to generate the skybox
* used Youtube and stressed a lot to learn about terrain and skybox generation ahaha. Highly recommend [ThinMatrix's] (https://www.youtube.com/user/ThinMatrix/playlists) GameDev Youtube channel for future CS 174A students :) 

#### Shobhit Garg
* in charge of the shooting functionality and collision detection
* created a Shape superclass that accepts vertices and indices and computes normals and draws the image. This has the ability to draw spheres, cubes, and any shape from a file - all of which inherit from Shape.
* created a framework to display object files. wrote an object loader that reads in vertices, indices, vertex normals; an object of type Shape is created using these and drawn. 
* enabled shooting functionality - an energy beam is shot when player clicks the mouse. This energy beam follows the direction the cannon is facing and travels in a straight line.
* enabled collision detection for the energy beam for intersection with the terrain. 
* credits: Garett Ridge, the TA. 

#### Neil Bedi
* created functionality for changing skybox on number key
* added background music with mute option
* implemented sound effects for controls
* used the [howler.js library](http://goldfirestudios.com/blog/104/howler.js-Modern-Web-Audio-Javascript-Library) for all music additions
* stylized webpage with CSS
* small fixes on player movement
* used the nifty [vivus.js library](https://maxwellito.github.io/vivus/) for animating the start logo
* start logo svg credit: [Bryn Taylor](http://www.flaticon.com/authors/bryn-taylor)

