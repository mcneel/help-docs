---
---


# EarthAnchorPoint
{: #kanchor824}
{: #kanchor823}
{: #kanchor822}
{: #kanchor821}
{: #kanchor820}
{: #kanchor819}
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/earthanchorpoint.png](images/earthanchorpoint.png) [Tools](tools-toolbar.html) 
Menus
![images/-no-menu-item.png](images/-no-menu-item.png) [Not on menus.](menuwhattodo.html) 
The EarthAnchorPoint command adds information to the model about the model's position in latitude, longitude, and elevation for GIS mapping applications.
Steps
Enter the earth location.Select a model point that corresponds to the earth location.Select North.Select East.Type identification information.Command-line options
Latitude
Longitude
Elevation
Identification (optional)
Name
URL
URL_tag
Description
Example
TheEarthAnchorPointcommand gives the ability to write Google Earth models. You can model an object, save it as a [Google Earth file (.kml file)](google-earth-kml-kmz-export.html), and then use Google Earth to view the model.
To do this, Rhino needs know how to position the model on the earth. Every model has an "Earth Anchor Point" that contains all the information that is needed to position the model on the earth. The earth anchor point for the Seattle Rhino headquarters might contain this information:
Earth anchor point location
Latitude: 47° 39' 08.54"N (47.653395°)
Longitude: 122° 20' 37.30"W (-122.34384°)
Elevation: 0 (the building is on the ground)
Given that a minute of longitude is roughly 6,000 feet at sea level, then a second would be about 100', and a hundredth of second, about a foot.
Model orientation
Basepoint = (0,0,0) model origin is the southwest corner of the building.
North = (0,1,0) y&#160;axis points north.
East = (1,0,0) x&#160;axis points east.
Identification (optional)
Name: McNeel HQ
Description:
URL: http://www.rhino3d.com
URL tag: Rhino
See also
 [Utility functions](sak-utilities.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](earthanchorpoint.html) 

