---
---

{: #kanchor1758}{: #kanchor1759}{: #kanchor1760}{: #kanchor1761}{: #kanchor1762}{: #kanchor1763}{: #kanchor1764}{: #kanchor1765}{: #kanchor1766}{: #kanchor1767}{: #kanchor1768}{: #kanchor1769}{: #kanchor1770}{: #kanchor1771}{: #kanchor1772}{: #kanchor1773}
# Print
 [![images/transparent.gif](images/transparent.gif)Where can I find this command?](javascript:void(0);) Toolbars
![images/print.png](images/print.png) [Drafting](drafting-toolbar.html)  [File](file-toolbar.html)  [Standard](standard-toolbar.html)  [Viewport Layout](viewport-layout-toolbar.html) 
Menus
File and Layout title
Print
Shortcut
 [Ctrl](ctrl-key.html) +P
The Print command prints an image of the viewport contents.
Includes controls on the left and a constantly updating print preview pane on the right.
The printing tools have to make it as quick and easy as possible to:
Identify what you want to printPosition it on the page where you want itScale the display to something usefulManage line pattern scales and line widthsDisplay print attributes in viewports
To display line widths and colors in viewports, use the [PrintDisplay](printdisplay.html) command or on the [viewport title menu](rhino-window.html), clickPrint Preview.To display linetypes in viewports, use the [LinetypeDisplay](linetypes.html#linetypedisplay) command.{: #destination}Destination
Displays the list of installed printers, including any PDF printer drivers.
Size
Paper sizes supported by the printer.
 **Properties** 
Windows printer driver settings.
Landscape/Portrait
Paper orientation.
Copies ___
Number of copies.
Print to file
Prints to a file.
Output type
Defines the printing method.
Vector Output
Prints lines, curves, and fill areas.
By default, Rhino prints everything it can using vectors.
Raster Output (slow)
Prints a bitmap image.
Output color
Defines how color is printed.
Print color
Uses the layer or property [Print Color](properties.html#printcolor) setting to print curves and wireframes.
Display color
Print objects with the same [wireframe color](properties.html#displaycolor) that displays in viewports.
Black and white
Converts colors to gray scale.
View and Output Scale
List of viewport names and layout pages
Viewport
Prints the current viewport display.
Extents
Zoom the current viewport to contain all objects in the model.
Window
Prints a selected window area.
 **Set** 
Select a new print area. The window grips can be manipulated after the window is drawn.
Move
Move the selected print area.
Multiple layouts
Prints multiple layout pages. Enter a comma-separated list of page numbers or page ranges. For example: 1,2,4-8.
Multiple page prints are sent out as a single print job so printing to PDF should result in a single PDF file with multiple pages.
All layouts
Prints all layout pages.
When printing multiple layouts to image file, multiple image files will be created all with an ascending index suffix appended to the file name.
Scale
Displays current display magnification as percentage. Select scale from the list or set the scale in paper units=model units.
On paper = In model
Sets the units used on the printed page and the equivalent units used in the model.
Margins and Position (model views only)
Sets or expands the non-print areas around the page.
Each of the options controls the position, margins, width, and height options.
Margins
Sets margins for all four sides.
Top, left, width, height
Sets the top and left margins and a width and height for the print area.
Top, right, width, height
Sets the top and right margins and a width and height for the print area.
Bottom, left, width, height
Sets the bottom and left margins and a width and height for the print area.
Bottom, right, width, height
Sets the bottom and right margins and a width and height for the print area.
Centered, width, height
Centers the print area and sets a width and height.
 **Match viewport aspect ratio** 
Sets the margins and position to the same aspect ratio as the selected viewport/layout.
 **Match maximum printable area** 
Sets the margins to the printer maximums.
Position
Centered
Centers the image in the print area.
Offset from
If theCenteredbox is not checked, choose from offset options.
Lower left
Offsets the image in the print area from the lower left.
Upper left
Offsets the image in the print area from the upper left.
Lower right
Offsets the image in the print area from the lower right.
Upper right
Offsets the image in the print area from the upper right.
X, Y, offset values and unit system
Specifies the offset amount in the x and y&#160;directions and sets the offset units.
Linetypes and Line Widths
Linetype
Match pattern definition
Printed line type pattern matches values in [linetype definition file](linetypes.html#linetypedefinitionfile).
Match viewport display
Printed linetype pattern matches the [current display](properties.html#linetype) properties
Line width
Scale by
Multiplier to globally change printed line widths.
Default line width
Ranges fromHairlinethrough normal drafting widths (in millimeters) throughNo Print.
To define your own line widths, add line-width values to the *printwidths.txt* file in the [Rhino support folder](supportfilelocation.html).
Non-scaling objects
Point objects
Size for [point objects](point.html) on the printed page.
Arrowhead size
Size for [arrowheads](arrowhead.html) on the printed page.
Text dot font size
Size for the [text dot](dot.html) font on the printed page.
Visibility
Optional items to include on the printed page.
Show
Background color
Prints the viewport [background color](appearance-colors.html#backgroundcolor).
Wallpaper
Prints the viewport [wallpaper](viewport.html#wallpaper).
The wallpaper will always scale to fit the extents of the print window.
Lights
Prints [light](lights.html) objects.
Clipping Planes
Prints [clipping plane](clippingplane.html) objects.
Only selected objects
Prints [selected objects](selection-commands.html#select-object-basics) only.
Locked objects
Prints [locked](lock.html) objects. Clear the check box to hide locked objects on the printed page.
Grid
Prints the construction plane [grid](grid.html).
Grid axes
Prints the construction plane [grid axes](grid.html#grid-axes-visibility).
Margins
Allows printing a dashed line at the margins.
Text
Notes
Prints the contents of [Notes](notes.html) window.
None
No notes printed.
Top
Prints the notes at the top of the page.
Bottom
Prints the notes at the bottom of the pages
File name
Prints the full file name including path.
None
No file name printed.
Top
Prints the file name at the top of the page.
Bottom
Prints the file name at the bottom of the page.
Printer Details
Displays a description of the currently selected printer details as reported by the driver and configuration settings.
Type
Printer model.
Where
 [Destination.](#destination) 
Paper type
Paper size or size designation.
Printable area
The area of the paper that the printer can use.
Scale X/Scale Y
If the printer requires calibration in order to print exactly, a scale factor can be applied.
See also
 [Use drafting tools](sak-drafting.html) 
&#160;
&#160;
Rhinoceros 6 © 2010-2015 Robert McNeel &amp; Associates.11-Nov-2015
 [Open topic with navigation](print.html) 

