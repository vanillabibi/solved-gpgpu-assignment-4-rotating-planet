Download Link: https://assignmentchef.com/product/solved-gpgpu-assignment-4-rotating-planet
<br>



Create a rotating planet as shown below in OpenGL. Implement it with features like transformations, lights, materials, textures, and etc

Requirements:

<ol>

 <li>Draw the planet by creating a quadrics object with gluNewQuadric(), specifying the texturing is desired with gluQuadricTexture(), and drawing a sphere with radius=5, slices=20, and stacks=20, centered around the origin with gluSphere(): GLUquadric *quad = gluNewQuadric(); gluQuadricTexture(quad, 1); gluSphere(quad, 5, 20, 20);</li>

 <li>Set up the perspective projection, camera, and transform the planet so that it is located at the center of the screen facing to your eyes.</li>

 <li>Load scuff.ppm as the source of your texture image to texture mapping the planet. (scuff.ppm is available under</li>

</ol>

/scratch1/jin6/cpsc4780/19_OpenGL_Texture)

<ol start="4">

 <li>Set the background color to black, and the ambient light to blue to make the planet looks like blue in a black space. Set the specular light to highlight the center area of the surface which is facing you.</li>

 <li>Rotating the planet by registering the timer callback function “rotate” to be triggered in at least 25 milliseconds in main():</li>

</ol>

glutTimerFunc(25, update, 0);




and the update function is given below: void update(int value)

{

rotate+=2.0f;

if(rotate&gt;360.f)

{

rotate-=360;

}

glutPostRedisplay();

glutTimerFunc(25,update,0);

}




<ol start="6">

 <li>No keyboard or mouse interaction is required, but you are welcome to play with it for fun.</li>

 <li>Feel free to refer to the sample codes in class, such as planet.c, lightedCube_texture.c, and etc. to accomplish your assignment.</li>

</ol>


