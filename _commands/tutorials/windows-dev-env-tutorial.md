---
---
**"Linux" Development Environment on Windows**
-------

This tutorial walks through how to make Windows work like linux, covering two ways to set up an environment that can use common Linux commands, that has a package installer, and that can use sudo to run elevated commands. Specifically, it covers setting up the Linux Subsystem for Windows 10 and installing Cygwin for other versions of Windows.

## Introduction
This tutorial is for people who want to set up a development environment on Windows where they can use common Linux commands (such as sed, awk, and grep) and other Linux-first tools (such as Ruby, Python, etc.) alongside Windows applications and without running a Virtual Machine with Linux installed, which may require more resources in terms of memory and CPU. 

The main topics covered are the Windows Subsystem for Linux, including how to install the update that enables it, how to activate the subsystem, and how to access Windows files from within the subsystem, and vice versa, and Cygwin, including how to install it, how to add new packages, how to run commands as sudo, and how to install the Chocolatey package manager. 


## Windows Subsystem for Linux
The Windows Subsystem for Linux (WSL) is a Windows 10 feature that enables you to run native Linux command line tools directly on Windows. The WSL sources your Windows path, so you can still run any Windows executable from the WSL command line. Unfortunately, there is not a version that is compatible with older versions of Windows. For those using other Windows versions, please skip to the section on Cygwin below.

**Setup**
- Step 1: install the Windows 10 Creator's Update
  - If you're automatically installing updates, you should already have this!
  - If not, go to Start > Settings > Update & Security > Check for Updates to download and install it
- Step 2: Activate Developer Mode
  - Start > Settings > Update & Security > For Developers
  - "For Developers" is an option on the bar on the left. Within that menu, select "Developer Mode" and accept the warning that pops up.
  - This may take a few minutes to activate. 
- Step 3: Activate WSL
  - Settings > Apps & Features > Turn Windows Features On or Off
  - Scroll to Windows Subsystem for Linux and enable it
  - It will prompt you to reboot. This will be the slowest step because Windows is basically installing Linux directly.
  
**Using bash**
- You should now be able to open bash directly from the command line. Note that if you have a different bash emulator installed (such as Git Bash) you do not want to be using that. WSL should have installed bash.exe into /usr/bin/bash. 
- If you're correctly using bash in the WSL, running pwd should output
  > /mnt/c/Windows/System32
- In general you don't want to (and may not have permission to) modify files in this directory, but running cd will take you to a home directory where you have full access.
- From there, you now have access to all the linux commands you know and love, including apt-get and sudo. 

**Moving files onto and off of the WSL**
- From within the WSL, you can access your Windows-based disks in the directory /mnt
  - /mnt will contain all disks on your hard drive. Most commonly, you will be looking in /mnt/c/Users/yourname
  - you can access this directory within the WSL as freely as you would any other directory, meaning you can use commands such as mv and cp to move files from one place to the next.
- Modifying Linux files with Windows tools is **not supported**
  - but you can do it anyway if you like to live dangerously. 
  - From a shell on Windows, you can find your WSL files at %userprofile%/AppData/Local/Packages
  - From there, the directory to enter depends on which Linux distribution you use. For ubuntu, the directory is CanonicalGroupLimited.UbuntuonWindows_79rhkp1fndgsc
  
## Cygwin
Cygwin is a Linux-style terminal for Windows. It's a good alternative to the Windows Subsystem for Linux for those who are not running Windows 10. It's main feature is the built-in package installer that functions as an a replacement for apt-get and other command line package installers.
