![ciab-logo](https://user-images.githubusercontent.com/1682855/51850975-ea4e3480-22f0-11e9-9128-d945e1e2a9ab.png?classes=float-left)  
  
##### (v5 Oct 2021)  
#### by Brian Mullan (bmullan.mail@gmail.com)  

---  

---  

_**I am happy to introduce CIAB v5**_ of the CIAB Remote Desktop System.  

**CIAB** ("*Cloud-In-A-Box*") Remote Desktop System is a server application that integrates and extends the [Apache Guacamole](https://guacamole.apache.org/) clientless remote desktop gateway on a Ubuntu 20.04 LTS host with all applications running in LXD System Containers. 

_Using **only** a web browser that supports HTML5, users can connect to a **CIAB System installed either locally or remotely on Cloud, VM or Physical Server**._    
_During installation the Admin can choose from many different **Desktop Environments** including:_  
- Kubuntu (re KDE)  
- Lubuntu (re LXDE)  
- Ubuntu Budgie  
- Ubuntu Gnome  
- Ubuntu MATE  
- Xubuntu (re XFCE)  

--- 

####_ **CIAB - "Cloud in a Box"**_  

The file _**"install-ciab.zip"**_ includes _**all**_ of the installation Bash Scripts and associated files required to create an *LXD container based CIAB Remote Desktop System*.  

CIAB installation will create two LXD containers:  
 
- **ciab-cn1** - which will have an installer's choice of *Desktop Envrionment* installed in it  
- **ciab-guac** - will have Guacamole, Tomcat9, PostgreSQL, and NGINX installed via Docker in *ciab-guac*.   We create the LXD "_**ciab-guac**_" container  
   with an command option to _**"enable**_ container _**"nesting"**_.   This is why we are able to install Docker _"inside"_ the LXD "_**ciab-guac**_"  
   container
   
Once installation is complete you can access both Guacamole & the ciab-cn1 based Desktop using any HTML5 Web Browser.  
   
We configure _Guacamole/NGINX_ etc with a _**"self-signed"**_ certificate to allow support for using HTTPS.   This means the connection **from** a User **to**  
the Remote Desktop is _**encrypted**_.  

---

---
  
#### Steps to Install CIAB Remote Desktop  

---  

_Installation of CIAB is predominately automated and requires minimal input by the Admin/Installer!_  
  
_**Steps:**_  
1) Copy the _**install-ciab.zip**_ to the (local/remote) (Cloud, VM, server etc) you want to create the CIAB System  
2) Unzip _**install-ciab.zip**_  
3) Execute _**ciab-pre-install.sh**_  
4) Execute  _**install-ciab.sh**_  

---

*NOTE*:   When _**Step 4**_ completes...  
 
a) _**both**_ of the CIAB LXD containers (**ciab-guac** and **ciab-cn1**) will have been *created*  
b) a _**"working"**_ installation directory **/opt/ciab/**  will have been created in *each* container  
c) additional configuration scripts specific to setting up software _**specific**_ to the function of each LXD container  
-- scripts to install Docker, Guacamole, Tomcat9, PostgreSQL, NGINX in the **ciab-guac** LXD container  
-- scripts to install a Desktop Environment and a User Acct for the person doing the CIAB installation into the _**ciab-cn1**_ container.  
 
---

---

At this point, refer to the [CIAB README-CIAB Installation.pdf](https://github.com/bmullan/CIAB_Remote_Desktop_System-v5/blob/main/README-CIAB%20Installation.pdf) for all addtional Installation Steps...
