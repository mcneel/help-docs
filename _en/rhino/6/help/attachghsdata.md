---
---


# AttachGHSData
{: #kanchor134}
{: #kanchor133}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/attachghsdata.png](images/attachghsdata.png) [Utilities](utilities-toolbar.html) 
Menus
Tools
Attach GHS Data
The AttachGHSData command adds GHS-specific information to a Rhino model by flagging geometry as GHS objects.
GHS geometry files analyze floating vessels (boats, ships, docks).
Steps
Creating a GHS file is a two-step process:
Use theAttachGHSDatacommand to define portions of the hull.Click **Apply** to save the data as you create it.Use the [SaveAs](save.html#saveas) command to export data to a [GHS file format](ghs-geometry-gf-gft-import-export.html) .GHS Geometry Files (GF)
Before saving a GHS Geometry file, GHS data needs to be associated the surfaces or meshes through theAttachGHSDatacommand.
TheAttachGHSDatacommand adds GHS specific information to a Rhino model by flagging surfaces and meshes as GHS shapes. TheAttachGHSDatacommand defines various parts of a GHS hull, tanks, etc. Only the information defined by theAttachGHSDatacommand is exported to a GHS file when you use theSaveAscommand to save the data.
You can define hulls, tanks, sails, and critical points to be exported to a GHS Geometry File without splitting up Rhino geometry. This includes creating tanks and compartments that are mated with the hull. The exporter has an advanced adaptive sectioning algorithm that will automatically adapt to abrupt changes in section in the hull without having to specify special station points. As you edit the Rhino model, the compartments and tanks are updated.
All data defined using this command are saved with the Rhino model and can be reused when the model is reloaded.
File Structure Reference
The Attach GHS Data dialog box is organized to accommodate the GHS file structure and provides easy access to the GHS file components.

## General Data
Title, Vessel Reference, Owner Reference, Comments
Provide for defining descriptive text associated with a GHS model.
Units
Sets the [units](unit-systems.html) preference for how the model is initially loaded into GHS. This does not affect the way points are stored in the model and can be changed in GHS using the GHS UNITS command.

## Hull Items, Tank Items, Sail Items
These tree nodes provide for grouping GHS parts into three available categories:
Hull Items
Define spaces that displace water.
Tank Items
Define spaces that contain liquids.
Sail Items
Items that do not contain or displace liquids, but are used during wind heeling calculations.
To add a part
Click **Add Part**, and select an object or an existing shape definition on which to base the new component.Each page contains only **Add Part** for adding new parts for each specific category.
## Part
A GHS part is a collection of one or more 3-dimensional volumes (components). The tree's part node will always have one or more child component nodes.
Part Name
A unique 12-character name.
Contents
The fluid that this part contains. Custom fluids may be defined on the Options node of the tree.
Description
Additional description of the part (up to 20 characters).
Add Component
Add an additional 3-D volume to this part. All components in a part are treated as a single space.
Reference Point (Feet)
The reference point is used for various purposes depending on the type of the part. For Tanks, the reference point can mark the point of suction, the point from which an ullage is taken, the point of damage or spilling, etc.
Longitudinal/Transverse/Vertical
Specify the relative distance from the vessel's origin.
Pick button
Pick a location in the model.
No/Has Sounding Tube
Measures the volume of a liquid inside a tank.
Set Tube
Select a curve that represents a sounding tube.
The curve information is copied. Deleting the curve in Rhino has no effect on the part's sounding tube definition.
Deletes the sounding tube information from a part. Removing tube information has no effect on the Rhino geometry.
Delete this Part
Deletes the GHS part information from the Rhino model. This has no effect on the Rhino geometry.

## Component
A component is a single 3-D volume that is defined by a shape and a transformation of that shape.
Component Name
Each component name must be unique for a given part.
Reference Shape
Each component uses a single reference shape to help define its volume. Select a currently defined shape from the menu.
Edit Shape
Edits the reference shape data.
New Shape
Creates a new shape and sets the component to reference the new shape. Old referenced shape is not deleted.
Effectiveness (permeability)
Multiplier for GHS volume and waterplane calculations. These are typically 1.0 for displacers, 0.985 for tanks, and -1.0 or -0.985 for deducting components.
Side
Specifies the mirror transformation on the referenced component.
Port (flipped)
The component is a mirror of the shape definition about the centerplane.
Starboard (same)
The component is the same as the shape definition.
Centerline (mirror)
The component is a combination of the shape and a shape mirrored about the centerplane.
Origin Shift (Feet)
The component's volume is actually the shape translated to a location in space based on a vector.
Longitudinal/Transverse/Vertical
Define the location vector.
Margins (Feet)
Optional values.
Forward/Middle/Aft
Freeboard margins relative to the deck edge.
Create Stations
Creates closed polylines that represent the component and show what would be saved in the GHS file.
Delete This Component
Deletes the component definition. This does not affect Rhino geometry.

## Shapes
Shape definitions are independent of components. This means that multiple components can reference the same shape. This mimics the GHS file format.
Shapes can be defined as intersection of surface and bounding box or as a group of selected curves.{: #kanchor135}
Shapes that are read from a geometry file with shell thickness keep the shell thickness information.
Shape name
Shape names must be unique.
Select Geometry
Select what defines the shape.
BySurface
Defines the shape as the intersection of a Rhino surface and a bounding box.
Select a surface.
ByCurves
Defines the shape as a set of curves. This is the closest match to what is actually exported to the GHS file.
Select a set of curves that represent the stations in a shape. The curve information is copied and saved with the shape. You can delete the Rhino curves without affecting the shape definition.
ByShape
Copy an existing shape definition.
Components that use this shape
Displays all of the components whose geometry is based on this shape.
Edit Component
Select a component and click **Edit Component** to edit the component.
Preview component
When selected, a preview of the selected component is displayed.
When cleared, a preview of the shape definition is displayed.
Geometry defined as a group of curves
Geometry defined as intersection of surface and boundary box
# of Stations
GHS represents volumes by a series of closed polylines (stations). These are cut from the meshes for Rhino geometry. This option defines the minimum number of stations to use to define the shape. Note: It usually does not take a lot of stations to get a good match to the shape. Try to keep the station count to something around 20. This only works ifRefine Stationsis cleared.
Refine Stations
Automatically inserts stations and attempts to create stations where significant changes in station area or shape occur. In most cases, it is best to leave this checked.
Boundary Box Extents
Defines the Longitudinal, Transverse, and Vertical extents of the component. If the entire Rhino geometry is inside the box, all of the geometry will be used.
Click **Pick** to select the extents in the model.
Fit Rhino Geometry
Fits a boundary box to the extents of Rhino geometry.
Delete this Shape
Deletes the current shape. If a component refers to this shape, the component will also be deleted.
Create Stations
Creates stations at the shape level.

## Critical Points
The Critical Points page lets you define locations that are of interest during hydrostatic calculations. This could include downflooding points or measured heights above the waterline.
Add
Edit
Delete
Display Critical Points as [Text Dots](dot.html) 
Point Position

## Options
Specify how the Rhino coordinate system should map to the GHS coordinate system.
Axis Mapping
Maps Rhino x,y,z coordinates to longitudinal, transverse, and vertical coordinates.
Available Fluids
Defines fluids and their specific gravities.
Add
Edit Name
Edit Sprg
Delete

## Conditions
Defines and runs stability conditions on the model while still inside of Rhino. You must own the appropriate applications to run conditions. Contact [Creative Systems](http://www.ghsport.com/home.htm) (makers of GHS) for more information.
Add
Rename
Delete
Copy
Run GHS
Run the analysis.
To save a GHS Geometry file
On theFilemenu, clickSave As.Select theGHS Geometry File (*.gf)type.Type a file name.Click **Save**.
## GHS Part Maker File (PM)
A GHS Part Maker file is a script that is processed by the Part Maker application to create or modify a GHS geometry file. In many cases this is a better alternative than the straight GHS Geometry File export because the script can be modified with notepad to include additional geometric information.
To save GHS Part Maker Files (PM)
From theFilemenu, clickSave As.SelectGHS Part Maker File (*.pm)type.Type a file name.Click **Save** .See also
 [Analyze an object's mass properties](sak-massproperties.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](attachghsdata.html) 

