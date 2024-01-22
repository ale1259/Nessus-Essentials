<img src="https://i.imgur.com/a3TTDwx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

# Nessus-Essentials Vulnerability Scanner

<h2>Environments and Technologies Used</h2>

- VMware
- Nessus Esssenials

<h2>Operating Systems Used </h2>
 - Windows 10


 <h2>High-Level Deployment and Configuration Steps</h2>

- Download and install VMware from this link https://www.vmware.com/products/workstation-player/workstation-player-evaluation.html

  -On the vendor's website select download for windows
<img src="https://i.imgur.com/bpzwJLE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

- Next step download Windows 10 ISO that is basically a file that allow us to install Windos 10 in a Virtual Machine. Click this link https://www.microsoft.com/en-us/software-download/windows10

  -Scroll down and select to Create Windows 10 installation media and download it
<img src="https://i.imgur.com/arUoXI0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

  -Open the .exe that you just download and start the creation of the ISO file

  -Click accept on the first window
<img src="https://i.imgur.com/XA5KM6u.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

 -On the second one select "Create installation media(USB flash drive,DVD, or ISO file) for another PC", click next 
<img src="https://i.imgur.com/QinB5YQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

  -On the next window leave everything by default
<img src="https://i.imgur.com/qH2Eogk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

  -Click next and select ISO file and click next again and choose where you wanted and put it in a folder
<img src="https://i.imgur.com/JvVVccN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

- While this is downloading let's install Nessus Essentials our vulnerability scanner. go to this link https://www.tenable.com/products/nessus/nessus-essentials
  
 -On the website on the right part fill out the information part to acquire a code that we need to activate Nessus Essentials, this will be send to your email 

<img src="https://i.imgur.com/DT5n1QH.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

-Go to your email and click Download Nessus and it will take you to a page that look like this 
<img src="https://i.imgur.com/CLRa80D.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

-Click on Tenable Nessus

<img src="https://i.imgur.com/lPZPn5X.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

-And select the one that says Windows-x86_64 105 MB- Windows Server 2012 and choose where to download it. The downloading progress is pretty straight foward just next until installation 
<img src="https://i.imgur.com/usdLy8O.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

<img src="https://i.imgur.com/eIIvmVj.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

<img src="https://i.imgur.com/qOlaVyn.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

<img src="https://i.imgur.com/MWQRYXt.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

<img src="https://i.imgur.com/mNo7iWA.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>



-After the installation finish will take you to a website. I sugest that you save the URL of the website so you can come back later 

<img src="https://i.imgur.com/Dc9ngAC.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>

-Click on Connect via SSL

<img src="https://i.imgur.com/g6A7aMx.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>

-Click on Advanced and Continue to localhost(unsafe)

<img src="https://i.imgur.com/pcCUFtu.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>

-First windows click Continue

<img src="https://i.imgur.com/p1h0EGU.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>

-Second window Register for Nessus Essentials

<img src="https://i.imgur.com/NmzqEJe.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>

-Skip the Get an activation code part since we already have it

<img src="https://i.imgur.com/8a7buIs.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>

-And put the activation code sent to your email, after that will ask you to create an account set up a username and password, submit it and it should start installing this may take some time 

<img src="https://i.imgur.com/C6VqtRB.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>

- Let's set up our Virtual Machine in the meantime. Open VMware Worksation and create a new Virtual Machine, the Windows 10 ISO should be downloaded by now go and search for it

<img src="https://i.imgur.com/Tj5jlhg.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
   
 -Look up for the location of your ISO file and continue the process is pretty straight foward. On the disk size adjust depending on your capacity

<img src="https://i.imgur.com/CF9fBnJ.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>

 -On this window select customize hardware. Depending on your hardware on this windows adjust the RAM dedicated to the VM, the number of processors, etc. 
 
<img src="https://i.imgur.com/YZHozFp.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>

 -Click close and Finish and it will start preparing the VM. Make sure you click any key to start booting the windows installation on the VM. Note press CTRL+Alt to return your cursor

 -The Windows installation process is simple. On this window select I don't have a product key, after that select Windows 10 Pro, accept the licence terms

 <img src="https://i.imgur.com/uHsT5aJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

 
-Select custom for this window, and select the hardrive you create. This will take some time too so come back when Nessus and Windows 10 are installed. To finish the VM select the region, skip the add a second keyboard part. Set up for personal use, Offline account, Limited expirience, name it, set up a password 

<img src="https://i.imgur.com/xFTTtEA.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>

 -Select "NO" for all of this settings. Continue skipping all the weird setting and Accept

<img src="https://i.imgur.com/emSmPdh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

- By now we should have our VM ready and Nessus Essentials ready to go. We are going to do a first basic scan against the VM, then a credential scan later to see what feedback we get from Nessus

-Let's first check th IP address of the VM. Go to command line and type ipconfig and chekc your IP address


<img src="https://i.imgur.com/9iK5up6.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>

 -Now that we have the IP address let's check connectivity from your actual PC. To do this we need to turn off the VM firewall. Type on wf.msc to serch for Windows Firewall 

<img src="https://i.imgur.com/RZEn3Gq.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

-Select Windows Defender Firewall Properties

<img src="https://i.imgur.com/3E6gR3i.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

-And turn off the firewall state on the Domain Profile, Private Profile and Public Profile sections

<img src="https://i.imgur.com/vZNEupP.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>


<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
