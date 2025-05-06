# CUSP Research Computing Facility (RCF) Tutorial and Guidance 

### RCF Features and Resources
The CUSP RCF account enables access to resources including:

* JupyterHub applications, home folders, shared project folders, and more
* Secure file transfer via SFTP
* Secure SSH access via a gateway with X11 forwarding capability (CLI or GUI), or via tunneling to a protected multi-user Linux and windows remote desktops
* Multi-user Windows and Linux remote desktop environments, which are fully integrated with their respective systems
* Analytical software such as MATLAB, RStudio, QGIS, Visual Studio Code (vscode) and others
* Powerful computing resources (1TB of RAM and 500TB + of storage)
* Personal home directories, temporary scratch directories, and project-specific workspaces  
* Ability to request a customized Virtual Machine (VM) or physical for specific projects (subject to approval)

  [Go Back to CUSP RCF Welcome page](https://serv.cusp.nyu.edu)


### About this document

This document includes four sections containing information about:

 * [Creating a Login Credential for the RCF Environment](#creating-a-login-credential-for-the-rcf-environment)
 * [Accessing the CUSP RCF Environment](#accessing-the-cusp-rcf-environment)
   * [Secure Shell (ssh)](#ssh)
   * [CUSP RCF Dashboard](#cusp-rcf-portal) 
   * [CUSP JupyterHub Portal](#cusp-jupyterhub-portal)
 * [Data Transfer](#data-transfer)
 * [Project Workspace Structure](#project-workspace-structure)
  

  
  
# Creating a Login Credential for the RCF Environment

All users — NYU faculty, students, and researchers as well as capstone sponsors and mentor from external agencies and companies — can request a login credential by filling out this [Google Form](https://forms.gle/QLGxL68UFBgsun9RA).
# Accessing the CUSP RCF Environment
To access the CUSP RCF environment you can choose from one of three options:

 * [Secure Shell (ssh)](#ssh)
 * [CUSP RCF Dashboard](#cusp-rcf-portal) 
 * [CUSP JupyterHub Portal](#cusp-jupyterhub-portal)


### Secure Shell (ssh)

1. Use a command line tool of your choice to directly SSH into the server with your credentials.
  ```
  ssh <YOUR_CUSP_ID>@gw.cusp.nyu.edu
  ```
2. When prompted, enter your password.
  ```
  password: <YOUR_CUSP_ID_PASSWORD>
  ```
3. Next, SSH into the notebook servers. Please note that 'notebook , notebook2, notebook3 ' are the names of the large Ubuntu servers mentioned above. This brings you to your personal home directory, from there you can navigate to you shared team project workspace or work on you home folder 
  ```
  ssh notebook
or
 ssh notebook2 (if you desire to work on the second node)
or
 ssh notebook3 (if you desire to work on the third node)
  ```
  

### CUSP RCF Dashboard  

The [CUSP RCF Dashboard](https://datahub.cusp.nyu.edu) is a one-stop shop for all things related to the RCF. Simply log in with your CUSP credentials.

From there, you can access all tools available to you, including terminals and remote desktops (Linux and Windows). On the remote desktops, you can use software GUI like ESRI ArcMap, QGIS, MS Office, MATLAB, and more.

<p align="center">
    <img src="https://github.com/CUSP-NYU/RCF/blob/main/images/dashboard.png" alt="CUSP RCF dashboard" width="300">
</p>
Please see the pic below after you login with CUSP ID and Password,  user can click on a selection to access remote desktop sessions or Terminal secure sessions on RCF large servers  
<p align="center">
    <img src="https://github.com/CUSP-NYU/RCF/blob/main/images/dash_after_login.png" alt="Dashboard Main Session" width="300">
</p>
Below is a pic showing a Ubuntu remote desktop within CUSP RCF dashboard from there you can launch available IDE GUIs (applications), ssh sessions, and jupyterlabs on different RCF servers 
<p align="center">
    <img src="https://github.com/CUSP-NYU/RCF/blob/main/images/ubuntu_session.png" alt="Dashboard Main Session" width="300">
</p>
Below is a pic showing  a Windows remote desktop within CUSP RCF dashboard from there user can run available windows IDE GUIs, Microsoft softwares and jupyterlabs as well as  MAP a Network drive (CUSP homefolder) etc..
<p align="center">
    <img src="https://github.com/CUSP-NYU/RCF/blob/main/images/windows_session.png" alt="Dashboard Main Session" width="300">
</p>

### CUSP JupyterHub Portal

Directly access the CUSP JupyterHub portals , RCF has three large servers with the jupyterlab application installed on them in order to balance the work load, you can access either of them  following the links below:
to learn about Jupyterlab Applciation go to this [tutorial](https://jupyterlab.readthedocs.io/en/latest/)

[notebook1](https://notebook.cusp.nyu.edu/) in your browser. , and then log in with your credentials.

[notebook2](https://jupyterhub.cusp.nyu.edu/) in your browser. , and then log in with your credentials.

[notebook3](https://data.cusp.nyu.edu/) in your browser. , and then log in with your credentials.


After authenticating with your CUSP credentials, You can create a new Jupyter Notebook or open a terminal by clicking the "New" button and selecting the desired option.
Please check below intructions on how to create your own conda environement and register a jupyter kernel  with Jupyterlab.

<p align="center">
    <img src="https://github.com/CUSP-NYU/RCF/blob/main/images/JupyterHub-login.png" alt="JupyterHub Login Interface" width="300">
</p>

The image above shows the JupyterLab interface.

<p align="center">
    <img src="https://github.com/CUSP-NYU/RCF/blob/main/images/JupyterLab-interface.png" alt="JupyterLab Interface" width="500">
</p>


# Data Transfer

There are two ways to transfer data, code, and documentation to the RCF large server for analysis and data sharing:
 * [Command Line Secure File Transfer](#command-line-secure-file-transfer)
 * [JupyterLab interface](#jupyterlab-interface)

### Command Line Secure File Transfer

To transfer large files, you can use the staging server with any secure transfer software. For example, using CLI (Command Line Interface) tools like sftp (Secure File Transfer Protocol).

```
sftp  <YOUR_CUSP_ID>@staging.cusp.nyu.edu
```
you will be prompted with the following
```
sftp>
```
To learn about what available internal command to sftp tool  you can type 
```
?
```
(Example : ls ( to list the file in you homefolder) , put (to put file from you current computer into the remote computer in your home folder)

The data will be transferred to your home folder. From there, you can move or copy it into your project workspace (the project workspace location is based on the project shortname in the form project-<shortname>) for further work or share it with your collaborators.

sftp is a command line interface from a MAC or linux machine , you can also use any GUI of your choice for example  : MacOS (cyberduck) and for Windows (winscp) 

### JupyterLab Interface (file upload)

You can also upload small files directly through the JupyterLab interface. Use the upload button (represented by an arrow icon) to select and upload files to your desired location within JupyterLab.



### creation of your own conda vitual environement and Jupyterlab Kernels  

While there are system-wide kernels available, we recommend creating your own kernels to have control over the packages and libraries you use. Below is a quick guide to creating your own kernel.

From a terminal window or after SSHing into the notebook server via the gateway mentioned in [Accessing the CUSP RCF Environment](#accessing-the-cusp-rcf-environment), follow these steps:

A. SSH into the gateway server
   ```
   ssh <YOUR_CUSP_ID>@gw.cusp.nyu.edu
   ```

B. After entering your credentials, SSH into the internal servers 
  ```
  ssh notebook   or ssh notebook2  or notebook3
  ```

Step 1: Create a new conda environment (the example used below is named myenv and the python version is 3.10 )
  ```
  conda create -n myenv python=3.10
  conda activate myenv
  ```

Step 2: Install any packages you need, e.g., the packages below are examples.
  ```
  conda install pytorch torchvision torchaudio -c pytorch
  conda install -c huggingface transformers
  conda install -c conda-forge scikit-learn pandas
  ```
Step 3: Install and activate ipykernel 
  ```
  conda install -c conda-forge ipykernel
  python -m ipykernel install --user --name=myenv
  ```

Done! You can now select your new kernel when running your notebook.

Run conda deactivate to deactivate your environment and conda activate myenv to bring it back up.

To remove an environment: 
  ```
  conda env remove — name myenv
  ```


# Project Workspace Structure 

**project-cusp2024** is used as an example in the Green environment. The structure of the workspace is similar in the Yellow environment but with several layers of security, including a dedicated secure network and secure storage.

The workspace dedicated to **project-cusp2024** is set up within the Restricted Green environment. It provides all functionalities and security features of the Green environment but can only be accessed by registered users affiliated with the research project.

The root directory to the project workspace is:
```
/green-projects/project-2024/
```

The structure of the workspace folder is as follows:
```
./
├── datamarts/                 # Read only data : provided by the project data owner, The data owner can upload data in this location with the help of cusp.it@nyu.edu. team can read and use this data
├── export/                    # Read only exportable if needed (request to be sent to cusp.it@nyu.edu)
└── workspace/
    |   ├── share/             # Shared folder storing data, working scripts, documentation, and official project outputs.
    │   ├── data/              # Shareable data
    │   │   └── CUSP/          # Data Related to CUSP projects
    │   ├── documentation/     # Documents, articles, technical documentation, etc.
    │   │   └── articles/
    │   ├── figures/           # Figures for presentations, publishing, etc.
    │   ├── output/            # Processed data for analysis.
    │   └── scripts/           # Working scripts intended to be shared with the team.
```
Note : The tree structure above show a share folder with a subfolders, it is only a suggestion , Team can create their own structure 
