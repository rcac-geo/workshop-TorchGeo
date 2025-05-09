---
title: Setup
---

FIXME: Setup instructions live in this document. Please specify the tools and
the data sets the Learner needs to have installed.

## Data Sets

<!--
FIXME: place any data you want learners to use in `episodes/data` and then use
       a relative link ( [data zip file](data/lesson-data.zip) ) to provide a
       link to it, replacing the example.com link.
-->
Download the [data zip file](https://example.com/FIXME) and unzip it to your Desktop

## Software Setup

::::::::::::::::::::::::::::::::::::::: discussion

### Details

Setup for different systems can be presented in dropdown menus via a `spoiler`
tag. They will join to this discussion block, so you can give a general overview
of the software used in this lesson here and fill out the individual operating
systems (and potentially add more, e.g. online setup) in the solutions blocks.

:::::::::::::::::::::::::::::::::::::::::::::::::::

:::::::::::::::: spoiler

### Windows

Use PuTTY

::::::::::::::::::::::::

:::::::::::::::: spoiler

### MacOS

Use Terminal.app

::::::::::::::::::::::::


:::::::::::::::: spoiler

### Linux

```module load conda cuda/12.6.0```

```conda create -p ./geo_env python=3.12```

```conda activate ./geo_env```

```(/home/liu4201/geo_env) liu4201@login03.gautschi:```

```pip3 install torch torchvision torchaudio```
```conda install torchgeo```
```conda list torchgeo```

```# packages in environment at /home/liu4201/conda_env/geo_env:
#
# Name                    Version                   Build  Channel
torchgeo                  0.7.0              pyhd8ed1ab_0    conda-forge
```

```conda install ipykernel```
```ipython kernel install --user --name=geo_env_kernel```

```Installed kernelspec geo_env_kernel in /home/liu4201/.local/share/jupyter/kernels/geo_env_kernel```

::::::::::::::::::::::::

Now Open thinLinc Desktop and open a Terminal
```sinteractive -A rcac -p ai -N1 -n14 --gpus-per-node=1 -t 5:00:00```

```
salloc: Granted job allocation 1119021
salloc: Waiting for resource configuration
salloc: Nodes h000 are ready for job

liu4201@h000.gautschi:[~] $
```

```module load jupyter```
```jupyter notebook```
copy and paste the url to webpage

Open a new Terminal
```ssh h000 -L 8888:localhost:8888```
