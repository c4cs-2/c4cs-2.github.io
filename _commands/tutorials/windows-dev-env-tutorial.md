---
---
**"Linux" Development Environment on Windows**
-------

This tutorial walks through how to make Windows work like linux, covering two ways to set up an environment that can use common Linux commands, that has a package installer, and that can use sudo to run elevated commands. Specifically, it covers setting up the Linux Subsystem for Windows 10 and installing Cygwin for other versions of Windows.

## Introduction
This tutorial is for people who want to set up a development environment on Windows where they can use common Linux commands (such as sed, awk, and grep) and other Linux-first tools (such as Ruby, Python, etc.) alongside Windows applications and without running a Virtual Machine with Linux installed, which may require more resources in terms of memory and CPU. 

The main topics covered are the Linux Subsystem for Windows 10, including how to install the update that enables it, how to activate the subsystem, and how to access Windows files from within the subsystem, and vice versa, and Cygwin, including how to install it, how to add new packages, how to run commands as sudo, and how to install the Chocolatey package manager. 


## Linux Subsystem for Windows
The Windows Subsystem for Linux (WSL) is a Windows 10 feature that enables you to run native Linux command-line tools directly on Windows. Unfortunately, there is not a version that is compatible with older versions of Windows. For those using other Windows versions, please skip to the section on Cygwin below.
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

