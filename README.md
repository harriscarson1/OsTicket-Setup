<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating System </h2>

- Windows 10</b> (22H2)


<h2>Installation Steps</h2>

<p>
Create an Azure VM running Windows 10
  </p>
<p>
  <img src="https://github.com/user-attachments/assets/6b911172-a987-4454-a079-f2a850da2ede" height="80%" width="80%"/>
  <img src="https://github.com/user-attachments/assets/5a4ff2b6-0e8a-4745-9d16-b00e08908aaf" height="80%" width="80%"/>
</p>
<br />

<p>
Useing Remote Desktop connect to the VM using the public IP address
  </p>
<p>
  <img src="https://github.com/user-attachments/assets/1bf8ee3f-3465-4213-8dbc-396eae98e450" height="80%" width="80%"/>
</p>
<br />
<p>
Download the required installation files for osTicket  on the VM and unzip the files to the desktop 
  </p>
<p>
  <img src="https://github.com/user-attachments/assets/e8dbcd53-35e1-41ee-b16a-029e1f630858" height="80%" width="80%"/>
</p>

<br />
<p>
In Control panel> Programs > Programs and features > Turn Windows features on or off, turn on the Internet Information System as well as enabling CGI which is in Internet Information Services > World Wide Web Services > Application Development Features > CGI
</p>
<p>

  <img src="https://github.com/user-attachments/assets/5fab12d4-eb24-4319-81ae-b2fb1116f727" height="80%" width="80%"/>
  <img src="https://github.com/user-attachments/assets/490411de-4c97-42d7-8ffe-32e7ed808795" height="80%" width="80%"/>
</p>
<br />
<p>
Then click OK and  IIS will install
  </p>
<p>
  <img src="https://github.com/user-attachments/assets/95a92fe2-f4e5-4e28-99e2-d276951558cd" height="80%" width="80%"/>
</p>
<br />
<p>
Confirm IIS is functional by checking 127.0.0.1 (loopback) in a web browser
  </p>
<p>
  <img src="https://github.com/user-attachments/assets/04c7e47a-e88b-41c7-90fe-26f4c8fee262" height="80%" width="80%"/>
</p>
<br />
<p>
Install PSPManager for IIS by double clicking it and going through the setup wizard
  </p>
<p>
  <img src="https://github.com/user-attachments/assets/9b47ecfc-2b7e-4c9d-b575-e80f332096dc" height="80%" width="80%"/>
</p>
<br />
<p>
Next we need to install the Rewrite module by clicking the installer
  </p>
<p>
  <img src="https://github.com/user-attachments/assets/52c1172e-6886-47b7-9d6c-9da72b2a462c" height="80%" width="80%"/>
</p>
<br />
<p>
Make a folder in the C: drive make a file named PHP
  </p>
<p>
  <img src="https://github.com/user-attachments/assets/9aa0aca3-5895-4c9c-a4a3-56434e756d3c" height="80%" width="80%"/>
</p>
<br />
<p>
Extract the PHP files into this folder we just created
  </p>
<p>
  <img src="https://github.com/user-attachments/assets/f058c592-e597-4953-afdc-37a44be14e07" height="80%" width="80%"/>
</p>
<br />
<p>
Next install Visual C++ Redist. using the installer
  </p>
<p>
  <img src="https://github.com/user-attachments/assets/828e4b5f-2918-43d3-9900-9a34914c2654" height="80%" width="80%"/>
</p>
<br />
<p>
Next we are installing the database for osTicket which is MySQL by using the installer selecting typical configuration and pressing install
  </p>
<p>
  <img src="https://github.com/user-attachments/assets/ca1c108d-2e48-424e-908e-f9f9efa76365" height="80%" width="80%"/>
</p>
<br />
<p>
Launch the configuration wizard and choose standard configuration set a username and password and then press execute to configure it
  </p>
<p>
  <img src="https://github.com/user-attachments/assets/51ebb869-0e0e-429c-bb3f-5fd300a09d30" height="80%" width="80%"/>
  <img src="https://github.com/user-attachments/assets/37f228b5-0b1e-4a13-9536-88d86ed28e75" height="80%" width="80%"/>
</p>
<br />
<p>
Next open IIS as and administrator and register PHP in the PHP manager by clicking register new PHP version and then browsing to the PHP file and then the php-cgi file in the C: drive and then clicking Ok
  </p>
<p>
  <img src="https://github.com/user-attachments/assets/e1ac205e-8d22-4d03-884b-3ffda7b979ef" height="80%" width="80%"/>
</p>
<br />
<p>
Then restart the IIS server by pressing the restart button
  </p>
<p>
  <img src="https://github.com/user-attachments/assets/721b8ef0-af7d-477e-8b23-04ffbe48296c" height="80%" width="80%"/>
</p>
<br />
<p>
Next we need to coly the osTicket files into the IIS server, We need to copy the upload file from the osTicket installation files to C:\inetpub\wwwroot and then rename the file osTicket
  </p>
<p>
  <img src="https://github.com/user-attachments/assets/69c0a72b-a3f0-4a2b-8fb0-f442602cdfd1" height="80%" width="80%"/>
</p>
<br />
<p>
We then need to restart IIS again
  </p>
<p>
  <img src="https://github.com/user-attachments/assets/e229874f-1ef3-4c74-9848-2c4ec39f38a0" height="80%" width="80%"/>
</p>
<br />
<p>
 Next we will try to browse to the Ticketing system, in IIS click sites > Default Web Site >osTicket once you click the osTicket folder there will be something one the right that says Browse *:80(http) we can click on that to view the site
  </p>
<p>
  <img src="https://github.com/user-attachments/assets/1a4d5298-987c-4251-b77a-062b242dc281" height="80%" width="80%"/>
</p>
<br />
<p>
Notice how some of the options are disabled
  </p>
<p>
  <img src="https://github.com/user-attachments/assets/f7abf99e-7fb1-48d9-86ed-902f39f4d861" height="80%" width="80%"/>
</p>
<br />
<p>
 To enable these we need to go back into IIS go to sites > Default Web Site >osTicket then select the PHP manager in PHP manager click enable or disable an extension then in that menu enable php_imap.dll, php_intl.dll, and php_opcache.dll
  </p>
<p>
  <img src="https://github.com/user-attachments/assets/a4dfae3a-fe68-40ef-bb47-07851d2dd151" height="80%" width="80%"/>
</p>
<br />
<p>
Refresh the site and see what changed
  </p>
<p>
  <img src="https://github.com/user-attachments/assets/c0bd7add-73ff-453a-8863-2c926639fb2a" height="80%" width="80%"/>
</p>
<br />
<p>
Next In C:\inetpub\wwwroot\osTicket\include we need to rename ost-sampleconfig.php to ost-sampleconfig.php
  </p>
<p>
  <img src="https://github.com/user-attachments/assets/3606e084-675f-4721-b4c5-e760ed07631e" height="80%" width="80%"/>
</p>
<br />
<p>
Next right click on ost-sampleconfig.php and click properties > security > advanced and then click enable inheritance to clear all the previous permissions and then for the sake of this demo i will just give everyone full access but this would be where you set permissions for access. Then click apply
</p>
<p>
  <img src="https://github.com/user-attachments/assets/0f3a1f3e-16e3-49f8-8548-24d79c6d9ac9" height="80%" width="80%"/>
</p>
<br />
<p>
Now go back to the osTicket webpage and press continue and fill in all the necessary information and then before pressing install we have to configure our database.
  </p>
<p>
  <img src="https://github.com/user-attachments/assets/65893db0-d95c-448c-a1a7-3fb0d6f001eb" height="80%" width="80%"/>
</p>
<br />
<p>
Now we will go back to the installation files and run the HeidiSQL setup, which will allow us to make a connection to our database
  </p>
<p>
  <img src="https://github.com/user-attachments/assets/60336003-a97d-4a7b-b1b4-f418d070ee18" height="80%" width="80%"/>
</p>
<br />
<p>
Once inside the HeidiSQL client press new on the bottom left and then input your user and password for your database you made earlier then press open
  </p>
<p>
  <img src="https://github.com/user-attachments/assets/5df3a07a-7def-4aeb-b605-55c024785a56" height="80%" width="80%"/>
</p>
<br />
<p>
Now right click where it says unnamed and click create new > Database and name it “osTicket” and press create
  </p>
<p>
  <img src="https://github.com/user-attachments/assets/6a29cd33-2fd0-462f-bfe7-1c69e741b73e" height="80%" width="80%"/>
</p>
<br />
<p>
Now go back to the osTicket setup webpage and type in your SQL database name username and password then click install now
  </p>
<p>
  <img src="https://github.com/user-attachments/assets/2c8a4c2f-8d62-47b4-ab13-347b874e5c0b" height="80%" width="80%"/>
</p>
<br />
<p>
osTicket is now fully installed and we have the respective links for users and admins at the bottom
</p>
<p>

  <img src="https://github.com/user-attachments/assets/fdd91195-d97c-4300-ad52-b9f0527df062" height="80%" width="80%"/>
</p>
<br />
<p>
Now we can see the osTicket database now has files in it and is fully functioning
  </p>
<p>
  <img src="https://github.com/user-attachments/assets/4f6668dd-3f7e-4802-b493-c39255de2580" height="80%" width="80%"/>
</p>
<br />
<p>
Now we can login
</p>
<p>
<img src="https://github.com/user-attachments/assets/a4e33d32-b085-4cd6-a451-81f271f003ae" height="80%" width="80%"/>
</p>
<br />
<p>
Now we are at our osTicket Dashboard
  </p>
<p>
  <img src="https://github.com/user-attachments/assets/73c2d42b-bc0d-40e3-aee3-9efe3822d557" height="80%" width="80%"/>
</p>
<br />
