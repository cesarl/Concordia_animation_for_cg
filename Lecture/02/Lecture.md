# Amimation for Computer Games - COMP 477

## 08/09/14

---------------
### Personnal notes before course

Interpolation definition :
x0 <= X <= x1

Extrapolation definition :
X < x0 || X > x1


http://paulbourke.net/miscellaneous/interpolation/


#### Polynomial interpolation

First order polynomial function = 2 points
Sedond order polynomial function = 3 points
etc etc ...
Polynomial are good for small number of points, but too much complex for a lot of points.

---------------

### Course

`
vec3 linearInterpolate(vec3 from, vec3 to, float dt)
{
	if (dt > 1.0f)
		return to;
	else if (dt < 0.0)
		return from;
	return ((1.0f - dt) * from) + (dt * to);
}
`

If we have three points :
Polynomial
a*t0^2 + b*t0 + c = x0
a*t1^2 + b*t1 + c = x1
a*t2^2 + b*t2 + c = x2

If I have n points :
a*t0^n + b*t0^(n-1) + c*t0^(n-2) + ...

__TODO___ : Read http://en.wikipedia.org/wiki/Smooth_function

Smooth function have to be at list C1 (>=1)
For most animation cases C1 works well. Sometime we need C2.
The camera path we are up to C2. With the exception of camera path, C2 works well.

------

We'll use spline -> we partition curve into set of points (3 for example)

For spline typicaly we use cubic polynomial.

`
vec3 cubicSpline(vec3 a, vec3 b, vec3 c, vec3 d, float dt)
{
	return a + b*t + c*t^2 + d*t^3;
}
`

------

Squash and stretch

In keyframe animation we don't have physics, and without physics it can look awkward. So we can use squash and stretch.

------

Transformations

- Rigid transformations :
	- Model / View
- Scaling transformations
- Projective transformations
... //see .pdf

Transformations are functions.



