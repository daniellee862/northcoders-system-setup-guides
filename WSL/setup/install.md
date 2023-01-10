# WSL Installation Guide

Windows Subsystem For Linux **(we will be referring to this as WSL)** is a tool which will allow you to run Linux natively of Windows. It allows you to install a Linux distribution as an app and gives you access to important bash commands such as `pwd` and `ls`!

These installation steps can all be found in the [WSL Documentation](https://docs.microsoft.com/en-us/windows/wsl/install).

## Installation Steps

The first step in order to use WSL is to enable the `Windows Subsystem for Linux` setting in your Windows settings. To find this you need to open the start menu and search for "**_Turn Windows features on or off_**". In this list of features you should make sure the `Windows Subsystem for Linux` setting is ticked.

It should look like the image below:

![Image of Windows setting enabling WSL](/WSL/images/windows-setting.png 'Enabling Windows Subsystem for Linux')

Next you will need to run Powershell as an **administrator**, you can do this by searching for **Powershell** in the start menu and then right clicking and selecting "Open as Administrator". Once this is doen you should see a blue terminal window like the one below, you should then enter the command `wsl --install` and wait until it is completed.

**Once this is done you should restart your machine**.

![Image of PowerShell installing WSL](/WSL/images/ps_admin.PNG 'Installing WSL using the PowerShell terminal')



After restarting your machine you should have an **Ubuntu** terminal pop up (if this doesn't happen you can open it from the start menu) that continues the installation after restart. You should see something like this:

![Image of Ubuntu terminal on restart](/WSL/images/ubuntu_install.PNG 'Continuing the installation after restarting your machine')

If all goes well you will be prompted to create a **username** and **password**. This doesn't have to be your Windows login information, and it will become the default user with administrator privileges - allowing you to run `sudo` commands.

**You will need sudo permissions throughout the course so make sure you can remember your password! Or even better use a password manager!**

And that's it, you're ready to go. Please continue to the next step which is [setting up your dev environment](/WSL/setup/setup.md)!

---

## Common Issues

Unfortunately things don't always go to plan and you may instead get an error message with a code such as `0x80070003`. Included below are a list of errors we commonly see and instructions on how to fix them. If you get an error not listed here please use the troubleshooting guidelines found [here](https://docs.microsoft.com/en-us/windows/wsl/troubleshooting#installation-issues) or post in the **precourse** channel on Slack.

| Error Code | Description                                                                   | Link                                                                                                                                                                         |
| ---------- | ----------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 0x800701bc | You need to download the WSL2 Ubuntu kernel update                            | [Help](https://docs.microsoft.com/en-gb/windows/wsl/install-manual#step-4---download-the-linux-kernel-update-package)                                                      |
| 0x80370102 | This error occurs when you do not have virtualisation enabled on your machine | [Help](https://docs.microsoft.com/en-us/windows/wsl/troubleshooting#error-0x80370102-the-virtual-machine-could-not-be-started-because-a-required-feature-is-not-installed) |
| 0x80070003 | Similar to the issue above but night need to go into your computers BIOS      | [Help](https://docs.microsoft.com/en-us/windows/wsl/troubleshooting#installation-issues)                                                                                   |
