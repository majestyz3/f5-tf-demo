Lab 2 – Getting Started
-----------------------------------

Welcome to the F5 Automation lab using terraform and aAsible! In this course we will:

Explore how to spin up a and spin down a F5 , by using a declarative API model to forward, aggregate and analyze BIG-IP in a cloud enviroment (azure).

During this hands-on lab you will learn the following:
•	The difference between a declarative and imperative API interface. 
•	Implemntation of a CI/CD pipeline to manage your F5.
•	Implemntation of the F5 automation toolchain.
 

~~~~~~~~~~~~~~~~~~~~~~~~~

**Exercise 1 - log into/create github account**


#. Open your web browser
#. Navigate to https://github.com/ (or https://github.com/join if you do not have a account) 
#. sign in/ register an account

    .. image:: ./github-create.png

------------------------------------------------ 

**Exercise 2 - azure subsciption check**

In this course, you must be able to create resources using azure and have a brief understanding of azure terminology. 
To check if you have appropriate permissions:

1.	Check your that you have acess to  your designated azure subscription

#. Log onto portal.azure.com
#. Sign in with your work credentials
#. Click on the icon shown in the image below and make sure you are in your apporiate subscription group

     .. image:: ./sub.png

#. Click resource groups, if you see the image below, please raise your hand as you may not have the appropriate azure. Subscription to complete the remainder of the lab. 

    .. image:: ./resource.png

#. If you are capable of creating resources, and see the below image, continue with lab. (your environment may/may not already have allocated resources)

    .. image:: ./group.png

------------------------------------------------ 

**Exercise 3 - install Visual Studio Code**

The instructions for this lab will be using Visual Studio Code (VScode) as the  source code editor. It Is not required but recommend you use the same for ease of completion.  
If you do not have VScode installed, follow the instructions below. If you already have VScode Installed on your laptop, proceed onto the next Exercise. 

#. Navigate to https://code.visualstudio.com/
#. follow instructions to  install  Vscode

------------------------------------------------ 

**Exercise 4 -  Install  Azure  CLI**


#. Open vs code on your windows/Mac 
#. In the upper right hand corner, click terminal => new terminal (a terminal will appear in the bottom of the screen like so:

     .. image:: ./VScode.png

On mac – (bash)
 #. brew update && brew install azure-cli

On windows – (PowerShell)

 #. paste the code into powershell 
    #. Invoke-WebRequest -Uri https://aka.ms/installazurecliwindows -OutFile .\AzureCLI.msi; Start-Process msiexec.exe -Wait -ArgumentList '/I AzureCLI.msi /quiet'
 #. Log into azure using command “az login” 
 #. The command line will open your defult browser and load an azure sign in page.


 Troubleshooting: 

 Mac: 
There may be a minor version mismatch or other issue during homebrew installation. The CLI doesn't use a Python virtual environment, 
so it relies on finding the installed Python version. A possible fix is to install and relink the python3 dependency from Homebrew.. use. Command 

    #. brew update && brew install python3 && brew upgrade python3
    #. brew link --overwrite python3


For further instructions, feel you can read the complete docs at https://docs.microsoft.com/en-us/cli/azure/install-azure-cli-windows?view=azure-cli-latest

------------------------------------------------ 
