---
title: Farm Rendering
---

# {{page.title}}
The Flamingo nXt Render Farm uses the power of several computers to render single images, batch jobs of multiple images or view-based animations. Neither Rhino nor Flamingo nXt is required on the computers used only as render farm clients.

#### A typical Farm layout
{: #render-farm}

![images/renderfarm-002.png](images/renderfarm-002.png){: style="margin-top:25px;"}

>![images/01.png](images/01.png)A computer with Rhino and Flamingo nXt.
>![images/02.png](images/02.png)Network server or shared farm folder.
>![images/03.png](images/03.png)Two render farm clients. (The nXt Render Farm comes with two free copies of the client software.)
>![images/04.png](images/04.png)Additional purchased render farm clients.

The Render Farm is free for up to two client computers. To add more client computers, purchase the nXt Render Farm license from [https://www2.mcneel.com/commerce/accurender/buy-farm.asp](https://www2.mcneel.com/commerce/accurender/buy-farm.asp).

#### Shared Farm folder
{: farm-folder}
The key to a functional render farm is a shared folder to which the master machine and all the client computers can access.  This is normally a shared network folder.  It can be a folder on the master machine or on a network.  The folder does not have to be assigned to the same name on each client, but each client does need full read/write/delete access to the folder.  The shared folder should have at least 20GB of available storage.

#### The nXt Render Farm includes two Applications:

##### The Farmer render client (nXtFarmer64.exe)
A small program that runs on each network rendering client and waits for jobs to be generated. Normally, render farms proceed silently without displaying the renderings on a monitor as they progress. Rendering in this manner allows you to use more computer power for lengthy tasks but does not allow interacting with the rendering as it progresses.

##### The Farm monitor (nXtFarmMonitor64.exe)
An applet that shows you the state of your render jobs and provides some simple control tools.
For advanced installations, the nXt Render Farm software lets you work with third-party render managers. The following procedures apply to the Render Farm included with Flamingo nXt. If you are planning to use third-party render farm software, some of these procedures will be different.

#### The Farm Process
{: #the-farm-process}
 1. To start a rendering using Flamingo nXt farm, instead of using the standard Render command, use the Render Farm *(Flamingo nXt 5.0 menu &gt; Render Farm)*. This will submit a render job to the [Farm output folder](options-flamingo.html#farm-output-folder). All materials and support information will automatically be submitted along with the job.
 2. Render jobs are split into many different farm tasks. The Render Farm clients continuously check the farm output folder for new tasks. Each client will pick up a task and start to render. The Farm Monitor  *(Flamingo nXt 5.0 &gt; Render Farm &gt; Farm Monitor...)* is a good way to keep track of the job's progress.
 3. Each farm client deposits the results in the farm folder under *job name* \Output.
 3. As each client finishes with a job, it will continue to pick up new jobs as they are submitted to the farm.
 4. Farm output will be in the [nXt image format (.nXtImage)](image-editor.html). Images in this format can be edited using the [nXt Image Editor](image-editor.html). The results can also be saved as TGA, PNG, TIF, and JPG files from the [nXt Image Editor](image-editor.html).

## Install and configure the Farm
{: #install}
The Farmer render client and the Farm monitor are installed with Flamingo on the master Rhino machine.  For other client computers that do not have Rhino and Flamingo nXt, the Farmer client needs to be installed.

##### Installing the Render Farmer
For machines that do not have Rhino and Flamingo installed, install the Farmer client:

 1. Download the current [Render Farmer software](http://www.rhino3d.com/download/The-Farm/1.0/release).
 1. Run the downloaded installer on each of the client computers.
 1. From the Start menu, run the Render Farmer on each machine.
 1. The Render Farmer will appear as an icon in the system tray.

##### To configure the Render Farm
{: #configure-the-render-farm}
1.  [Right-click](mouse-button-right.html) on the icon and select Restore.
1. In the nXt Farmer window, on the Options menu, click Path and select the path to the Render Farm folder.

On the computer with Rhino and Flamingo nXt set the Zoo folder in Rhino. From the Tools menu, click Options, set the common farm location to the [Farm output folder](options-flamingo.html#farm-output-folder).

The Render Farm is now configured.

## Using the Render Farm
{: #using-the-render-farm-from-flamingo-nxt}
Currently, the farm can be used three ways for processing renderings on multiple computers: single rendering jobs, batch jobs, and animations.

##### To verify that the client workstations are responding
After starting the Render Farmer client on all the client computers:

 1. On any of the computer, in the Windows Start menu, click [Farm Monitor](#render-farm-monitor).
 1. The client machines should appear in the upper list box.
 1. Each Render Farmer client should be listed under the Machine list.  The Status should read Active.

If there is a problem with this, review the [install](#install) and [configuration topics](#configure-the-render-farm).


##### To submit a job to the render farm
1. In Rhino, configure your rendering and view as you would for a normal rendering.
1. On the Flamingo nXt menu, click Start Farm Render.
1. The [Farm Job](#farm-job) dialog should appear.
1. Verify the correct option and hit OK.


##### Monitoring the Farm
After submitting a job to the Render Farm, use the [Farm Monitor](#render-farm-monitor).

 1. On the master computer, in the Windows Start menu, click [Farm Monitor](#render-farm-monitor).
 1. A recent job should show up in the Jobs list. This can take a few minutes for large jobs.
 1. The status of the job will change to active.
 1. After a period of time, the machines above should pick up tasks with the same date.
 1. The Percent complete increases as tasks are completed.
 1. Watch for the job status Completed when the job is finished.


## Farm Job Options
{: #farm-job}

#### Name
{: #job-name}
The date and time is automatically pre-pended to the name you choose. A sub-folder for the job is created in the Render Farm shared folder. An output folder is also created in the new job folder.
After each job is complete, output can be found in the job's output folder.

#### Start job
Job may be started immediately after submission, at a later time, or manually through the Farm monitor.

#### Now
Start the job now.

#### Later (Manually)
Start the job later using the nXt [Farm Monitor](#render-farm-monitor) to start the job.

#### After
Start the job at a specified date and time.

#### Rendering Constraints Passes
{: #rendering-constraints}
Set the number of passes needed to finish the batch job.  See the [Passes](documentproperties-flamingo.html#number-of-passes) topic for more details.


## Render Farm Monitor
{: #render-farm-monitor}
The Render Farm Monitor is a stand-alone program that reports the status of the client workstations and the jobs currently in the Farm. Jobs can be suspended and restarted from the monitor and a client workstation can be excluded from participating in the render farm.

To access the Farm Monitor from Rhino go to the Flamingo nXt 5.0 menu > Render Farm > Farm Monitor.

To access the Farm Monitor from Windows, on the Start menu click **All Programs > nXt Render Farm > Farm Monitor**.

#### Options
Right-click a Machine or a Job to access options.

#### Refresh
Refresh job list.

#### Suspend Machine
Exclude workstation from participating in the Render Farm.

#### Resume Machine
Resume workstation to participating in the Render Farm.

#### Suspend Job
Pause the specified job.

#### Resume Job
Resume the specified job.

#### Remove Job
Delete the specified job from the list.

## Licensing the Render Farm
{: #licensing-the-render-farm-}
The free version of the Render Farm lets two network computers (nodes) work on jobs simultaneously. If you wish to have more network nodes running simultaneously, you can purchase an unlimited node license from [https://www2.mcneel.com/commerce/accurender/buy-farm.asp](https://www2.mcneel.com/commerce/accurender/buy-farm.asp).

Once you have purchased your license and have acquired a product key, use the following procedures to license your farm.

##### To authorize the node
1. Wait for any active farm jobs to complete before beginning your licensing.
1. Save your Product Key to a text file on a network location so you can easily cut and paste it into each node.
1. If the node is currently active, in the Windows system tray (on the taskbar), [right-click](mouse-button-right.html) the Render Farm icon, and then click **Close**.
1. Click the **Windows Start** button, and then click **All Programs**.
In the nXt Render Farm folder, click **Authorize Farm**.
1. In the edit box, paste or type your Product Key and click **OK**.

##### To start the node
1. Click the **Windows Start** button, and then click **All Programs**.
In the nXt Render Farm folder, click **Render Farmer**.
1. [Right-click](mouse-button-right.html) the tray icon, and on the menu, click **Restore**.
1. On the Help menu, click **About**.
If the version number indicates an Evaluation version, licensing has not been successful.
1. Minimize the Render Farmer window to return it to the tray.
