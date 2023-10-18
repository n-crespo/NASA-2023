pvs-on-windows
==============

> NOTE: The reason this is a bit janky is because VSCode has a feature that
> lets you access WSL files while running VSCode as a Windows process, but PVS
> will NOT work if you run VSCode as a windows process. 

> This also may not work if VSCode is already installed on Windows, but I
> haven't had that problem.

1. Install Ubuntu WSL (Windows Subsystem for Linux) 
  - Open a power shell prompt (Windows Key --> type Powershell --> run as administrator)
  - type `wsl --install`
    - you may have to do this first:
      - windows key --> turn windows features on or off --> 
        - enable Windows Subsystem for Linux
        - enable Windows Hypervisor Platform
        - enable Virtual Machine Platform
        - enabling these may prompt a system restart
      - at this point you should be able to use `wsl --status` and make sure it
      says version 2 and Ubuntu
2. Install Ubuntu
  - Open the Windows Store (windows key search again), install "ubuntu"
  - in Powershell, use `wsl --list --online` to make sure ubuntu is installed and working (and using Version 2)
3. In Powershell, type `ubuntu` to open Ubuntu terminal
4. Follow the directions to make a UNIX account, you can leave the password blank (if it lets you) because it really doesn't matter much
5. Use `su {username}` to [s]witch [u]ser
6. use `exit` to exit back to root user
7. In root, `sudo apt update`, `sudo apt full-upgrade`
8. `apt install code` (add `sudo` or switch to root if permission denied)
9. Switch to any user (not root)
10. `code .` opens vscode in the current directory
11. Install PVS Extension, follow directions for installing PVS executables
12. Contact me if this doesn't work


* The only part of this that may not work is that the installation for vscode
using apt may be more complicated than I said above. If the above doesn't work,
here is someone else's instructions for doing the same thing (i forgot their
name)(stolen from Teams group)

  1. Install and enable WSL2. If you've never done this before, you may need to look up a tutorial because you will likely need to change some virtualization options.
  2. Download Debian from the Microsoft Store. You may use another prebuilt distro in the store, or configure your own distro. However, these instructions are written assuming you are using a flavor with the apt package manager.
  3. Run Debian in Windows to start the set up process.
  4. Update the distro and grab the unzip utility with these commands:
  sudo apt update
  sudo apt upgrade
  sudo apt install unzip
  5. To add Microsoft repositories and install vscode, run the following commands in the Debian terminal:
  sudo apt-get install wget gpg
  wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg
  sudo install -D -o root -g root -m 644 packages.microsoft.gpg /etc/apt/keyrings/packages.microsoft.gpg
  sudo sh -c 'echo "deb [arch=amd64,arm64,armhf signed-by=/etc/apt/keyrings/packages.microsoft.gpg] https://packages.microsoft.com/repos/code stable main" > /etc/apt/sources.list.d/vscode.list'
  rm -f packages.microsoft.gpg

  sudo apt install apt-transport-https
  sudo apt update
  sudo apt install code

  6. Once the installation is complete, use the command "code" at the command line.
  !!!! You will get a warning that essentially says that you are doing this wrong, uninstall code for Linux and install code for Windows instead. Ignore this and just enter "Y" you want to continue.

  7. VS Ccode will start. Download the PVS plugin and let it install PVS and nasalib as normal.

# Resources 
[Install Ubuntu on WSL2 on Windows 11](https://ubuntu.com/tutorials/install-ubuntu-on-wsl2-on-windows-11-with-gui-support#1-overview)
