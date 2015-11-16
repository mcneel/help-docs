---
---

{: #kanchor2531}{: #kanchor2532}{: #kanchor2533}{: #kanchor2534}{: #kanchor2535}{: #kanchor2536}{: #kanchor2537}{: #kanchor2538}{: #kanchor2539}{: #kanchor2540}{: #kanchor2541}{: #kanchor2542}{: #kanchor2543}{: #kanchor2544}{: #kanchor2545}{: #kanchor2546}{: #kanchor2547}{: #kanchor2548}
# Entering Numbers
Using numbers in Rhino for distance, angle, and coordinate entry.
There are many ways to enter points, numbers, and angles in Rhino.
No spaces are permitted in a number, angle, or coordinate point.
Basic numbers
Whole numbers
123
Decimal numbers
+123.456
0.456
.456
Scientific notation
-1.23456e10
1.23456E10
Fractions
5/16
1-3/4 (1.75)
You can specify units when typing lengths and point coordinates. Rhino will automatically convert the number you type into the model's units. For example, if your model units are meters and you type 27cm, Rhino automatically converts your number to 0.27.
Example
1.235millimeters
-1.234cm
+16'5" (16 feet 5 inches)
1'2-3/4" (1 foot 2.75 inches)

## X, Y, and Z coordinates
{: #coordinate-entry}
For an introduction to coordinate systems, see: [http://www.mathopenref.com/coordintro.html](http://www.mathopenref.com/coordintro.html).
When prompted for a point, you can click the mouse in a viewport to define the point coordinates or you can or type the coordinates in several ways:
You can type x and y coordinates or x, y and z coordinates to place points. With thewprefix you can type world coordinates, withrprefix relative coordinates, and withwrprefix world relative coordinates.
Construction plane coordinates{: #construction-plane-coordinates}
x,y,z
3,4,5
2,-11 (2,-11,0) When you omit the z coordinate, it is automatically set to 0.
If you type only x and y&#160;coordinates, the point will lie on the construction plane of the active view.
Polar (radius&lt;rotation angle)
17&lt;45
Polar (radius&lt;rotation angle,z)
17&lt;45,8
Spherical (radius&lt;rotation angle&lt;z&#160;elevation angle)
5&lt;30&lt;45
Spherical (x,y&lt;elevation angle)
5,6&lt;15
Surveyor (distance&lt;N/Sangle E/W)
11&lt;N30d22'54.43"W
To use construction plane coordinates
At a prompt for a point, type coordinates in the formatx,y,zand press [Enter](enter-key.html) .Example
Start the [Line](line.html) command and place the first line point at0,0.This starts the line at the construction plane origin.At theEnd of line...prompt, type12,6,10and press [Enter](enter-key.html) .The line is drawn from the construction plane origin to a point 12,6,10 in the construction plane coordinates.{: #world-coordinates}World coordinates
Typewin front of the coordinates, to use the world coordinate system; otherwise the construction plane coordinates of the active view are used.
World x,y,x
w9,3,4
World polar
w78&lt;32
To use world coordinates
At the command prompt, type coordinates in the formatwx,y,zand press [Enter](enter-key.html) .Example
Start the [Line](line.html) command and place the first line point atw0,0,0and press [Enter](enter-key.html) .This starts the line at the world coordinate origin.At theEnd of line...prompt, typew12,6,10and press [Enter](enter-key.html) .The line is drawn from the world origin to a point 12,6,10 in the world coordinates.{: #relative-construction-plane-and-world-coordinates}Relative coordinates
In commands like [Line](line.html) and [Polyline](polyline.html), you can specify relative points.
Construction plane
@3,4 (Move 3 units in the x&#160;direction and 4 units in the y&#160;direction from the previous point.)
r3,4
R3,4
@5&lt;30 (Relative points work with any point format.)
World
@w11&lt;N30d22'54.43"W
Relative polar construction plane
r4&lt;45
@4&lt;45
Relative polar world
rw4&lt;45
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](unit-systems.html) 

