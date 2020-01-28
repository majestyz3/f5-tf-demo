Lab 3 – Continued Preperation of lab Environment
-----------------------------------

In this lab you will clone the repository from github and install  cheff inspec.

------------------------------------------------ 

**Exercise 1 - fork & clone repo **

**NOTE:** if you have never used GitHub before, you will have to generate a new ssh key pair, the instuctions to do so can be found here  https://help.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent


#. Naviage to repo using link: https://github.com/mjmenger/terraform-azure-bigip-setup
#. Fork the repo using the fork button displayed below. 

    .. image:: ./fork.png


GitHub should create a copy of the repository in your git. Now you’re ready to clone the repository to your own machine. As seen below, click the green clone button, and copy the web URL. 


     .. image:: ./clone.png


    #. Open VScode
    #. In the upper right, click on terminal  => new terminal (or you can use existing one if you already have it up from previous steps) 
    #. Navigate to a directory on your local machine where you wish to save the repository’s content.
    #. Use command: 
        #. Git clone (PASTE WEB URL HERE) 

------------------------------------------------ 

**Exercise 2 - Check Application Services 3 Extension (AS3) RPM Availability**
  
#. Open Postman 

#. Open the the Postman collection `RPMs`

    .. image:: ./as3post.jpg

#. Click the `Get AS3 RPM Package` request 

#. Examine the request. Note that we are sending a 'GET' request with an empty body. Send the GET request by clicking the blue 'Send' button.

    .. image:: ./send1.jpg

#. You should see a similar response. 

    .. image:: ./as3rpm.jpg

**NOTE:** By sending this GET request to 'https://10.1.1.9/mgmt/shared/appsvcs/info' with the correct credentials, the response shows details of the AS3 API available on this BIG-IP. 

**NOTE:** This AS3 RPM package was pre-installed. For instructions, visit the link here: https://clouddocs.f5.com/products/extensions/f5-appsvcs-extension/latest/userguide/installation.html 


------------------------------------------------ 

**Exercise 3 - Check Telemetry Streaming RPM Availability**
  
#. Open the the Postman collection `RPMs`

#. Click the `Get TS RPM Package` request 

#. Examine the request. Note that we are sending a 'GET' request with an empty body. Send the GET request by clicking the blue 'Send' button. 

    .. image:: ./sendts.jpg

#. You should see a similar response. 

    .. image:: ./tsrpm.jpg

**NOTE:** By sending this GET request to 'https://10.1.1.4/mgmt/shared/telemetry/info' with the correct credentials, the response shows details of the TS API available on this BIG-IP. 

**NOTE:** This Telemetry Streaming RPM package was pre-installed. For instructions, visit the link here: https://clouddocs.f5.com/products/extensions/f5-appsvcs-extension/latest/userguide/installation.html 

------------------------------------------------ 
