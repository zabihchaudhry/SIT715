# SIT715
Hi,
To install Wordpress on container using docker. We will give easy way to that.
First you need make a new space in your organization in your bluemix account and make sure it is empty and in US SOUTH region.

Then you need to install plugins and cf cli exe from any of these batch files based on your OS compatiblity:

you can download one click deploy batch for <a href="https://github.com/zabihchaudhry/SIT715/raw/master/install-batch-x86.zip">32-bit</a> and for <a href="https://github.com/zabihchaudhry/SIT715/raw/master/install-batch-x64.zip">64-bit </a>

This batch will download the cf exe itself and ask you to login to your bluemix account. Once logged in then it will download the IBM Container plugin. Then it will generate the random namespace for your organization which must be unique in the world. After setting it will directly route you to the deploy repo here: https://hub.jazz.net/deploy/index.html?repository=https://github.com/zabihchaudhry/SIT715.git
Just login in and type the name of your app and select region should be US SOUTH and space would be the one you have created new for this project and you are ready to go.

In any case you are unable to run batch file then follow these steps:
download the cf cli from here: https://github.com/cloudfoundry/cli/releases then open the command prompt. write 

cf api https://api.ng.bluemix.net
cf login
cf install-plugin https://static-ice.ng.bluemix.net/ibm-containers-windows_x64.exe -f
cf ic namespace set _here_ “any unique name eg. "sdh_cyega_zcb" which is not used by anyone in the world, and if failed try again”

Then open the browser make sure it not open in the private windows or internet explorer as I had faced problems using these on bluemix.
Open this link: 
https://hub.jazz.net/deploy/index.html?repository=https://github.com/zabihchaudhry/SIT715.git

Then follow the same instructions give above.
This process is slow and you have to have patience as it will take 30 minutes aprox. If you need to open then app which you have installed you need to open the Wordpress container and access the link to the site showing in container details from there. 
In this method you are not allowed to open to app link as that will be stop and has nothing to do with the running WordPress.

When you open the link it will ask you to install the Wordpress without any asking for database or storage settings. just fill up the information and you are ready to go. your website is live now and you can make any changes in that. 
