---
---

{: #kanchor2664}{: #kanchor2665}{: #kanchor2666}{: #kanchor2667}{: #kanchor2668}{: #kanchor2669}{: #kanchor2670}
# Units
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/documentproperties.png](images/documentproperties.png) [File](file-toolbar.html)  [Properties](properties-toolbar.html)  [Standard](standard-toolbar.html) 
Menus
File
Properties
Model unitsproperties manage the units settings for the current model space.
Layout unitsproperties manage the [layout](layout.html) units for the current layout space.
Units and tolerances
Model units
Controls the units used in the model.
Layout units
Controls the units used in the layouts.
When you change from one units system to another, Rhino asks if you want to have the geometry automatically scaled to match the unit change.
{: #absolutetolerance}Absolute tolerance
Tolerance in units used when creating new geometry that cannot be absolutely accurate. For example, trimming surfaces, doing offsets and Boolean operations usually create approximate geometry.
{: #angletolerance}Angle tolerance
Sets the angle tolerance in some commands use to create, modify, or evaluate geometry.
When creating or modifying geometry the angle between two objects will be less than or equal to the tolerance value.
Two objects will meet an evaluation criterion, such as tangency, when the angle between them is less than the tolerance value.
Custom units
Name
The unit name.
Units per meter
Enters a scale in units per meter.
Distance display
Sets the distance display for the status bar and distance and length commands.
Decimal
Sets the display to decimal (1.25).
Fractional
Sets the display to fractional (1-1/4).
Feet &amp; Inches
Sets the display to feet and inches (1'-3").
Display precision
Sets the number of decimal places for the distance display.
Note
It is best to select a tolerance when you start modeling and stick with it.Importing a model in a format that supports units and tolerances will not adjust Rhino's units or tolerances. A dialog box will warn you if the units do not match.The following three items are a good guide to choosing tolerances.Rhino can work in any unit system and with any tolerance. The default unit system is millimeters, and the default tolerance is 0.01 millimeters. You can change the default unit system or tolerance by setting up a template. If you frequently need to work in more than one unit system or with more than one tolerance, set multiple templates.In general, Rhino works best if you choose a unit system whose absolute tolerance is around 0.01 to 0.001, the "size" of a small feature (like a tiny fillet or small curve offset distance) is &gt;= 10 x tolerance, and the "size" of the model is &lt;= 100000.Using an absolute tolerance that is smaller than 0.0001 will noticeably slow some intersection and fitting processes.
## Distance units
{: #distanceunits}
Use any of the Rhino unit measurements including fractions. You can mix fractional and decimal input.
Microns
1.2mic
1.2micron(s)
Millimeters
1.2mm
1.2millimeter(s)
Centimeters
1.2c
1.2cm
1.2centimeter(s)
Meters
1.2m
1.2meter(s)
Kilometers
1.2km
1.2kilometer(s)
Microinches
1.2microinch(es)
Mils
1.2mil(s)
Feet and Inches
1"
1in
1inch(es)
1'2-1/2(")
1'2.2(")
1-1/2"
1.5"
1'
1ft
1foot
1feet
Miles
1mi
1mile(s)
Other
Angstrom
Nanometer
Decimeter
Dekameter
Hectometer
Megameter
Gigameter
Yard
Printer point
Printer pica
Nautical mile
Astronomical unit
Lightyear
Parsec

## Angle units
Use any of the Rhino angle unit measurements including fractions. You can mix input types.
The direction for 0 degrees is 3 o'clock. Positive angular measurement is counterclockwise.
Decimal Degrees
The "°" symbol can be used, but it is easier to just typed.
45 (If no units are specified, then degrees are assumed.)
45°
45d
39deg
22.875degs
12.345e2degree
180degrees
47.653395°
Degrees/minutes/seconds
128d37'22"
128°37'22"
99d37'45.234"
32.543'
32'30.1234"
Radians (1πr=180°)
3.1415926535897932384626433832795r (pi radians)
1.234r
1.234rad
1.234rads
1.234radian
1.234radians
Gradians (100g=90°)
4.00g
4.00grad
4.00grads
Surveyor's units
S47°39'08.54"E
See also
 [Manage document properties](sak-documentproperties.html) 
 [Measure objects](sak-measure.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](units.html) 

