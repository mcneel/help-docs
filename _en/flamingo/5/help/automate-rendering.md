---
title: Automated rendering
---

# {{page.title}}


## Batch rendering
{: #batch-rendering}
Batch jobs let you submit multiple jobs to be rendered automatically. A Batch job can specify a specific view, resolution and number of passes. Batch renderings can be started on a single or sent out the [Render Farm](render-farm.html). Open the Batch list and add jobs to the list. The batch jobs list will be saved in the model.

##### Where can I find this command?

 * Menus > Flamingo nXt 5.0 > More Tools > Batch Render

### Batch Render Dialog
{: #batch-render}
Start by adding a job, then edit the properties to set up batch jobs.

#### Add
Each Batch job is based on a view saved in the model.  Click on the Add item to select from a list of views in the model.  All the other menu items will activate once a job is added and selected.

#### Delete
Select an existing batch job.  Then use Delete to remove the job from the batch list.

#### Properties
Select an existing batch job, then use Properties to set the [Batch Render Properties](#batch-render-properties).  Properties include file name, resolution, and number of passes for each job.

#### Move Up
Move the viewport name up in the list.

#### Move Down
Move the viewport name down in the list.

#### Batch List
{: #batch-list}
Displays information about the list of views to be rendered. Double-click on an existing job to edit set the [Batch Render Properties](#batch-render-properties).

#### Rendering Status
Displays pass, scan line, and elapsed time information about the progress of the batch process.

####  Stop Rendering
Stops the batch process.

#### Render Batch Locally
{: #render-batch-locally}
Uses only the current computer to render the batch jobs. The rendered images will output to the location specified in the [Batch Render Properties](#batch-render-properties).

####  Send Batch To Farm
Sends the batch jobs to the [Render Farm](render-farm.html). The jobs will be rendered by all available Farm clients. The render images will output to the shared Farm folder.

### Batch Render Properties
{: #batch-render-properties}

#### Viewport to render
Shows the view that this job will render. See [Render tab, Viewport to render](render-tab.html#viewtorender).

#### File name
Click the Save button ![images/saveimageas.png](images/saveimageas.png){: .inline} and specify a file name for the rendered image.

#### Alpha channel
Save the image with the Alpha Channel.  See the [Use alpha channel background](environment-tab.html#alpha) for more details.

#### Use document settings
{: #rendering-resolution}
The default is to use the current document resolution settings to render.  If another resolution is needed, then uncheck this box and specify a resolution. See the [Render tab, Resolution](render-tab.html#resolution) topic for more details.

#### Rendering Constraints Passes
{: #rendering-constraints}
Set the number of passes needed to finish the batch job.  See the [Passes](documentproperties-flamingo.html#number-of-passes) topic for more details.

<!-- TODO: Flamingo nXt 5 runs from the RDK.  The need to Flamingo Automate render is not clear.  What is needed to run animations with nxt right now?
The number of passes and the ability to send a render to the farm are required still.  So the dialog should be smaller.
Alpha channel This needs to be investigated. The rest of this section is commented out.-->

<!-- Commented out until automated render can be determined

## Animations
{: #animation}
There are two ways to create animations in Rhino.  Animations can be configured using [Rhino's Animation toolbar](http://docs.mcneel.com/rhino/5/help/en-us/index.htm#commands/animation.htm) or using the [Bongo](http://bongo.rhino3d.com/) animation plugin.

##### To submit an animation job to the render farm
1. Run the [FlamingoNXtAutomateRender](automate-rendering.html#flamingonxtautomaterender) command.
1. In the Configure Automated Render Command dialog, select **Render to farm**.
&#160;
Specify the Job name,and click the OK button.
&#160;
Set a type of animation from Rhino's Animation setup toolbar. Select Render Full as the Capture method.
&#160;
Record the animation from the Animation toolbar. The render jobs will be sent to Render Farm.
&#160;
When the jobs are finished in Render Farm, run the FlamingoNXtAutomateRender command again and select all the jobs in the dialog.
&#160;
Click the Copy selected files to specified output folder button and select a folder where all the render images will be copied to.


## FlamingoNXtAutomateRender command
{: #flamingonxtautomaterender}


## Configure Automated Render Command

### Enabled
Redirects the default **Render** command to use the **Render Farm**.

### Use default render dialog
Resets the **Render** command to render directly instead of to the farm.

### Number of render passes to render
Specifies the number of render passes.

### Render to farm
Redirects the **Render** command to render to the farm.

### Job name
Specifies the **Render Farm**  [Job name](automate-rendering.html#job-name).

## Render constraints

### Number of render passes to render
Specifies the [number of passes](documentproperties-flamingo.html#number-of-passes).

### Save alpha channel
Saves the [alpha channel](render-window.html#save-with-alpha-channel) background.
-->
