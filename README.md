# CUSP Research Computing Facility (RCF)

CUSP RCF is a shared resource for CUSP researchers, faculty, and students; NYC agencies; and citizens interested in using data in a secure environment for urban research and policy. It is a Safe Data Environment providing a suite of powerful tools and services so researchers can collaboratively work in a seamless and reproducible manner, while at the same time protecting data privacy. 

Researchers have full control of their data and workspace. As data providers, they are responsible for the privacy and confidentiality of their data. They are required, however, to follow the data policies baseline recommended and required by [NYU Policy on Responsible Use of NYU Computers and Data](https://www.nyu.edu/about/policies-guidelines-compliance/policies-and-guidelines/responsible-use-of-nyu-computers-and-data-policy-on.html).

CUSP RCF is a perfect environment to host student assignments, group projects, and capstone projects for the reasons mentioned above. Each capstone group will share a project workspace and run code against the project data using all of the available tools and platforms.

### RCF Features and Resources
The CUSP RCF account enable access to resources including:

* JupyterHub application, home folders, shared project folders, and more
* Secure file transfer via SFTP
* Secure SSH access via a gateway with X11 forwarding capability (CLI or GUI), or via tunneling to a protected multi-user Linux remote desktop
* Multi-user Windows remote desktop environments, which are fully integrated with their respective systems
* Backup and restore capabilities with an enterprise-class backup system (IBM Spectrum Protector)
* Analytical software such as MATLAB, RStudio, QGIS, and others
* Powerful computing resources (1TB of RAM and 500TB of storage)
* Personal home directories, temporary scratch directories, and project-specific workspaces  
* Ability to request a customize VMs for specific projects (subject to approval) 


### About this document

This document includes four sections containing information about:

 * [Creating a Login Credential for the RCF Environment](#creating-a-login-credential-for-the-rcf-environment)
   * [Students](https://github.com/CUSP-NYU/RCF#students)
   * [Capstone Sponsors and Team Leaders](https://github.com/CUSP-NYU/RCF#capstone-sponsors-and-team-leaders)
 * [Accessing the CUSP RCF Environment](https://github.com/CUSP-NYU/RCF#accessing-the-cusp-rcf-environment)
   * [SSH](#ssh)
   * [CUSP RCF Portal](https://github.com/CUSP-NYU/RCF#cusp-rcf-portal) ***(currently inaccessible due to an upgrade)***
   * [JupyterHub](https://github.com/CUSP-NYU/RCF#jupyterhub)
 * [Data Transfer](https://github.com/CUSP-NYU/RCF#data-transfer)
 * [Project Workspace Structure](https://github.com/CUSP-NYU/RCF#project-workspace-structure)
  

  
  
# Creating a Login Credential for the RCF Environment

CUSP students should register using a CUSP ID, which is the same as their [NYU NetID](https://www.nyu.edu/life/information-technology/accounts-and-access/identity-and-accounts/netid-and-password.html). Please note that the CUSP ID password is different from NYU NetID password.

### Students 
To register for a CUSP account, please provide the following information to cusp.it@nyu.edu:

* Full name 
* Email address
* NYU NetID
* CUSP sponsor

### Capstone Sponsors and Team Leaders
To register for a CUSP account, please provide the following information to cusp.it@nyu.edu:

* Full name 
* Email address
* NYU NetID or preferred username if you do not have a NYU NetID
* Project lead
* Names of all collaborators on the given project
* Project name 
* Data size (current and anticipated increases if applicable) 

  
# Accessing the CUSP RCF Environment

To access the CUSP RCF environment you can choose from one of three options:

 * [SSH](https://github.com/CUSP-NYU/RCF#ssh)
 * [CUSP RCF Portal](https://github.com/CUSP-NYU/RCF#cusp-rcf-portal) ***(currently inaccessible due to an upgrade)***
 * [CUSP JupyterHub Portal](https://github.com/CUSP-NYU/RCF#cusp-jupyterhub-portal)


### SSH

1. Use a command line tool of your choice to directly SSH into the server with your credentials.
  ```
  ssh <YOUR_CUSP_ID>@gw.cusp.nyu.edu
  ```
2. When prompted, enter your password.
  ```
  password: <YOUR_CUSP_ID_PASSWORD>
  ```
3. Next, SSH into the notebook server. Please note that 'notebook' is the name of the large Ubuntu server mentioned above. This brings you to your personal home directory.
  ```
  ssh notebook   
  ```


### CUSP RCF Portal (currently inaccessible due to an upgrade)

The [CUSP RCF Portal](https://serv.cusp.nyu.edu/dash_beta/#/) is a one-stop shop for all things related to the RCF. Simply log in with your CUSP credentials. 

From there, you can access all the tools available to you, including terminals and remote desktops (Linux and Windows). On the remote desktops, you can use software like ESRI ArcMap, QGIS, MS Office, MATLAB, and more.

<p align="center">
    <img src="https://github.com/CUSP-NYU/RCF/blob/main/images/CUSP-RCF-Portal.png" alt="CUSP RCF Portal" width="300">
</p>

### CUSP JupyterHub Portal

Directly access the CUSP JupyterHub portal by navigating to [this link](https://notebook.cusp.nyu.edu/) in your browser. Make sure you are on the NYU network or connected via the [NYU Virtual Private Network (VPN)](https://www.nyu.edu/life/information-technology/infrastructure/network-services/vpn.html), and then log in with your credentials.

<p align="center">
    <img src="https://github.com/CUSP-NYU/RCF/blob/main/images/JupyterHub-login.png" alt="JupyterHub Login Interface" width="300">
</p>

The image above shows the classic view of the JupyterHub interface. You may also encounter the JupyterLab interface.

<p align="center">
    <img src="https://github.com/CUSP-NYU/RCF/blob/main/images/JupyterLab-interface.png" alt="JupyterLab Interface" width="500">
</p>


# Data Transfer

There are two ways to transfer data, code, and documentation to the RCF large server for analysis and data sharing:
 * [Command Line Secure File Transfer](https://github.com/CUSP-NYU/RCF#command-line-secure-file-transfer)
 * [JupyterLab interface](https://github.com/CUSP-NYU/RCF#jupyterlab-interface)

### Command Line Secure File Transfer

To transfer large files, you can use the staging server with any secure transfer software. For example, using CLI (Command Line Interface) tools like sftp (Secure File Transfer Protocol).

```
sftp  <YOUR_CUSP_ID>@staging.cusp.nyu.edu
```
The data will be transferred to your home folder. From there, you can move or copy it into your project workspace for further work or share it with your collaborators.

### JupyterLab interface

You can also upload small files directly through the JupyterLab interface. Use the upload button (represented by an arrow icon) to select and upload files to your desired location within JupyterLab.

You can create a new Jupyter Notebook or open a terminal by clicking the "New" button and selecting the desired option.

While there are system-wide kernels available, we recommend creating your own kernels to have control over the packages and libraries you use. Below is a quick guide to creating your own kernel.

From a terminal window or after SSHing into the notebook server via the gateway mentioned in [Accessing the CUSP RCF Environment](https://github.com/CUSP-NYU/RCF#accessing-the-cusp-rcf-environment), follow these steps:

1. SSH into the gateway server
    ```
    ssh <YOUR_CUSP_ID>@gw.cusp.nyu.edu
    ```

3. After entering your credentials, SSH into the internal server "notebook":
    ```
    ssh notebook
    ```

4. After you are logged into the "notebook" server, create and register your Conda environment in JupyterHub by initializing Conda (required) to set up Conda for your user:
    ```
    conda init
    ```

5. Create a specific Conda environment named MyP3.10 with Python 3.10:
    ```
    conda create --name MyP3.10 python=3.10
    ```

6. Activate your new environment:
    ```
    source activate MyP3.10
    ```

7. Install Jupyter and ipykernel to register the environment with JupyterHub:
    ```
    pip install jupyter
    ```

8. Add the environment to JupyterHub:
    ```
    ipython kernel install --name "MyP3.10" --user
    ```
    
9. Verify if the kernel is present by logging into the [CUSP JupyterHub portal](https://notebook.cusp.nyu.edu).

10. To add packages to your environment, ensure it is activated and use pip or conda to install the desired packages:

    ```
    source activate MyP3.10
    pip install <package_name>
    # or
    conda install <package_name>
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
├── datamarts/
├── export/
└── workspace/
    ├── <YOUR_CUSP_ID>/        # Individual team member's folders for working, testing, and experimenting. Others do not have access.
    ├── share/                 # Shared folder storing data, working scripts, documentation, and official project outputs.
    │   ├── data/              # Raw data; DO NOT MODIFY or REMOVE files.
    │   │   └── CUSP/
    │   ├── documentation/     # Documents, articles, technical documentation, etc.
    │   │   └── articles/
    │   ├── figures/           # Figures for presentations, publishing, etc.
    │   ├── output/            # Processed data for analysis.
    │   └── scripts/           # Working scripts intended to be shared with the team.
```
