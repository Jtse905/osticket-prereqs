# osticket-prereqs<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- osTicket-v1.15.8
- PHPManagerForIIS_V1.5.0
- HeidiSQL_12.3.0.6589
- mysql-5.5.62-win32
- Rewrite_amd64_en-US
- VC_redist.x86

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To begin, we must first install Internet Information Services (IIS) in Windows. To do so, open up the control panel. Once the control panel is open, on the left side click on "Turn Windows features on or off".
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
With the Windows Features window open, scroll down until you find "Internet Information Services". Check the box next to it, and open "World Wide Web Services". Then open "Application Development Features", and check the box next to "CGI". 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once IIS has been setup, we need to install "IIS URL Rewrite Module 2". Once installed, exit the window and open up your "File Explorer" and go to the C: drive. 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once in the C: drive, create a new folder and name it "PHP". 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once the "PHP" folder is created in the C: drive, extract the contents of the file named "php-7.3.8-nts-Win32-VC15x-86" into the "PHP" folder you created. 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, we will install "Microsoft Visual C++ 2015-2022 Redistribution (x86)". 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once "Microsoft Visual" is installed, we will need to install "MySQL Server 5.5". 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once "MySQL" is installed, open up "IIS Manager" in Windows. We Will now enable "PHP" within "IIS". With "IIS" open, on the left click on "osTicket-Window" under the "Connections" tab. Than click on "PHP Manager". 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Inside the "PHP Manager", click on "Register new PHP Version" underneath PHP Setup. 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once the "Register New PHP Version" window is open, search for the "PHP" folder that you created earlier in the C: drive. 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Inside the "PHP" folder, select the application "php-cgi". Click open and click okay to register the new PHP version. 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once the new PHP Version is installed, restart the osTicket server inside "IIS Manager" by right clicking on "osTicket-Window" and clicking "stop". Wait a couple seconds, and than right click "osTicket-Window" again and click on "start". 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After the server restart, we need to install the osTicket files. To do so, open up two "File Explorer" windows. To do so, right click "File Explorer" and click "File Explorer". Do this two times. In one "File Explorer" window, navigate to your downloads and locate the your osTicket instillation files. You should see an "upload" file. In the second "File Explorer" window, navigate to the "inetpub" folder and enter it. Go to "wwwroot" file. Once inside, move the "upload" folder from your osTicket instillation files, into the "wwwroot" file. 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once the "upload" folder is inside the "wwwroot" folder, we need to change name of the "upload" folder. Right click the "upload" folder and change the name to "osTicket".  
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Finally, we may open up osTicket. To do so, inside "IIS", on the left side, click on osTicket. Than, on the right side, click on "Browse .80(http)". This will open up a new window on your web browser for osTicket. 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
We will now have to install some recommended extensions. We will need to open up "IIS Manager" again. Within "IIS", on the left side open the "sites" tab, then the "Default Web Site" tab. Click on the "osTicket" tab. On the right side, open up the "PHP Manager". 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
With the "PHP Manager" open, underneath the "PHP Extensions", click on "Enable or disable an extension". 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In "PHP Extensions", scroll down until you see "php_imap.dll". Right click it and click "enable". 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Next, scroll down to "php_opcache.dll" and enable it.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lastly, find "php_intl.dll" and enable it. 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Now go back to osTicket in your web browser. Refresh the page to see that the extensions have been enabled. 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
We will now have to rename a specific file inside the osTicket folder. Go to your C: drive. Inside the C: drive, go inside the "inetpub" folder. Once inside, go into the "wwwroot" folder, then the "osTicket" folder, and finally the "include" folder. Once inside the "include" folder, scroll down until you find the "ost-sampleconfig.php" file. Remove "sample" from the name. Rename it to "ost-config.php". 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
On the osTicket web browser window, you can click continue to go to the next screen. Next we will have to edit security permissions for osTicket. To do so, right click on the "ost-config.php" file and click on "properties". 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
With the properties window open, click on the "security" tab. With the "security" tab open, click on "advanced" towards the bottom. 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Click on "Disable inheritance" and then "Remove all inherited permissions from this object". This will disable all permissions for this file. So osTicket may function properly in this lab. We would NOT do this in a real-world scenario. 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
We then will add permissions to the file. Click on "Add" in the "Advanced Security Settings" window. Towards the top click "Select a principle". Select the open window in the "Enter the object name to select" window. Type "everyone" to give everyone on the system permissions to this file, this setup is only for lab simulation. We would NOT do this in a real life scenario. With everyone typed in, click "check names". After, click okay. You may exit each window and open the osTicket web browser tab, click continue.  
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
On this page, input input your information to setup your organization. Stop once you get down to "Database Settings". You will need to input an SQL Database which we will install and create.  
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In your "downloads folder", find and install "HeidiSQL 12.3.0.6589". Once installed, open "HeidiSQL". Here we will need to create a new SQL. To create one, click on "new" at the bottom left. 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
We will need to create a new database to connect to for osTicket. Right click the bolded "Unnamed" word, and click on "Create new" then click on "database". 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Name your database "osTicket" and click "OK". 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Once you have named your database "osTicket", in osTicket on your web browser, input "osTicket" inside the "MySQL Database" line. Then input information for the "SQL Username" and "SQL Password". Then towards the bottom of the page, click "Install now". 
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
You may now see that osTicket is fully configured in the web browser. You may also see some data being compiled in "HeidiSQL". 
</p>
<br />
