---
---
<!-- TODO: This page needs to be updated more with current automated rendering information.-->

# Automate Rendering
The Flamingo nXt **Render Farm** uses the power of several computers to render single images, batch jobs of multiple images, or view-based animations. Neither Rhino nor Flamingo nXt is required on the computers that are used only as render farm clients.

## A typical Farm layout
{: #render-farm}
![images/renderfarm-002.png](images/renderfarm-002.png)

>![images/01.png](images/01.png)A computer with Rhino and Flamingo nXt.
>![images/02.png](images/02.png)Network server or shared farm folder.
>![images/03.png](images/03.png)Two render farm clients. (The nXt Render Farm comes with two free copies of the client software.
>![images/04.png](images/04.png)Additional purchased render farm clients.

## The Farm Process
{: #the-farm-process}
When rendering using Flamingo nXt, instead of rendering a single image with the **Render** command, use the **Render Farm**  *(Flamingo nXt menu &gt; Render Farm)*. This will submit a render job to the [Farm output folder](options-flamingo.html#farm-output-folder). All materials and support information will automatically be submitted along with the job.
The **Render Farm** clients continuously check the farm output folder for a new job. Each client will pick up a part of the job and start to render. The **Farm Monitor**  *(Flamingo nXt &gt; Utilities &gt; Farm Monitor)* keeps track of the job's progress.
Each farm client deposits the results in the farm folder under &lt;&lt; *job name* &gt;&gt;\Output.
Farm output will be in the [nXt image format (.nXtImage)](image-editor.html). Images in this format can be edited using the [nXt Image Editor](image-editor.html). The results can also be saved as TGA, PNG, TIF, and JPG files from the [nXt Image Editor](image-editor.html).
As each client finishes with a job, it will continue to pick up new jobs as they are submitted to the farm.
The Render Farm is free for up to two client computers. To add additional client computers, purchase the **nXt Render Farm** license from [https://www2.mcneel.com/commerce/accurender/buy-farm.asp](https://www2.mcneel.com/commerce/accurender/buy-farm.asp).
The **nXt Render Farm** includes two parts:

>nXtFarmer.exe (nXtFarmer64.exe)

A small program that runs on each network rendering client and waits for jobs to be generated. Normally, render farms proceed silently without displaying the renderings on a monitor as they progress. Rendering in this manner allows you to use more computer power for lengthy tasks but does not allow interacting with the rendering as it progresses.

>nXtFarmMonitor.exe (nXtFarmMonitor64.exe)

An applet that shows you the state of your render jobs and provides some simple control tools.
For advanced installations, the nXt Render Farm software lets you work with third-party render managers. The following procedures apply to the Render Farm included with Flaming nXt. If you are planning to use third-party render farm software, some of these procedures will be different.

##### To configure the Render Farm
{: #configure-the-render-farm}

>Create a folder to store the Render Farm jobs on a common shared location.

This folder can be on a network server machine or any location that all farm computers can access. All of the farm client computers must have read/write access to this folder. The shared folder should have at least 20GB of available storage.
You must perform the following four steps on all computers you plan to use in the Render Farm, including any nXt workstations that will submit jobs to the render farm:
1. Install the **nXt Render Farm** software.
1. From the **Start** menu, run the **Render Farmer** on each machine.
The **Render Farmer** will appear as an icon in the system tray.
1.  [Right-click](mouse-button-right.html) on the icon and select **Restore**.
1. In the **nXt Farmer** window, on the **Options** menu, click **Path** and select the path to the **Render Farm** folder.

>On the computer with Rhino and Flamingo nXt where you will ready the models to render and submit jobs to the farm, in Rhino, from the **Tools** menu, click **Options**, set the common farm location to the [Farm output folder](options-flamingo.html#farm-output-folder).

The Render Farm is now configured.

##### To verify that the client workstations are responding

>On any of the client workstations, on the **Windows Start** menu, click **Render Farmer**.

The client machines should appear in the upper list box.

## Using the Render Farm
{: #using-the-render-farm-from-flamingo-nxt}
Currently, the farm can be used three ways for processing renderings on multiple computers: single rendering jobs, batch jobs, and animations.

## Single Images
{: #single-images}
When rendering single images, each image is split into &quot;slices&quot; and distributed to multiple computers.
The progress of jobs can be viewed with the [Farm Monitor](automate-rendering.html#render-farm-monitor). As soon as the job is sent, another farm job may be submitted. Newly submitted jobs will queue up in the render farm shared folder. By default, the farm will render the jobs in the order they were received.
To reconstruct the output into a single image, use the [nXt Image Editor, Arithmetic](image-editor.html#arithmetic) function.

##### To submit a single image job to the render farm
1. In Rhino, configure your rendering and view as you would for a normal rendering.
1. On the **Flamingo nXt** menu, click **Render Farm**.

## Farm Job Options

### Name
{: #job-name}
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
{: #render-constraints}

####  [Passes](documentproperties-flamingo.html#number-of-passes)

## Batch Jobs
{: #batch-jobs}
Batch jobs let you submit multiple jobs and views to the Render Farm with one command. Each batch rendering will be rendered by a single client computer.

##### To submit a batch job to the render farm
1. In Rhino, configure your rendering and view as you would for a normal rendering.
1. On the **Flamingo nXt** menu, click **Render Batch**.

## Batch Render Options
{: #batch-render}

### Add
Add a viewport to the batch list.

### Remove
Delete a viewport from the batch list.

### Properties
Set the [Batch Render Properties](automate-rendering.html#batch-render-properties).

### Move Up
Move the viewport name up in the list.

### Move Down
Move the viewport name down in the list.

## Batch List
{: #batch-list}
Displays information about the list of views to be rendered.

## Rendering

### View
Displays pass, scan line, and elapsed time information about the progress of the batch process.

###  **Stop Rendering**
Stops the batch process.

###  **Render Batch Locally**
{: #render-batch-locally}
Uses only the current computer to render the batch jobs. The rendered images will be output to the location specified in the batch job properties.

###  **Send Batch To Farm**
Sends the batch jobs to the [Render Farm](automate-rendering.html#render-farm). The jobs will be rendered by all available Farm clients. The render images will be output to the shared Farm folder.

## Batch Render Properties
{: #batch-render-properties}

### Viewport to render
See: [Render tab, Viewport to render](render-tab.html#viewtorender).

## Output file

### File name
Click the **Save** button and specify a file name for the rendered image.

### Alpha channel
 [Use alpha channel background.](environment-tab.html#alpha)

## Rendering resolution
{: #rendering-resolution}

### Use document settings
See [Render tab, Resolution](render-tab.html#resolution).

## Rendering constraints
{: #rendering-constraints}

###  [Passes](documentproperties-flamingo.html#number-of-passes)

## Animation
{: #animation}
Animations in Rhino can be configured using Rhino's **Animation toolbar**.

##### To submit an animation job to the render farm
1. Run the [FlamingoNXtAutomateRender](automate-rendering.html#flamingonxtautomaterender) command.
1. In theConfigure Automated Render Commanddialog, select **Render to farm**.
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

## Render Farm Monitor
{: #render-farm-monitor}
The **Render Farm Monitor** is a standalone program that reports the status of the client workstations and the jobs currently in the Farm. Jobs can be suspended and restarted from the monitor and a client workstation can be excluded from participating in the render farm.

## To access the Farm Monitor from Rhino

>On the **Flamingo nXt** menu click **Utilities** &gt; **Farm Monitor**.

## To access the Farm Monitor from Windows

>On the **Start** menu click **All Programs &gt; nXt Render Farm &gt; Farm Monitor**.

## Options
Right-click a **Machine** or a **Job** to access options.

### Refresh
Refresh job list.

### Suspend Machine
Exclude workstation from participating in the Render Farm.

### Resume Machine
Resume workstation to participating in the Render Farm.

### Suspend Job
Pause the specified job.

### Resume Job
Resume the specified job.

### Remove Job
Delete the specified job from the list.

## Licensing the Render Farm
{: #licensing-the-render-farm-}
The free version of the Render Farm allows two network computers (nodes) to work on jobs simultaneously. If you wish to have more network nodes running simultaneously, you can purchase an unlimited node license from [https://www2.mcneel.com/commerce/accurender/buy-farm.asp](https://www2.mcneel.com/commerce/accurender/buy-farm.asp).
Once you have purchased your license and have acquired a product key, use the following procedures to license your farm.

##### To authorize the node
1. Wait for any active farm jobs to complete before beginning your licensing.
1. Save your **Product Key** to a text file on a network location so you can easily cut and paste it into each node.
1. If the node is currently active, in the Windows system tray (on the taskbar), **/mouse_button_right.htm');" id="a16" style="position: relative;">right-click** the **Render Farm** icon, and then click **Close**.
1. Click the **Windows Start** button, and then click **All Programs**.
In the **nXt Render Farm** folder, click **Authorize Farm**.
1. In the edit box, paste or type your **Product Key** and click **OK**.

##### To start the node
1. Click the **Windows Start** button, and then click **All Programs**.
In the **nXt Render Farm** folder, click **Render Farmer**.
1.  **p('../mouse_button_right.htm');" id="a17" style="position: relative;">Right-click** the tray icon, and on the menu, click **Restore**.
1. On the **Help** menu, click **About**.
If the version number indicates an Evaluation version, licensing has not been successful.
1. Minimize the **Render Farmer** window to return it to the tray.

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

## Farm generated output files

### Copy selected files to specified output folder

### Refresh file list

### Check all items

### Uncheck all items
&#160;
