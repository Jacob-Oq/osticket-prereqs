<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

you can find the necessary files <a href="https://drive.google.com/drive/u/2/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6">here!</a>
 

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- A modern computer (Although I was able to do this running Windows 7 and once on Linux | Ubuntu just to try it)
- A Microsoft Azure account to use a virtual machine
- Patience (Be sure to take your time and don't give in to frustrations. If something isn't working correctly double check and be sure a step didn't get skipped. This can take some time to get running and you may be tempted to rush things.)
- Minimal distractions. Focus is key.
- Maybe some backgorund music to help pass the time if you prefer

<h2>Installation Steps</h2>

If using a virtual machine be sure you are on the VM and not your main system. Then, before installing any files, be sure to have Internet Information Services (IIS) enabled. OsTicket will be installed locally and it needs IIS in order to function. To turn on IIS, open the Control Panel. 

![setting up iis -1](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/f08c96b9-2a08-4005-9f6c-841bd8dff76e)

From the Control Panel, open "Programs" and find "Turn Windows Features On or Off." 

![setting up iis -2](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/2c2d2ce1-a75d-4132-b3dd-4dc0f2ff9e76)

Within this menu, expand Internet Information Services, then Web Management Tools and enable IIS Management Console.

![setting up iis -3](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/255416f7-63fb-4ebc-a792-169abc44c3fc)


Click the "+" to expand "World Wide Web Services" then do the same at "Application Development Features." 

![setting up iis -4](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/9236a99a-46f3-45e5-a7e9-16a6421917e3)

![setting up iis -5](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/fc74f0d4-9dcc-4e72-998f-29367a1429c9)

Once there, enable CGI and click ok to confirm.

![setting up iis -6](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/ff60ab51-ea60-4a53-97a1-202b8d04ec92)


![setting up iis -7](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/8b073ec4-91c5-4b34-a6c5-0d3c3718622a)


<br><br/>

Next enable IIS then download and install PHP Manager for IIS (PHPManagerforIIS_V1.5.0.msi). 

![setting up iis -9](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/52aa064c-df81-4773-ac9c-d0e577cc8031)


Download and install the Rewrite Module (rewrite_amd64_en-US.msi) after installing PHP Manager for IIS. 

![setting up iis -10](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/fcaf0013-a84c-4eab-8fed-a82a625260a3)


<br></br>

After installing the Rewrite Module, create a new folder/directory called C:\PHP on the Windows (C:) drive. 

![setting up iis -11](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/87b6f842-53bb-413f-94f7-5f75a32a44be)


This new folder will be used to extract all the contents from the PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) zip folder into the C:\PHP folder. 

![setting up iis -12](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/a3c757aa-333b-4ef7-9048-a25e3596e29d)


<br></br>

Download and install VC_redist.x86.exe

![setting up iis -13](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/9016ea04-f1d5-438e-890d-9bf5577ee30d)


<br></br>

![setting up iis -14](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/76ddb561-cf94-4d50-addf-8d2155344179)

Once done, download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi). Within the MySQL setup wizard, click "I accept the terms" 

![setting up iis -15](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/13f5ca4a-627b-4a34-ade9-1946b4384b09)

select a Typical install. 

![setting up iis -16](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/1c6ec465-cb74-48bf-85a4-8d4e57304642)


Install. 

![setting up iis -17](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/76642bc8-fb5d-41f4-b568-e6d7e3092d55)


Launch the Configuration Wizard after the installation. Click next.

![setting up iis -18](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/a64cb9c8-9e6c-47ae-b36f-a2876d83a32e)

![setting up iis -19](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/d440110c-a3b4-4b01-a5e6-c021f0d2492f)


Select Standard Configuration and select Install As Windows Service and make sure Launch the MySQL Server automatically is checked. 

![setting up iis -20](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/9e0cc47c-a31c-4fe8-929a-abd03c2cc107)

![setting up iis -21](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/ccab1a56-988b-4100-b914-6b6b3efed506)

For credentials, the username will be root and the password of your choosing. For these purposes, the credentials will be basic to where they can be easily guessed.

![setting up iis -22](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/1a6c8c60-f160-40f8-8de0-e3b0fa9819d5)

Click excecute on the next prompt and allow it to finish.

![setting up iis -23](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/26fbd495-7db6-404c-82bb-9821f0792e28)


Then click Finish.

![setting up iis -24](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/478f5f04-a24a-4af5-a4d1-1d58a3856035)


<br></br>

Before installing osTicket, we need to configur IIS. Open IIS as an administrator. once it is open, select PHP Manager. 

![setting up iis -25](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/9887cf46-b68a-4f37-9792-542ff2fe950b)


Within PHP Manager, select Register new PHP version. 

![setting up iis -26](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/d75ffa82-da84-40a7-87a6-492318aa4190)


Select Browse and select the PHP CGI executable file (php-cgi.exe) within the PHP folder created earlier. 

![setting up iis -27](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/7eb2327d-8636-47b8-b467-9ce919c877da)


After registering the PHP version, reload the IIS server within the management console.

<br></br>

Download osTicket v1.15.8. Extract and copy the "upload" folder to the following path: c:\inetpub\wwwroot. Within the c:\inetpub\wwwroot folder, rename "upload" to "osTicket." Reload the IIS server afterwards. 

![setting up iis -28](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/d4891bb6-648c-422e-9484-ac67d016899f)

Within the IIS console, browse to Sites -> Default -> osTicket. 

![setting up iis -29](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/7515d61d-c156-4d35-877a-be1c9fac78b3)


Click "Browse *:80" and the installation page for osTicket will now show up. Some extensions are not enabled and they will be enabled with the IIS console before installing osTicket. 

![setting up iis -30](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/ec92f770-132a-43fd-a6fc-ee9d4ca5d552)


Click on PHP Manager while in the osTicket menu in IIS to begin the process. Click on "Enable or disable an extension." 

![setting up iis -31](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/f5ca785e-7f9e-48f4-b669-cc9b8ff635f9)


Enable the following extentions: php_imap.dll, php_intl.dll, php_opcache.dll. 

![setting up iis -32](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/fe82b542-120e-41b6-b8a5-eb1f94cfbeb2)

The osTicket installation page should now appear with all checks except APCu Extensions and Zend OP cache

![setting up iis -33](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/8c99ba4b-055e-4803-bf98-08ceef01dff2)

<br></br>

Before continuing to install osTicket, from C:\inetpub\wwwroot\osTicket\include, rename ost-sampleconfig.php to ost-config.php. 

![setting up iis -34](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/c0dc9b38-c5f5-4a31-9af6-76cec9b68922)

![setting up iis -35](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/fc338145-df9b-41c6-96ee-0d70c6c40145)


Next change the permissions to ost-config.php which was just created. Open its Properties and change the following permissions: Disable inheritence -> Remove All and New Permissions -> Everyone -> All. 

![setting up iis -36](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/7f05bb40-e92d-48a9-9f51-220c768915df)

![setting up iis -37](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/122e244f-9c66-4a2d-bb63-28259d58ab2f)

![setting up iis -38](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/bf9c306a-75d0-42f7-a9c4-9ca9fbbbe2f4)

![setting up iis -39](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/0b5a4644-0150-475e-b338-0dbbc97172d0)

![setting up iis -40](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/054c117f-2a75-433e-8da5-3768972601a7)

![setting up iis -41](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/4344c2d4-87a1-47b4-9e55-c20d871432d1)

![setting up iis -42](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/c4dab821-8b96-4ad9-9611-72941eef385a)

![setting up iis -43](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/097c083d-a1bf-4f2a-9c72-a02f4cf9c5b6)

![setting up iis -44](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/4e293269-6b16-4f12-a4ce-d27abcf2a894)

<br></br>

Download and install HeidiSQL. 

![setting up iis -48](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/35c594ea-47b4-468e-9766-ed34fc4dfbd2)

![setting up iis -49](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/63698bff-28fb-43c5-b9fc-e41d045e6a17)

![setting up iis -50](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/68534ab6-17e0-4d88-afc8-d3f21f74150a)

![setting up iis -51](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/47dc12f9-9c4d-4677-bc16-4d0787e82928)

![setting up iis -52](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/fc1b80be-994c-4c43-9924-85f9c7310d55)

![setting up iis -53](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/2e47d81a-1848-44d7-b2a2-4f768bdd4e91)


Create a new session with HeidiSQL and enter the password used in the installation of MySQL earlier and within the new session, right-click on Unnamed and create a new database named osTicket. 

![setting up iis -55](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/e2579227-206a-4e1b-9f4a-6b8718449432)

![setting up iis -56](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/9eb1e9d3-d240-46a7-bf10-b9e8e799aa61)

![setting up iis -57](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/89def1e4-3700-4844-96e2-a2c7c2132a9a)

![setting up iis -58](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/68d1e74d-b5e8-4f66-b270-bc15f95ddaab)

![setting up iis -59](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/914ad01e-eace-4161-857f-540248006c71)

<br></br>

Within osTicket browser window, enter the necessary details to set up osTicket. For the MySQL database, use the credentials used for MySQL and HeidiSQL. 

![setting up iis -60](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/68fd2d89-e96c-45c8-a18f-8555231f526c)

<br></br>

After everything is done, osTicket should now be installed! 

![setting up iis -61](https://github.com/Jacob-Oq/osticket-prereqs/assets/150084528/89875fc3-eb7a-4a72-b97b-aa65efd02d39)



Before continuing to use osTicket, delete the setup folder found in C:\inetpub\wwwroot\osTicket. Then, return to C:\inetpub\wwwroot\osTicket\include and change the permissions of the ost-config.php file. The file should no longer have full access to Everyone. Revert the permissions to "Read" only. 






