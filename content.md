## Preamble
This is a quick walkthrough to setup a local development environment in Windows, for the Code Institute  Diploma in Full Stack Web Development.  This environment is not strictly necessary as all the IDE tools are available online however, it does provide a useful exercise for the more adventurous and a 'plan b' should there be any connectivity issues.

This article will provide the content for my milestone project 1 and is currenly in draft.

For the purpose of the course I have installed a clean build of the latest version of Windows10.  This is not strictly necessary but does remove the clutter of previous installations and a task I perform regularly anyway.  I won't go into detail about the installation as it is well documented in Google.

After installing all the latest updates I put the minimum software on that use regularly.  I use Chocolately to manage this as it is a great package manger for windows and all installations can be done from a few command lines:

## Prerequistes
Your GitHub repository url with CI Template provisioned from https://github.com/Code-Institute-Org/gitpod-full-template 
Windows Subsystem for Linux - WSL2 is the latest and improved version.
VSCode - plus Remote, Docker and git extensions

Install WSL
If you running Windows 10 version 2004 and higher (Build 19041 and higher) or Windows 11, installation is much simpler.  I'm using Windows 10 Home 22H2 19045.2728 at time of writing.  More information can be found at https://learn.microsoft.com/en-us/windows/wsl/install if these instructions don't work for you.

Open Powershell as Administrator and enter the following:

>wsl --install

Accept and allow any prompts.  When complete, restart Windows to download and configure further updates.

When Windows reboots, Ubuntu should continue to install in a Terminal window. This may take a few minutes but, when complete you'll you'll be asked to enter a new UNIX username.  This will be specifically for Ubuntu and not related to your Windows login.  I entered neil and created a new password when prompted.

You are now in a Bash terminal in a Linux Ubuntu virtual environment (black window).  Leave this window open and open another Powershell window as Administrator and check your wsl installation.  Type the following in Powershell >:

>wsl -l -v
  NAME      STATE           VERSION
* Ubuntu    Running         2

Version 2 confirms wsl2 is installed

Now install VSCode
In Powershell as Admistrator type >:

>choco install vscode -y

Open VSCode 

press ctrl shift and p 

Look for the Remote: Development Extensions pack and select it the install from the left hand panel:

(wsl should already have installed)
Dev Containers - install
Remote ssh - install
Github Codespaces - install

Press ctrl shift and p again and look for Dev containers: clone repository in named container volume and accept all defaults: got it and install 

Allow Docker Desktop to install.

Finally Close and log out of Windows to complete the installation.

Log back in to Windows and allow install to continue, accept Docker terms and conditions and wait for it to load up.  Skip the next details or, fill in the form if you prefer.  Wait until the Docker engine starts.  Be patient, this can take a while.


