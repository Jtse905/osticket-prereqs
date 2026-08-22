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
<img width="1215" height="846" alt="1" src="https://github.com/user-attachments/assets/b3347a1b-8a19-4dfe-94e7-b7824f331b9c" />
</p>
<p>
To begin, we must first install Internet Information Services (IIS) in Windows. To do so, open up the control panel. Once the control panel is open, on the left side click on "Turn Windows features on or off".
</p>
<br />

<p>
<img width="1350" height="809" alt="2" src="https://github.com/user-attachments/assets/49451dc3-c139-4b87-8f23-1824665b1106" />
</p>
<p>
With the Windows Features window open, scroll down until you find "Internet Information Services". Check the box next to it, and open "World Wide Web Services". Then open "Application Development Features", and check the box next to "CGI". 
</p>
<br />

<p>
<img width="951" height="748" alt="4" src="https://github.com/user-attachments/assets/4c224072-e4cc-4cf0-8bcf-aba03b26b7c7" />
</p>
<p>
Once IIS has been setup, we need to install "IIS URL Rewrite Module 2". Once installed, exit the window and open up your "File Explorer" and go to the C: drive. 
</p>
<br />

<p>
<img width="1239" height="840" alt="5" src="https://github.com/user-attachments/assets/58d00695-ab1c-49ba-859b-db905d440fdd" />
</p>
<p>
Once in the C: drive, create a new folder and name it "PHP". 
</p>
<br />

<p>
<img width="1991" height="1059" alt="6" src="https://github.com/user-attachments/assets/c824d340-8233-48cf-ba3a-9d10d0f66f58" />
<img width="2023" height="936" alt="7" src="https://github.com/user-attachments/assets/dd319129-a5fc-4d26-a020-9436389f909f" />
</p>
<p>
Once the "PHP" folder is created in the C: drive, extract the contents of the file named "php-7.3.8-nts-Win32-VC15x-86" into the "PHP" folder you created. 
</p>
<br />

<p>
<img width="1030" height="597" alt="8" src="https://github.com/user-attachments/assets/311a6b87-5f47-402c-ab1f-462030ba2625" />
</p>
<p>
Next, we will install "Microsoft Visual C++ 2015-2022 Redistribution (x86)". 
</p>
<br />

<p>
<img width="927" height="655" alt="9" src="https://github.com/user-attachments/assets/3daae710-5302-4983-bd2c-062b6f4ea847" />
</p>
<p>
Once "Microsoft Visual" is installed, we will need to install "MySQL Server 5.5". 
</p>
<br />

<p>
<img width="2122" height="1148" alt="10" src="https://github.com/user-attachments/assets/7d5f4bde-6c2f-465f-94d3-f14db381be03" />
</p>
<p>
Once "MySQL" is installed, open up "IIS Manager" in Windows. We Will now enable "PHP" within "IIS". With "IIS" open, on the left click on "osTicket-Window" under the "Connections" tab. Than click on "PHP Manager". 
</p>
<br />

<p>
<img width="1134" height="1147" alt="11" src="https://github.com/user-attachments/assets/53b351d0-59e6-4a7d-ad28-6ed234627802" />
</p>
<p>
Inside the "PHP Manager", click on "Register new PHP Version" underneath PHP Setup. 
</p>
<br />

<p>
<img width="2018" height="1102" alt="12" src="https://github.com/user-attachments/assets/e7cbb40f-343b-4a93-ad70-de08ddde054f" />
</p>
<p>
Once the "Register New PHP Version" window is open, search for the "PHP" folder that you created earlier in the C: drive. 
</p>
<br />

<p>
<img width="1976" height="1106" alt="13" src="https://github.com/user-attachments/assets/dcb1332c-5b15-4132-9bff-f1b78acf5e77" />
</p>
<p>
Inside the "PHP" folder, select the application "php-cgi". Click open and click okay to register the new PHP version. 
</p>
<br />

<p>
<img width="1973" height="1064" alt="14" src="https://github.com/user-attachments/assets/6535a75e-e5ff-444a-8c83-177acf3e83a8" />
<img width="1965" height="1075" alt="15" src="https://github.com/user-attachments/assets/674d8a11-3d0e-46bb-89af-398c9923bbe0" />
</p>
<p>
Once the new PHP Version is installed, restart the osTicket server inside "IIS Manager" by right clicking on "osTicket-Window" and clicking "stop". Wait a couple seconds, and than right click "osTicket-Window" again and click on "start". 
</p>
<br />

<p>
<img width="2269" height="738" alt="16" src="https://github.com/user-attachments/assets/8cb9948a-1207-4102-b960-055f50ce1d46" />
</p>
<p>
After the server restart, we need to install the osTicket files. To do so, open up two "File Explorer" windows. To do so, right click "File Explorer" and click "File Explorer". Do this two times. In one "File Explorer" window, navigate to your downloads and locate the your osTicket instillation files. You should see an "upload" file. In the second "File Explorer" window, navigate to the "inetpub" folder and enter it. Go to "wwwroot" file. Once inside, move the "upload" folder from your osTicket instillation files, into the "wwwroot" file. 
</p>
<br />

<p>
<img width="2013" height="713" alt="17" src="https://github.com/user-attachments/assets/7ac8cd70-f190-4fb8-bc85-9ec7e7aad204" />
</p>
<p>
Once the "upload" folder is inside the "wwwroot" folder, we need to change name of the "upload" folder. Right click the "upload" folder and change the name to "osTicket".  
</p>
<br />

<p>
<img width="2094" height="1209" alt="18" src="https://github.com/user-attachments/assets/bca05391-8fed-4478-8240-188b1911cfbd" />
</p>
<p>
Finally, we may open up osTicket. To do so, inside "IIS", on the left side, click on osTicket. Than, on the right side, click on "Browse .80(http)". This will open up a new window on your web browser for osTicket. 
</p>
<br />

<p>
<img width="1995" height="893" alt="19" src="https://github.com/user-attachments/assets/0f4d7fe4-f8f9-4ab1-ab69-c788a38dbbe7" />
</p>
<p>
We will now have to install some recommended extensions. We will need to open up "IIS Manager" again. Within "IIS", on the left side open the "sites" tab, then the "Default Web Site" tab. Click on the "osTicket" tab. On the right side, open up the "PHP Manager". 
</p>
<br />

<p>
<img width="1287" height="1251" alt="20" src="https://github.com/user-attachments/assets/c471952a-2490-45a8-a714-8617f7206657" />
</p>
<p>
With the "PHP Manager" open, underneath the "PHP Extensions", click on "Enable or disable an extension". 
</p>
<br />

<p>
<img width="1360" height="1261" alt="21" src="https://github.com/user-attachments/assets/96a31159-bb7d-4a25-8180-e685e9e7f871" />
</p>
<p>
In "PHP Extensions", scroll down until you see "php_imap.dll". Right click it and click "enable". 
</p>
<br />

<p>
<img width="1067" height="1170" alt="22" src="https://github.com/user-attachments/assets/d5f210ed-533a-4df5-91a5-1311288cb0c2" />
</p>
<p>
Next, scroll down to "php_opcache.dll" and enable it.
</p>
<br />

<p>
<img width="1060" height="483" alt="21 5" src="https://github.com/user-attachments/assets/f78f44f3-1b3b-4f92-891b-c13378188fdb" />
</p>
<p>
Lastly, find "php_intl.dll" and enable it. 
</p>
<br />

<p>
<img width="1163" height="932" alt="23" src="https://github.com/user-attachments/assets/fa50adfb-14bb-4a35-a557-aef921896d7c" />
</p>
<p>
Now go back to osTicket in your web browser. Refresh the page to see that the extensions have been enabled. 
</p>
<br />

<p>
<img width="1580" height="1440" alt="25" src="https://github.com/user-attachments/assets/b88cfa1d-ab02-41ef-8a37-4a3ed433ca1a" />
<img width="1289" height="773" alt="24" src="https://github.com/user-attachments/assets/e9b3d024-f951-4aab-88d0-26a439ebc59d" />
</p>
<p>
We will now have to rename a specific file inside the osTicket folder. Go to your C: drive. Inside the C: drive, go inside the "inetpub" folder. Once inside, go into the "wwwroot" folder, then the "osTicket" folder, and finally the "include" folder. Once inside the "include" folder, scroll down until you find the "ost-sampleconfig.php" file. Remove "sample" from the name. Rename it to "ost-config.php". 
</p>
<br />

<p>
<img width="1089" height="1435" alt="26" src="https://github.com/user-attachments/assets/0e9c77b4-d28e-4804-8372-22c1125f0a5b" />
</p>
<p>
On the osTicket web browser window, you can click continue to go to the next screen. Next we will have to edit security permissions for osTicket. To do so, right click on the "ost-config.php" file and click on "properties". 
</p>
<br />

<p>
<img width="1525" height="1187" alt="27" src="https://github.com/user-attachments/assets/0f11074c-dddd-4298-abf8-dae51a83f788" />
</p>
<p>
With the properties window open, click on the "security" tab. With the "security" tab open, click on "advanced" towards the bottom. 
</p>
<br />

<p>
<img width="1525" height="866" alt="28" src="https://github.com/user-attachments/assets/f07d13f7-687e-462a-853a-f6ee4337a149" />
<img width="1348" height="944" alt="29" src="https://github.com/user-attachments/assets/3795c50f-65a2-4863-84f9-06555c78a487" />
</p>
<p>
Click on "Disable inheritance" and then "Remove all inherited permissions from this object". This will disable all permissions for this file. So osTicket may function properly in this lab. We would NOT do this in a real-world scenario. 
</p>
<br />

<p>
<img width="1502" height="1015" alt="30" src="https://github.com/user-attachments/assets/632ef30f-718b-4822-ba03-06d213c7ab09" />
</p>
<p>
We then will add permissions to the file. Click on "Add" in the "Advanced Security Settings" window. Towards the top click "Select a principle". Select the open window in the "Enter the object name to select" window. Type "everyone" to give everyone on the system permissions to this file, this setup is only for lab simulation. We would NOT do this in a real life scenario. With everyone typed in, click "check names". After, click okay. You may exit each window and open the osTicket web browser tab, click continue.  
</p>
<br />

<p>
<img width="1165" height="1388" alt="31" src="https://github.com/user-attachments/assets/ca10ccff-87ad-4384-885c-e39e95e4c334" />
</p>
<p>
On this page, input input your information to setup your organization. Stop once you get down to "Database Settings". You will need to input an SQL Database which we will install and create.  
</p>
<br />

<p>
<img width="1408" height="943" alt="32" src="https://github.com/user-attachments/assets/ca67a760-013f-4bb4-8293-8bfebe5e99e3" />
<img width="1029" height="743" alt="33" src="https://github.com/user-attachments/assets/779accd4-03c5-422d-b6d0-16d96458da79" />
</p>
<p>
In your "downloads folder", find and install "HeidiSQL 12.3.0.6589". Once installed, open "HeidiSQL". Here we will need to create a new SQL. To create one, click on "new" at the bottom left. 
</p>
<br />

<p>
<img width="1069" height="720" alt="34" src="https://github.com/user-attachments/assets/8e010708-baf8-4f51-8a07-870f46ce4aff" />
</p>
<p>
We will need to create a new database to connect to for osTicket. Right click the bolded "Unnamed" word, and click on "Create new" then click on "database". 
</p>
<br />

<p>
<img width="1082" height="673" alt="35" src="https://github.com/user-attachments/assets/e1e6e89d-0b49-4b2f-820b-d1e7c2e8ce2e" />
</p>
<p>
Name your database "osTicket" and click "OK". 
</p>
<br />

<p>
<img width="2213" height="1153" alt="36" src="https://github.com/user-attachments/assets/77bdca87-e2bb-4867-85e1-70eabc36fff2" />
</p>
<p>
Once you have named your database "osTicket", in osTicket on your web browser, input "osTicket" inside the "MySQL Database" line. Then input information for the "SQL Username" and "SQL Password". Then towards the bottom of the page, click "Install now". 
</p>
<br />

<p>
<img width="1891" height="1230" alt="37" src="https://github.com/user-attachments/assets/95a51110-65b5-41dd-a167-5f3a3a69c85b" />
</p>
<p>
You may now see that osTicket is fully configured in the web browser. You may also see some data being compiled in "HeidiSQL". osTicket is now setup. 
</p>
<br />
