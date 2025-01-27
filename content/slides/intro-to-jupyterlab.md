---
title: "Intro to JupyterLab"
subtitle: "QGreenland Researcher Workshop 2023"
index: 10
background-image: "https://live.staticflickr.com/65535/50237921218_962ba3da87_k.jpg"
title-slide-attributes:
  data-notes: |-
    In this workshop, we are going to be using JupyterLab for our hands-on work because
    it provides a convenient and consistent computing environment that eliminates
    distracting challenges caused by differing operating systems.

    We will use JupyterLab in the cloud via a service called "CryoCloud", which everyone
    should already be registered for. If you are not, please use the break time following
    this module to register! Send a message to Matt or Trey on Slack with your GitHub
    username as soon as possible and we will ensure your registration goes through
    quickly.
---

# Note

We are going to demo a number of features around the use of JupyterLab in the
following slides. Please plan to watch as we explain various features before
trying them yourself in an [exercise](/content/exercises/getting-started-with-jupyterlab.html)
after the presentation.


# What is JupyterLab?

👪 JupyterLab is a human-friendly interface to computation resources.

💻 You can do almost anything you can do on your personal computer!

![JupyterLab logo](/_media/jupyterlab_about_logo.png)

:::{.notes}
The JupyterLab logo is a screenshot from JupyterLab's "Help -> About JupyterLab"
pop-up in CryoCloud.
:::


## JupyterHub ![](/_media/jupyterhub_icon.png){width="5%" style="vertical-align:middle"}

CryoCloud: your personal JupyterLab in the cloud

* JupyterHub: <https://hub.cryointhecloud.com>
* Website: <https://book.cryointhecloud.com>

![Cryocloud logo](/_media/cryocloud_logo.png){width="25%"}


::: {.notes}
JupyterHub is a system for creating many JupyterLabs, e.g. for classrooms
:::

## JupyterHub ![](/_media/jupyterhub_icon.png){width="5%" style="vertical-align:middle"}

Log in to CryoCloud JupyterHub with your GitHub username

* Important: select a 4GB server option
* Your JupyterLab workspace is dedicated, _not_ shared!

![Jupyterhub server selection](/_media/jupyterhub_server_selection.png){width="70%"}

:::{.notes}
We encourage users to start with the 4GB RAM option to start. If individuals run
into memory issues working with a dataset during the workshop, trying the 8GB
option is reasonable.

Although each user has their own dedicated workspace and file system, compute
resources are not completely isolated. For example, selecting a 4GB RAM server
size results in a guaranteed allocation of 4GB but if more memory is free on the
node a user may be able to utilize more than 4GB.

* No scheduler like on a supercomputer
    * Your computations will not interfere with anyone else's
:::


# JupyterLab features

![JupyterLab](/_media/jupyterlab.png)

:::{.notes}
Show what the CryoCloud JupyterLab looks like after signing in and selecting a
server.
:::


# 

![JupyterLab - memory/RAM usage](/_media/jupyterlab_memory.png)

:::{.notes}
Highlight where to monitor memory usage. If a dataset is particularly large
and/or an operation on the data is getting stuck, check memory usage.

If individuals run into memory issues working with a dataset during the
workshop, trying the 8GB option is reasonable.
:::


#

![JupyterLab left side panel](/_media/jupyterlab_left_side_panel.png)

:::{.notes}
We will talk about the left side panel first.
:::


## File Browser ![](/_media/jupyterlab_file_browser_icon.png){width="3%" style="vertical-align:middle"}

:::::: {.columns}
::: {.column}
* Drag & drop from your desktop
* Open many types of files and get a useful display
    * CSV will display as table
    * GeoJSON will display on a map
    * Images will open with an image viewer
:::

::: {.column}
![JupyterLab file browser](/_media/jupyterlab_file_browser.png)
:::
::::::

::: {.notes}
Your home directory is dedicated to you. You will not be able to overwrite anyone else's
files, and vice versa. The `shared*` directories are the only common files.

Be _very_ careful when deleting files from `shared-public/`, it's possible to delete
other people's data.

If you need to delete a file in the file browser, select it and press the `Delete` key,
or right-click a file and select "Delete" from the menu.
:::


## Running terminals and kernels ![](/_media/jupyterlab_running_terminals_kernels_icon.png){width="3%" style="vertical-align:middle"}
:::::: {.columns}

::: {.column}
* Lists currently running Terminals and Kernels.

* If one of these apps gets 'stuck', you may need to shut it down and
  try again

* If you accidentally close a terminal or notebook tab, you can re-access it by
  clicking on its entry here.
:::

::: {.column}
![JupyterLab Running Terminals and Kernels](/_media/jupyterlab_running_terminals_kernels.png)
:::

::::::

:::{.notes}
We will not be covering the usage of the final three side panel views.
:::

#

![JupyterLab Launcher](/_media/jupyterlab_launcher.png)

:::{.notes}
Applications can be launched from the Launcher, opening a new tab/window for
that application.

To open a new Launcher, click the `+` tab, `File > New Launcher`, or the Blue
`+` button in the file browser left side panel.
:::


## Terminal ![](/_media/jupyterlab_terminal_icon.png){width=5% style="vertical-align:middle"}

* `conda install <package>`
* `mamba install <package>`
* Common GDAL/OGR utilities: `gdalinfo`, `ogrinfo`, etc.

![JupyterLab terminal](/_media/jupyterlab_terminal.png)

::: {.notes}
Conda and Mamba are already installed, and a `notebook` environment is pre-created. Use
`conda`/`mamba` commands to install Python dependencies into the `notebook` environment.
:::


## Desktop ![](/_media/jupyterlab_desktop_icon.png){width=5% style="vertical-align:middle"}

![Desktop](/_media/jupyterlab_desktop.png)

:::{.notes}
The desktop opens in a new browser tab, not a new tab in JupyterLab.
:::

## Desktop ![](/_media/jupyterlab_desktop_icon.png){width=5% style="vertical-align:middle"}

On first launch, select "Use default config"

![Use default config](/_media/xfce_first_launch.png)


## Desktop: file browser

The "Home" icon on the desktop shows the same files as JupyterLab File Browser.

![Desktop file browser](/_media/jupyterlab_desktop_file_browser.png)

::: {.notes}
There's also a terminal emulator and other utilities often found in a desktop
GUI environment.
:::


## Desktop: QGIS and QGreenland

Can open QGreenland!

![Desktop with QGIS and QGreenland](/_media/jupyterlab_desktop_qgreenland.png)

::: {.notes}
Opening QGreenland should take ~2 minutes.

Do not use the logout function within the desktop, as this may make it difficult to get
back into your desktop.
:::


## Desktop: logging out
::: {.callout-warning}
Do not use "Logout" from the desktop environment!
:::

To close the desktop, please close the window/tab that the desktop environment is open in.

:::{.notes}
_TODO: add an image showing a "no" symbol over the logout menu?_
:::


## Jupyter Notebooks

:::::: {.columns}
::: {.column}
* A tool for [Literate Programming](https://en.wikipedia.org/wiki/Literate_programming)
    * Showing your work
    * Tracking provenance
    * Telling a story

* See also:
    * Quarto
    * JupyterBook
:::

::: {.column}
![Jupyter Notebook](/_media/jupyterlab_notebook.png)
:::
::::::

:::{.notes}
At this point, do a live demo of the `demo.ipynb` notebook.

When demoing the notebook, ensure that we narrate double-clicking markdown cells
to show the source of it. And also how to expand/collapse cells.

Also be sure to demonstrate how to create a new cell, change it's type
(Markdown, Code, ...), and move cells around.

<!-- alex ignore execution -->
Note that execution order matters.

Finally, demo the `sync.sh` script which moves some data to fast local storage
(`qgis-data/`). Before running, do `rm -rf ~/qgis-data/* && rm ~/demo.ipynb`.
This step is important; without it, opening QGreenland could take multiple minutes. The
`qgis-data` directory is where you should store any data if speed matters. E.g. if you
have a 1GB dataset, it'll be very important that it lives in fast storage!

```
/home/jovyan/shared/QGreenland/sync.sh
```
:::


## Shut down your server!

::: {.callout-important}
_At the end of each day, click `File > Hub Control Panel` and then click `Stop My Server`_
:::

:::::: {.columns}
::: {.column width="50%"}
![Control Panel](/_media/jupyterhub_control_panel.png){width=80%}
:::

::: {.column width="50%"}
![Stop My Server](/_media/jupyterhub_stop_my_server.png){width=80%}
:::
::::::

::: {.notes}
Shut down your server at the end of each day to save on cloud costs.

Any files you have created will remain next time you log in!
:::

# Exercise

💪 [Getting started with JupyterLab](/content/exercises/getting-started-with-jupyterlab.html)
