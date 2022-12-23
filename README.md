# threeJs
Learning basic of 3js for AR and VR.

WebGLRender --
            uses coordinate system where Y axis point up.
            z-axis point towards the viewer.
            EUS :- East, Up, South.
            X --> East
            Y --> Up
            Z --> South
            
Object are defined using vertices. A single one is                 called vertex,is a vector value. Vector is group of number.
Single number is scalar (Assume 3D Cube --> 8 vertices, 6 faces).
Object is made out of vertices and faces.

When an image is mapped ,a 3d engine needs to know how to place the image on each face that uses it. To facilitates this, a vertex not only has to know the x,y,z values , it also need to know the X and y values of image map, usually called u, v values
let assume 4*4 image 
    u - left to right 
    V - right to left 
    bottom left is (0,0)

In principle, WebJs uses shades, Which is consists of a vertex shader and fragment shader.

vertex shader --> moves the vertex into the normalized clip coordinates.
                  x,y and z between -1 and 1.
         
3JS do the coordinates maths and uses the matrix model.

  Model
  view
  projection

Fragment Shader --> Works at pixel level.
                    Follows the vertex shader and so already has the vertices converted into clip coordinates
                    The purpose of the fragment shader is to determine the color for the individual pixel.

The process of taking the 3D data and turning this into a 2D picture is often called the rendering pipeline.


section 2

To actually show the results of these interactions with the sensor, we'll need to use WebGL (low level api for accessing the GPU on the devices, which is hard to use), 3Js makes it easy use.
The library now includes a WebXR manager that acts as a bridge between the 3D camera and the WebXR.

https://niksgames.com/webxr/

We can set these Geometry in BoxBufferGeometry
Geometry Classes :
   .Box   --> BoxBufferGeometry
   .circle   --> circleBufferGeometry
   .cone 
   .cylinder 
   .dodecahedron 
   .icosahedron 
   .octahedron
   .plain 
   .sphere 
   .tetrahedron 
   .Torus     --> TorusBufferGeometry
   .TorusKnor
   
 Constructive Geometry classes :
   .edges 
   .extrude 
   .lathe
   .parametric 
   .shape 
   .text  
   .cube

Touch Gestures:
  tap, doubletap,quadtap, press, pan, swipe, pinch, rotate,

