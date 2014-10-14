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

The skeleton hierarchy is in skeleton.out


# Week 3

For skeletal animation

1 - Convert from local transformation to global transformation
2 - Stack transformations

Skinning :

Weight concern bones and not joins.

### Mocap

There is not keyframes and so not interpolations.

Issues :
- Aquisition :
    - There can be error, camera rays can missed each others
    - You need a lot of cameras
    - You have to compute the skeleton from markers

-------

60 degrees around axis(1,1,0) -->
(we have to normalize the axis)
cos(60 / 2) + sin(60 / 2) * (i + j)
Putain je pige rien (cf mes notes sur cahier -> ca va etre a l'exam :/ )

# Week 4

a * b = e ^ (log a b)
= e ^ (log a + log b)

---------

### Space based deformations

#### Barycentric corrdinates :
