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

<h2>Deployment and Configuration Steps</h2>

-Let's first check th IP address of the VM. Go to command prompt and type ipconfig and chekc your IP address


<img src="https://i.imgur.com/9iK5up6.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>

 -Now that we have the IP address let's check connectivity from your actual PC. To do this we need to turn off the VM firewall. Type on wf.msc to serch for Windows Firewall 

<img src="https://i.imgur.com/RZEn3Gq.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

-Select Windows Defender Firewall Properties

<img src="https://i.imgur.com/3E6gR3i.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

-And turn off the firewall state on the Domain Profile, Private Profile and Public Profile sections

<img src="https://i.imgur.com/vZNEupP.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>

-Now ping it from your actual PC in the command prompt you should get a response 

<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

-Go to Nessus Essentials it is basically a web app. Your session may have expired just sign in again. Create a new scan and  select a Basic Network Scan

<img src="https://i.imgur.com/XinsTmz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

-Name it something like Windows 10 Single Host and on the targets section put the VM IP address. You can configure the scan to do it regularly if you work for an organization for instance, an even provide the credentials of the VM so Nessus can go deeply into the VM and scan even more potential vulnerabilities. 

<img src="https://i.imgur.com/QWOpmXZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

-Leave everything by default and click Save, and now we have the scan to run it in the future

<img src="https://i.imgur.com/ricNvKy.png" height="100%" width="100%" alt="Disk Sanitization Steps"/>

-Click and Launch the scan. 

<img src="https://i.imgur.com/SVYEKmK.png" height="100%" width="100%" alt="Disk Sanitization Steps"/>

-You can check the progress if you click on it. Let's wait for the scan to finish and see

<img src="https://i.imgur.com/pdJUJt5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

-Now that the scan was run you can check and see the severity of the Vulnerabilities from Critical to Info, since we run this scan without credentials it will just give us a little bit of vulnerabilities 

<img src="https://i.imgur.com/eVoXhmU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

-You can click on vulnerabilities and check what is going on, it will show all of the vulnerabilities that were found and you can click on them and will give you more information even how to remidiate it. The blue ones(info) won't probably requiere a solution but it's something that you should be aware off 

<img src="https://i.imgur.com/5ccSUJ3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

- Next thing we are going to do is set up the VM to be able to accept authenticated scans and provide the credentials to Nessus and we are going to run the scan again and see the results of the new scan

-Now back into the VM let's search for services 

<img src="https://i.imgur.com/VNMdf2a.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>

-First we are going to enable Remote Registry that will allow the scanner to connect to this computer registry and kind of crawl through the registry and look for insecure configurations, double click on it after you found it 

<img src="https://i.imgur.com/TBeMjj9.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>

-Set up the starup type on Automatic -> Start -> OK. Now it is enabled

<img src="https://i.imgur.com/8Gxs489.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>

 -Now go to Change User Account Control settings and since our computer is not on the domain we have to do the kind of hacks things to be able to run the scan 
 
<img src="https://i.imgur.com/c0ERbUX.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>

-Turn the bar all the way down and click OK

<img src="https://i.imgur.com/OSf0IO5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

-Now open the registry and we need to add a key that's supposed to further disable user account control for the remote account we are going to use to connect to this computer during the scan 

<img src="https://i.imgur.com/MDesEpj.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>

-We need to browse for HKEY_LOCAL_MACHINE->Software->Microsoft->Windows->CurrentVersion->Policies->System. Inside here we are going to create a word called "LocalAccountTokenFilterPolicy" right click on a blanck->New->DWORD(32-bit)Value, name it and then Enter, double click it and set the value data to 1, close the registry. Next restart the VM

<img src="https://i.imgur.com/athysoQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

-Then log in again and we need to go to Nessus, check the scan you created, click on More and Configure, and we are going to add a set of credentials. Type the username and password of the VM and click save

<img src="https://i.imgur.com/6eefcFz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

-Then launch the scan again and when it finished let's compare the results. We should be able to see more results since we provide Nessus a set of credentials and we configured the VM to accept remote scans



<img src="https://i.imgur.com/c0ERbUX.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>



<img src="https://i.imgur.com/c0ERbUX.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>


<img src="https://i.imgur.com/c0ERbUX.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>


<img src="https://i.imgur.com/c0ERbUX.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>

