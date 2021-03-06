![ciab-logo](https://user-images.githubusercontent.com/1682855/51850975-ea4e3480-22f0-11e9-9128-d945e1e2a9ab.png?classes=float-left)  
  
##### (v6 Jan 2022)  
#### by Brian Mullan (bmullan.mail@gmail.com)  

---  

*Installation time is approx 13-15 minutes.*

---  

_**I am happy to introduce CIAB v6**_ of the CIAB Remote Desktop System.  

**CIAB** ("*Cloud-In-A-Box*") Remote Desktop System is a server application that integrates and extends the [Apache Guacamole](https://guacamole.apache.org/) clientless remote desktop gateway on a Ubuntu 20.04 LTS host with all applications running in LXD System Containers.   

_Using **only** a web browser that supports HTML5, users can connect to a **CIAB System installed either locally or remotely on Cloud, VM or Physical Server**._  

  
_During installation the Admin can choose from many different **Desktop Environments** including:_  
- Lubuntu (re LXDE)  
- Ubuntu Budgie  
- Ubuntu Gnome  
- Ubuntu MATE  
- Xubuntu (re XFCE)  
- Kubuntu (re KDE) - **NOTE**: *The KDE desktop is not implemented at this time but hopefully soon.* 

--- 

#### _**CIAB - "Cloud in a Box"**_  

The file _**"ciab.zip"**_ includes _**all**_ of the installation Bash Scripts and associated files required to create an *LXD container based CIAB Remote Desktop System*.  

CIAB installation will create two LXD containers:  
 
- **ciab-cn1** - which will have an installer's choice of *Desktop Envrionment* installed in it  
- **ciab-guac** - will have Guacamole, Tomcat9, PostgreSQL, and NGINX installed via Docker in *ciab-guac*.  
       
   We create the LXD "_**ciab-guac**_" container with the command option to _**"enable**_ container _**"nesting"**_. 
   This is why we are able to install Docker _"inside"_ the LXD "_**ciab-guac**_" container.  
   
Once installation is complete you can access both Guacamole & the ciab-cn1 based Desktop using any HTML5 Web Browser.  
   
We configure _Guacamole/NGINX_ etc with a _**"self-signed"**_ certificate to allow support for using HTTPS.   
  
This means the connection **from** a User **to** the Remote Desktop is _**encrypted**_.  

> _**NOTE**_ 
> *With CIAB-Guacamole for user "Connections" you can configure CIAB-Guacamole to also connect to Windows Servers !*


---
  
#### Steps to Install CIAB Remote Desktop System v6    

---  

_Installation of CIAB is predominately automated and requires minimal input by the Admin/Installer!_  

Execute the following 2 Bash scripts extracted from the CIAB.ZIP file

> 1. **ciab-pre-install.sh**
> 2. **ciab-install.sh**
  
**Steps to Install CIAB:**   
Follow the Installation Diagrams & Information in the _**[CIAB Remote Desktop System Installation Guide.PDF](https://github.com/bmullan/CIAB_Remote_Desktop_System-v6/blob/main/CIAB%20Remote%20Desktop%20System%20Installation.pdf)**_


---

---


