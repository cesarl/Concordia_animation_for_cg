# Amimation for Computer Games - COMP 477

## 03/09/14

Prof Tiberiu Popa
tiberiu.popa@concordia.ca
https://users.encs.concordia.ca/~stopopa/

Programming in C/C++ and OpenGL
That's a program based course.

We gonna learn how to program some technics of animation.

First topic we gonna cover is character animation :
- Skeleton animation

Types of animations :
- Skeleton animation
- Motion capture
- Physicaly based animation
- Soft bodies / Cloth simulation

We'll see :
- Transformation methods
- Skinning
- Reverse kinematic == by rotating my arm, my hand will move -> find the rotation of join to have the good location at the -> example a robot arm who try to kick in a specific location.
- Motion capture
- Mesh deformation
	- Sometines physics and skeleton are not so usefull when I want to morph one mesh into a new one. Example, a human to a bird.
- Cloth simulation
- Facial animation
- Fluid simlation
- Particle systems


-----------------------------------

-----------------------------------

# Week 2

We'll see today how to pose or character.

With patrix the order of transformation makes a difference.

Difference between change of basis and transformations :
- Transformation :
	- Move an object
	- To change the coordiante frame -> for example position of an object from the camera (we multiply by the inverse of the camera transformation)
- Change on basis -> ?

## Lab


	glUnproject(windowX, windowY, windowZ, viewport ...) 
	v = cross(v1, v2);
	v.normalize();


