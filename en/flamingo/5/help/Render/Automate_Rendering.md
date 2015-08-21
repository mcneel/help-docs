---
layout: toc-page
---


# Automate Rendering
{: toc-title }

The Flamingo nXt **Render Farm** uses the power of several computers to render single images, batch jobs of multiple images, or view-based animations. Neither Rhino nor Flamingo nXt is required on the computers that are used only as render farm clients.


## <img src="FarmMonitorIcon.png"/>A typical Farm layout
{: .toc-header }

<img src="RenderFarm-002.png"/>

 1. <img src="../Materials/01.png"/>A computer with Rhino and Flamingo nXt.
 1. <img src="../Materials/02.png"/>Network server or shared farm folder.
 1. <img src="../Materials/03.png"/>Two render farm clients. (The nXt Render Farm comes with two free copies of the client software.
 1. <img src="../Materials/04.png"/>Additional purchased render farm clients.

## <img src="FarmMonitorIcon.png"/>The Farm Process
{: .toc-header }

When rendering using Flamingo nXt, instead of rendering a single image with the **Render** command, use the **Render Farm**  *(Flamingo nXt menu &gt; Render Farm)*. This will submit a render job to the [Farm output folder](../General/Options_Flamingo.html#Farm_output_folder). All materials and support information will automatically be submitted along with the job.

The **Render Farm** clients continuously check the farm output folder for a new job. Each client will pick up a part of the job and start to render. The **Farm Monitor**  *(Flamingo nXt &gt; Utilities &gt; Farm Monitor)* keeps track of the job's progress.

Each farm client deposits the results in the farm folder under &lt;&lt; *job name* &gt;&gt;\Output.

Farm output will be in the [nXt image format (.nXtImage)](Image_Editor.html). Images in this format can be edited using the [nXt Image Editor](Image_Editor.html). The results can also be saved as TGA, PNG, TIF, and JPG files from the [nXt Image Editor](Image_Editor.html).

As each client finishes with a job, it will continue to pick up new jobs as they are submitted to the farm.

The Render Farm is free for up to two client computers. To add additional client computers, purchase the **nXt Render Farm** license from [https://www2.mcneel.com/commerce/accurender/buy-farm.asp](https://www2.mcneel.com/commerce/accurender/buy-farm.asp).

The **nXt Render Farm** includes two parts:

 * nXtFarmer.exe (nXtFarmer64.exe)
A small program that runs on each network rendering client and waits for jobs to be generated. Normally, render farms proceed silently without displaying the renderings on a monitor as they progress. Rendering in this manner allows you to use more computer power for lengthy tasks but does not allow interacting with the rendering as it progresses.

 * nXtFarmMonitor.exe (nXtFarmMonitor64.exe)
An applet that shows you the state of your render jobs and provides some simple control tools.

For advanced installations, the nXt Render Farm software lets you work with third-party render managers. The following procedures apply to the Render Farm included with Flaming nXt. If you are planning to use third-party render farm software, some of these procedures will be different.


#### To configure the Render Farm

 * Create a folder to store the Render Farm jobs on a common shared location.
This folder can be on a network server machine or any location that all farm computers can access. All of the farm client computers must have read/write access to this folder. The shared folder should have at least 20GB of available storage.

You must perform the following four steps on all computers you plan to use in the Render Farm, including any nXt workstations that will submit jobs to the render farm:

1.

Install the **nXt Render Farm** software.

2.

From the **Start** menu, run the **Render Farmer** on each machine.

The **Render Farmer** will appear as an icon in the system tray.

3.

 [Right-click](../mouse_button_right.html) on the icon and select **Restore**.

4.

In the **nXt Farmer** window, on the **Options** menu, click **Path** and select the path to the **Render Farm** folder.

 * On the computer with Rhino and Flamingo nXt where you will ready the models to render and submit jobs to the farm, in Rhino, from the **Tools** menu, click **Options**, set the common farm location to the [Farm output folder](../General/Options_Flamingo.html#Farm_output_folder).
The Render Farm is now configured.


#### To verify that the client workstations are responding

 * On any of the client workstations, on the **Windows Start** menu, click **Render Farmer**.
The client machines should appear in the upper list box.


## <img src="FarmMonitorIcon.png"/>Using the Render Farm
{: .toc-header }

Currently, the farm can be used three ways for processing renderings on multiple computers: single rendering jobs, batch jobs, and animations.


## Single Images
{: toc-header }

When rendering single images, each image is split into &quot;slices&quot; and distributed to multiple computers.

The progress of jobs can be viewed with the [Farm Monitor](Automate_Rendering.html#Render_Farm_monitor). As soon as the job is sent, another farm job may be submitted. Newly submitted jobs will queue up in the render farm shared folder. By default, the farm will render the jobs in the order they were received.

To reconstruct the output into a single image, use the [nXt Image Editor, Arithmetic](Image_Editor.html#Arithmetic) function.


#### To submit a single image job to the render farm

1.

In Rhino, configure your rendering and view as you would for a normal rendering.

2.

On the **Flamingo nXt** menu, click **Render Farm**.


## Farm Job Options
{: .toc-header }


### Name
{: .toc-header }

The date and time is automatically pre-pended to the name you choose. A sub-folder for the job is created in the **Render Farm** shared folder. An output folder is also created in the new job folder.

After each job is complete, output can be found in the job's output folder.


### Start job


#### Now

Start the job now.


#### Later (Manually)

Start the job later using the nXt Render Farm Monitor to start the job.


#### After

Start the job at a specified date and time.


### Render constraints


####  [Passes](DocumentProperties_Flamingo.html#Number_of_passes) 


## Batch Jobs
{: toc-header }

Batch jobs let you submit multiple jobs and views to the Render Farm with one command. Each batch rendering will be rendered by a single client computer.


#### To submit a batch job to the render farm

1.

In Rhino, configure your rendering and view as you would for a normal rendering.

2.

On the **Flamingo nXt** menu, click **Render Batch**.


## Batch Render Options
{: .toc-header }


### <img src="BatchRender_Add.png"/>Add
{: .toc-header }

Add a viewport to the batch list.


### <img src="BatchRender_Remove.png"/>Remove
{: .toc-header }

Delete a viewport from the batch list.


### <img src="BatchRender_Properties.png"/>Properties
{: .toc-header }

Set the [Batch Render Properties](Automate_Rendering.html#Batch_Render_Properties).


### <img src="BatchRender_MoveUp.png"/>Move Up
{: .toc-header }

Move the viewport name up in the list.


### <img src="BatchRender_MoveDown.png"/>Move Down
{: .toc-header }

Move the viewport name down in the list.


## Batch List
{: .toc-header }

Displays information about the list of views to be rendered.


## Rendering
{: .toc-header }


### View
{: .toc-header }

Displays pass, scan line, and elapsed time information about the progress of the batch process.


###  <kbd>Stop Rendering</kbd> 
{: .toc-header }

Stops the batch process.


###  <kbd>Render Batch Locally</kbd> 
{: .toc-header }

Uses only the current computer to render the batch jobs. The rendered images will be output to the location specified in the batch job properties.


###  <kbd>Send Batch To Farm</kbd> 
{: .toc-header }

Sends the batch jobs to the [Render Farm](Automate_Rendering.html#Render_Farm). The jobs will be rendered by all available Farm clients. The render images will be output to the shared Farm folder.


## Batch Render Properties
{: .toc-header }


### Viewport to render
{: .toc-header }

See: [Render tab, Viewport to render](Render_Tab.html#ViewToRender).


## Output file
{: .toc-header }


### <img src="BatchRenderSaveButton.png"/>File name
{: .toc-header }

Click the **Save** button and specify a file name for the rendered image.


### Alpha channel
{: .toc-header }

 [Use alpha channel background.](../Environment/Environment_Tab.html#Alpha) 


## Rendering resolution
{: .toc-header }


### Use document settings
{: .toc-header }

See [Render tab, Resolution](Render_Tab.html#Resolution).


## Rendering constraints
{: .toc-header }


###  [Passes](DocumentProperties_Flamingo.html#Number_of_passes) 
{: .toc-header }


## Animation
{: toc-header }

Animations in Rhino can be configured using Rhino's **Animation toolbar**.


#### To submit an animation job to the render farm

1.

Run the [FlamingoNXtAutomateRender](Automate_Rendering.html#FlamingoNXtAutomateRender) command.

2.

In theConfigure Automated Render Commanddialog, select **Render to farm**.

&#160;

Specify theJob name,and click theOKbutton.

&#160;

Set a type of animation from Rhino'sAnimation setuptoolbar. SelectRenderFullas theCapture method.

&#160;

Record the animation from theAnimationtoolbar. The render jobs will be sent to Render Farm.

&#160;

When the jobs are finished in Render Farm, run theFlamingoNXtAutomateRendercommand again and select all the jobs in the dialog.

&#160;

Click theCopy selected files to specified output folderbutton and select a folder where all the render images will be copied to.


## <img src="FarmMonitorIcon.png"/>Render Farm Monitor
{: .toc-header }

The **Render Farm Monitor** is a standalone program that reports the status of the client workstations and the jobs currently in the Farm. Jobs can be suspended and restarted from the monitor and a client workstation can be excluded from participating in the render farm.


## To access the Farm Monitor from Rhino
{: .toc-header }

 * On the **Flamingo nXt** menu click **Utilities** &gt; **Farm Monitor**.

## To access the Farm Monitor from Windows
{: .toc-header }

 * On the **Start** menu click **All Programs &gt; nXt Render Farm &gt; Farm Monitor**.

## Options
{: .toc-header }

Right-click a **Machine** or a **Job** to access options.


### <img src="FarmMonitor_Refresh.png"/>Refresh
{: .toc-header }

Refresh job list.


### <img src="FarmMonitor_SuspendMachine.png"/>Suspend Machine
{: .toc-header }

Exclude workstation from participating in the Render Farm.


### <img src="FarmMonitor_ResumeMachine.png"/>Resume Machine
{: .toc-header }

Resume workstation to participating in the Render Farm.


### <img src="FarmMonitor_SuspendJob.png"/>Suspend Job
{: .toc-header }

Pause the specified job.


### <img src="FarmMonitor_ResumeJob.png"/>Resume Job
{: .toc-header }

Resume the specified job.


### Remove Job
{: .toc-header }

Delete the specified job from the list.


## Licensing the Render Farm
{: .toc-header }

The free version of the Render Farm allows two network computers (nodes) to work on jobs simultaneously. If you wish to have more network nodes running simultaneously, you can purchase an unlimited node license from [https://www2.mcneel.com/commerce/accurender/buy-farm.asp](https://www2.mcneel.com/commerce/accurender/buy-farm.asp).

Once you have purchased your license and have acquired a product key, use the following procedures to license your farm.


#### To authorize the node

1.

Wait for any active farm jobs to complete before beginning your licensing.

2.

Save your **Product Key** to a text file on a network location so you can easily cut and paste it into each node.

3.

If the node is currently active, in the Windows system tray (on the taskbar), **/mouse_button_right.htm');" id="a16" style="position: relative;">right-click** the **Render Farm** icon, and then click **Close**.

4.

Click the **Windows Start** button, and then click **All Programs**.

In the **nXt Render Farm** folder, click **Authorize Farm**.

5.

In the edit box, paste or type your **Product Key** and click **OK**.


#### To start the node

1.

Click the **Windows Start** button, and then click **All Programs**.

In the **nXt Render Farm** folder, click **Render Farmer**.

2.

 **p('../mouse_button_right.htm');" id="a17" style="position: relative;">Right-click** the tray icon, and on the menu, click **Restore**.

3.

On the **Help** menu, click **About**.

If the version number indicates an Evaluation version, licensing has not been successful.

4.

Minimize the **Render Farmer** window to return it to the tray.


## FlamingoNXtAutomateRender command
{: .toc-header }


## Configure Automated Render Command
{: .toc-header }


### Enabled
{: .toc-header }

Redirects the default **Render** command to use the **Render Farm**.


### Use default render dialog
{: .toc-header }

Resets the **Render** command to render directly instead of to the farm.


### Number of render passes to render
{: .toc-header }

Specifies the number of render passes.


### Render to farm
{: .toc-header }

Redirects the **Render** command to render to the farm.


### Job name
{: .toc-header }

Specifies the **Render Farm**  [Job name](Automate_Rendering.html#Job_Name).


## Render constraints
{: .toc-header }


### Number of render passes to render
{: .toc-header }

Specifies the [number of passes](DocumentProperties_Flamingo.html#Number_of_passes).


### Save alpha channel
{: .toc-header }

Saves the [alpha channel](Render_Window.html#Save_with_alpha_channel) background.


## Farm generated output files
{: .toc-header }


### <img src="CopySelectedFiles.png"/>Copy selected files to specified output folder
{: .toc-header }


### <img src="RefreshFileList.png"/>Refresh file list
{: .toc-header }


### <img src="CheckAll.png"/>Check all items
{: .toc-header }


### <img src="UncheckAll.png"/>Uncheck all items
{: .toc-header }

&#160;

