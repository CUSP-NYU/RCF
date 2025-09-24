# CUSP Research Computing Facility (RCF) Tutorial and Guidance 

### 📌 This guide covers logging into and working in the **RCF**. Visit the **RCF** directly [here](https://serv.cusp.nyu.edu).

### RCF Features and Resources
The CUSP RCF account enables access to:

* JupyterHub applications, home folders, shared project folders, and more
* Secure file transfer via SFTP
* Secure SSH access via a gateway with X11 forwarding capability (CLI or GUI), or via tunneling to a protected multi-user Linux and windows remote desktops
* Multi-user Windows and Linux remote desktop environments, which are fully integrated with their respective systems
* Analytical software such as MATLAB, RStudio, QGIS, Visual Studio Code (VS Code) and others
* Powerful computing resources (1TB of RAM and 500TB + of storage)
* Personal home directories, temporary scratch directories, and project-specific workspaces  
* Ability to request a customized Virtual Machine (VM) or physical server for specific projects, subject to approval
  

### About this Document

This document includes four sections containing information about:

 * [Creating a Login Credential for the RCF Environment](#creating-a-login-credential-for-the-rcf-environment)
 * [Accessing the CUSP RCF Environment](#accessing-the-cusp-rcf-environment)
   * [Secure Shell (ssh)](#secure-shell-ssh)
   * [CUSP RCF Dashboard](#cusp-rcf-dashboard) 
   * [CUSP JupyterHub Portal](#jupyterlab-interface-file-upload)
 * [Data Transfer](#data-transfer)
 * [Project Workspace Request and Structure](#project-workspace-structure)

  
# Creating a Login Credential for the RCF Environment

All users — NYU faculty, students, and researchers as well as capstone sponsors and mentor from external agencies and companies — can request a login credential by filling out this [Google Form](https://forms.gle/QLGxL68UFBgsun9RA).

# Accessing the CUSP RCF Environment
To access the CUSP RCF environment you can choose from one of three options:

 * [Secure Shell (ssh)](#secure-shell-ssh)
 * [CUSP RCF Dashboard](#cusp-rcf-dashboard) 
 * [CUSP JupyterHub Portal](#jupyterlab-interface-file-upload)


### Secure Shell (ssh)

1. Use a command line tool of your choice to directly SSH into the server with your credentials.
  ```
  ssh <YOUR_CUSP_ID>@gw.cusp.nyu.edu
  ```
2. When prompted, enter your password.
  ```
  password: <YOUR_CUSP_ID_PASSWORD>
  ```
3. Next, SSH into the notebook servers. You can access one of three available Ubuntu notebook servers by using SSH. The three servers are named: `notebook`, `notebook2`, and `notebook3`. Each server provides access to your personal home directory. From there, you can navigate to either a collaborative team workspace or continue working in your personal folder. 

   Use **one of the following commands** to connect:

  ```
ssh notebook   # Connect to the first server
ssh notebook2  # Connect to the second server
ssh notebook3  # Connect to the third server
  ```
  

### CUSP RCF Dashboard  

The [CUSP RCF Dashboard](https://datahub.cusp.nyu.edu) is a one-stop shop for all things related to the RCF. Simply log in with your CUSP credentials.

Once logged in, you'll have access to a range of tools, including:
- **Remote Desktops** (Linux & Windows)  
  Use pre-installed software such as:
    - ESRI ArcGIS Desktop (ArcMap)
    - QGIS
    - Microsoft Office
    - MATLAB
    - ... and more.
      
- **Terminals**  
  Access command-line environments

<p align="center">
    <img src="https://github.com/CUSP-NYU/RCF/blob/main/images/dashboard.png" alt="CUSP RCF dashboard" width="300">
</p>

Once you log in with your **CUSP ID and password**, you'll see the Dashboard interface (see image below). 

<p align="center">
    <img src="https://github.com/CUSP-NYU/RCF/blob/main/images/dash_after_login.png" alt="Dashboard Main Session" width="300">
</p>

From there, simply click on one of the available options to:
- Launch a **Remote Desktop Session** (Linux or Windows)
- Open a **Terminal (SSH) Session** on the RCF large servers
  
<p align="center">
    <img src="https://github.com/CUSP-NYU/RCF/blob/main/images/dash_after_login.png" alt="Dashboard Main Session" width="300">
</p>

Below is an image of an **Ubuntu Remote Desktop** accessed through the **RCF Dashboard**.

<p align="center">
    <img src="https://github.com/CUSP-NYU/RCF/blob/main/images/ubuntu_session.png" alt="Dashboard Main Session" width="300">
</p>

From this desktop environment, you can:

- Launch available **Integrated Development Environments (IDE)** 
- Open **SSH sessions** to other RCF servers
- Use **JupyterLab** on different RCF servers

Below is an image of a **Windows Remote Desktop** accessed via the **RCF Dashboard**.
<p align="center">
    <img src="https://github.com/CUSP-NYU/RCF/blob/main/images/windows_session.png" alt="Dashboard Main Session" width="300">
</p>

From this environment, users can:
- Run available **Windows-based IDEs**
- Use **Microsoft software** such as Word, Excel, and PowerPoint  
- Launch **JupyterLab** 
- **Map a network drive** to access your CUSP home folder and shared directories

Below is an image of a **Ubuntu Terminal Session (CLI)** running on a `notebook` large server. You can launch similar sessions on any of the other **RCF large servers**.

<p align="center">
    <img src="https://github.com/CUSP-NYU/RCF/blob/main/images/terminal_session.png" alt="Dashboard Main Session" width="300">
</p>

This command-line interface allows you to:
- Run code 
- Troubleshoot and manage files using Command Line Interface (CLI) tools  


**Note:** You can upload files by simply **dragging and dropping** them from your local desktop into the active browser session. The uploaded file will appear in your **RCF home folder** automatically. 



### CUSP JupyterHub Portal

You can directly access **JupyterLab** via any of the three large servers below. These servers help distribute workloads and provide reliable performance. 

New to JupyterLab? Learn more in this [JupyterLab Tutorial](https://jupyterlab.readthedocs.io/en/latest/).

Choose any of the following links to open in your browser and log in using your **Login credentials**:
- [notebook1](https://notebook.cusp.nyu.edu/) 
- [notebook2](https://jupyterhub.cusp.nyu.edu/) 
- [notebook3](https://data.cusp.nyu.edu/) 


After logging in with your credentials, you can create a new **Jupyter Notebook** or open a **Terminal** by clicking the **"New"** button and selecting the desired option.

Scroll below for instructions on how to create your own **conda environment** and register a **Jupyter kernel** within JupyterLab.

<p align="center">
    <img src="https://github.com/CUSP-NYU/RCF/blob/main/images/JupyterHub-login.png" alt="JupyterHub Login Interface" width="300">
</p>

The image below displays the **JupyterLab** interface.

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
You will be prompted with the following:
```
sftp>
```
In the `sftp` tool, you can view a list of available internal commands by typing:
```
?
```
This will display a list of all the commands you can use within the `sftp` session. 

**Example commands:**
- `ls` — Lists the files in your home folder.
- `put` — Uploads a file from your local computer to the remote server's home folder. From there, you can move or copy it into your project workspace (located at `project-<shortname>`) for further work or share it with your collaborators.

`sftp` is a command-line interface typically used from a macOS or Linux machine. However, you can also use a Graphical User Interface (GUI) of your choice. For example:
- **macOS**: Cyberduck  
- **Windows**: WinSCP

### JupyterLab Interface (File Upload)

You can also upload small files directly through the JupyterLab interface. Use the upload button (represented by an arrow icon) to select and upload files to your desired location within JupyterLab.



### Creating Your Own Conda Virtual Environment and JupyterLab Kernels

While there are system-wide kernels available, we recommend creating your own kernels to have control over the packages and libraries you use. Below is a quick guide to creating your own kernel.

From a terminal window or after SSHing into the notebook server via the gateway mentioned in [Accessing the CUSP RCF Environment](#accessing-the-cusp-rcf-environment), follow these steps:

1. SSH into the gateway server
   ```
   ssh <YOUR_CUSP_ID>@gw.cusp.nyu.edu
   ```

2. After entering your credentials, use one of the following commands to SSH into the internal servers:
  ```
ssh notebook # Connect to the first server
ssh notebook2 # Connect to the second server
ssh notebook3 # Connect to the third server
  ```

3: Create a new conda environment (in this example, named `myenv` with Python version 3.10)
  ```
  conda create -n myenv python=3.10
  conda activate myenv
  ```

4: Install any packages you need. Below are some example package installations:
  ```
  conda install pytorch torchvision torchaudio -c pytorch
  conda install -c huggingface transformers
  conda install -c conda-forge scikit-learn pandas
  ```
5: Install and activate ipykernel by running the following commands:
  ```
  conda install -c conda-forge ipykernel
  python -m ipykernel install --user --name=myenv
  ```

Done! You can now select your newly created kernel when running your notebook.

To deactivate your environment, use:
  ```
  conda deactivate # Deactivate the current environment
  ```
To reactivate it, simply run:
  ```
  conda activate myenv # Reactivate the 'myenv' environment
  ```
To remove an environment: 
  ```
  conda env remove — name myenv # Remove the 'myenv' environment
  ```


# Project Workspace Request and  Structure 

In order to be able to collaborate (sharing date, documents, codes etc..) on a project, Please provide cusp.it@nyu.edu with the following infomation 
Project name  (in the format : project-<projet-name>)
Project members CUSP_IDs if  members don't have CUSP_ID they can request them see above 
Project short description and data size


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
**Note:** The folder structure shown above is just a suggested layout. Teams are free to create and organize their own folder structure as needed.
