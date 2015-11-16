---
---

What are knots?{: #kanchor3096}
Part of the information needed to define a [NURBS](http://www.rhino3d.com/nurbs) curve is a list of numbers called a *knot vector* and the values of the numbers in this list are called *knots*.
Imagine a rope. If you hold it at the ends, the rope will sag according to the laws of nature (gravity, the stiffness of the rope, etc.) with a polynomial definition. If you tie it off somewhere along its length (by putting knots in it), there will be a different polynomial definition (sag) for each segment between the knots.
The numbers in the knot vector list must be increasing, but the list can contain duplicates. However, a value can be duplicated at most * [degree](changedegree.html) * many times. If a value in the knot vector list is duplicated exactly [degree](changedegree.html) many times, it is called a *fully multiple knot value*.
Examples of valid *knot vectors* for a degree-3 [NURBS](http://www.rhino3d.com/nurbs) curve include:
1, 2, 3, 4, 5, 6 (no fully multiple knot values)
1,1,1,2,3,3,3,4,4,5,6,7,7,7 (here the values 1, 3 and 7 are fully multiple knot values).
-23.456, -3.0, 1.34, 1.34, 99.2, 99.2, 99.2, 100.234, 1.56e45, 1.56e45 (here the value 99.2 is a fully multiple knot value)
 [Open topic with navigation](knot.html) 

