![ciab-logo](https://user-images.githubusercontent.com/1682855/51850975-ea4e3480-22f0-11e9-9128-d945e1e2a9ab.png?classes=float-left)  

**I am happy to introduce CIAB v3 !**  a major upgrade & refactoring of the CIAB Remote Desktop System.


**CIAB** ("*Cloud-In-A-Box*") v3 Remote Desktop System is a server application that integrates and extends the [Apache Guacamole](https://guacamole.apache.org/) clientless remote desktop gateway on a Ubuntu 18.04 LTS host with LXD containers. 

The CIAB Administrator can also easily deploy a number of web applications (see below) using a GUI tool provided on the Admin's Desktop.

Using **only** a web browser that supports HTML5, users can connect to this web interface and access web applications and the Ubuntu Mate desktop as pre-configured and authorized by the CIAB administrator.


![ ](/home/bmullan/ciab/ciab-desktop/ciab-v5/documentation/line-break.png  "line-break")  


![ ](/home/bmullan/Pictures/ciab images/hand-guac.png  "CIAB Remote Desktop System")  


##CIAB Remote Desktop System 
#####(v5 - Oct 2021)

####by Brian Mullan (bmullan.mail@gmail.com)  

![ ](/home/bmullan/ciab/ciab-desktop/ciab-v5/documentation/line-break.png  "line-break")  

####CIAB - *"Cloud in a Box"*

The file _**"install-ciab.zip**_" includes all of the installation Bash Scripts and associated files required to create an *LXD container based CIAB Remote Desktop System*.  

 CIAB will create 2 LXD containers:  
 
- **ciab-cn1** - which will have an installer's choice of *Desktop Envrionment* installed in it  
- **ciab-guac** - will have Guacamole, Tomcat9, PostgreSQL, and NGINX installed via Docker in *ciab-guac*.   We create the LXD "_**ciab-guac**_" container  
   with an command option to _**"enable**_ container _**"nesting"**_.   This is why we are able to install Docker _"inside"_ the LXD "_**ciab-guac**_"  
   container
   
Once installation is complete you can access both Guacamole & the ciab-cn1 based Desktop using any HTML5 Web Browser.  
   
We configure _Guacamole/NGINX_ etc with a _**"self-signed"**_ certificate to allow support for using HTTPS.   This means the connection **from** a User **to**  
the Remote Desktop is _**encrypted**_.  

![ ](/home/bmullan/ciab/ciab-desktop/ciab-v5/documentation/line-break.png  "line-break")  
  
####Steps to Install CIAB Remote Desktop  

---  
 
1) Copy the _**install-ciab.zip**_ to the (local/remote) (Cloud, VM, server etc) you want to create the CIAB System  
2) Unzip _**install-ciab.zip**_  
3) Execute _**ciab-pre-install.sh**_  
4) Execute  _**install-ciab.sh**_  

*NOTE*:   When _**Step 4**_ completes...  
 
a) _**both**_ of the CIAB LXD containers (**ciab-guac** and **ciab-cn1**) will have been *created*  
b) a _**"working"**_ installation directory **/opt/ciab/**  will have been created in *each* container  
c) additional configuration scripts specific to setting up software _**specific**_ to the function of each LXD container  
-- scripts to install Docker, Guacamole, Tomcat9, PostgreSQL, NGINX in the **ciab-guac** LXD container  
-- scripts to install a Desktop Environment and a User Acct for the person doing the CIAB installation into the _**ciab-cn1**_ container.  
 
![ ](/home/bmullan/ciab/ciab-desktop/ciab-v5/documentation/line-break.png  "line-break")  
  
