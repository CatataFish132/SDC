# Development Container Setup Guide

This document provides step-by-step instructions on setting up a development environment using Docker containers in Visual Studio Code (VS Code). 

## Prerequisites

Before you begin, ensure you have the following:

- **Visual Studio Code**: Download and install VS Code from [here](https://code.visualstudio.com/).
- **Docker**: Install Docker Desktop for Windows or use your Linux distribution's package manager to install Docker.
  - For Windows users: Follow additional steps to set up WSL (Windows Subsystem for Linux) if using a non-Windows-based container.

## Installation Steps

### Step 1: Install VS Code and Extensions

1. **Install Visual Studio Code**: If you haven't already, download and install it from the [official site](https://code.visualstudio.com/).

2. **Install Dev Containers Extension**:
   - Open VS Code.
   - Go to the Extensions view by clicking on the Extensions icon in the Activity Bar on the side of the window or pressing `Ctrl+Shift+X`.
   - Search for "Dev Containers" and install it.

### Step 2: Clone the Repository

1. **Clone the repository** containing your project:
```sh
git clone https://github.com/CatataFish132/SDC.git
```
2. **Open VS Code**, then open the cloned repository folder by selecting File > Open Folder.
     

### Step 3: Setup Docker and WSL (Windows Only) 

1. **Install Docker** : Download and install from Docker Desktop.

2. **Enable WSL** : 
Open PowerShell as Administrator and run:
```sh
wsl --install
```
        
        
Restart your machine if prompted.
         
### Step 4: Configure GUI for Windows 

1. **Install XLaunch** : Download from [XLaunch](https://sourceforge.net/projects/xming/files/Xming/6.9.0.31/Xming-6-9-0-31-setup.exe/download)

2. **Configure Display** : Set the display number to 0.
        

### Step 5: Build the Dev Container 

In VS Code, open the Command Palette (Ctrl+Shift+P).\
Type and select >Dev containers: reopen in container
     

### Step 6: Additional Docker Setup for Linux 

1. **Install Docker** :
```sh
sudo apt update
sudo apt install docker.io
```
 
2. **Allow Localhost Access** :

Run the following command to allow local connections:
```sh
xhost local:root
```