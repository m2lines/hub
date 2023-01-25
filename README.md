# M2LInES JupyterHub

Our team has a cloud-based [JupyterHub](https://jupyter.org/hub) which is open for use by all team members.

|  |  |
|--|--|
| **Hub Address** | https://m2lines.2i2c.cloud/ |
| **Hub Location** | [Google Cloud `us-central1`](https://cloud.google.com/compute/docs/regions-zones) | 
| **Hub Operator**| [2i2c](https://2i2c.org/) |
| **Hub Configuration** | https://github.com/2i2c-org/infrastructure/tree/master/config/clusters/m2lines |

## Getting Help

For questions about how to use the Hub, please open an issue in this repo:

- https://github.com/m2lines/hub/issues

Ryan will respond to your issue and decide whether to refer it to 2i2c for technical support.

## Hub Usage

This is a rough and ready guide to using the Hub.
This documentation will be expanded as we learn and evolve.
Feel free to [edit it yourself](https://github.com/m2lines/hub/edit/main/README.md) if you have suggetions for improvement!

### Logging In

1. 👀 Navigate to https://m2lines.2i2c.cloud/ and click the big orange button that says "Log in to continue"
2. 🔐 You will be prompted to authorize a GitHub application. Say "yes" to everything.
   Note you must belong to the [m2lines](https://github.com/orgs/m2lines/people) GitHub organization
   in order to access the hub. (Johanna can add you.)
3. 📠 You will redirect to a screen with the following options. Choose which machine type you want to use.
 
   <img width="410" alt="image" src="https://user-images.githubusercontent.com/1197350/167696045-d3c660c2-94d9-4a32-a8ad-61f340101ad5.png">
   
   You should try to use the smallest image you need.
   The GPU images should be used only when needed to accelerate model training.
4. 🕥 Wait for your server to start up. It's normal for this to take a few minutes.

### Using JupyterLab

After your server fires up, you will be dropped into a JupyterLab environment.

If you are new to JupyterLab, you might want to peruse the [user guide](https://jupyterlab.readthedocs.io/en/stable/user/interface.html).

### Shutting Down Your Server

Your server will shut down automatically after a period of inactivity. 
However, if you know you are done working, it's best to shut it down directly.
To shut it down, go to https://m2lines.2i2c.cloud/hub/home and click the big red button that says "Stop My Server"

<img width="800" alt="image" src="https://user-images.githubusercontent.com/1197350/167768526-7742a260-d353-4bdb-b9d0-36e9cc17aba1.png">

You can also navigate to this page from JupyterLab by clicking the `File` menu and going to `Hub Control Panel`.

### The Python Environment

The Hub environment contains a full-featured, up-to-date Python environment.
The environments are maintained by Pangeo. You can read all about them at the following URL:

- https://github.com/pangeo-data/pangeo-docker-images/

These are Docker images which you can also run on your own computer.
The Hub contains a specific version of the image which can be found [here](https://github.com/2i2c-org/infrastructure/blob/master/config/clusters/m2lines/common.values.yaml).
For example, at the time of writing, the version of `pangeo-notebook` is `2022.05.10`.
A complete list of all packages installed in this environment is located at:

- https://github.com/pangeo-data/pangeo-docker-images/blob/2022.05.10/pangeo-notebook/packages.txt

There are separate images for pytorch and tensorflow.

You can install additional packages using `pip` and `conda`.
However, these will disappear when your server shuts down.

### Files and Data

Data and files work differently in the cloud.
To help onboard you to this new way of working, we have written a guide to Files and Data in the Cloud:

- https://docs.2i2c.org/en/latest/data/index.html

We recommend you read this thoroughly, especially the part about Git and GitHub.

### Dask

To help you scale up calculations using a cluster, the Hub is configured with Dask Gateway.
For a quick guide on how to start a Dask Cluster, consult this page from the Pangeo docs:

- https://pangeo.io/cloud.html#dask

[More info to be added soon]





