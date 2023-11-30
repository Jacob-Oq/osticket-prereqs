<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

 https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Item 1
- Item 2
- Item 3
- Item 4
- Item 5

<h2>Installation Steps</h2>

Before installing any files, be sure to have Internet Information Services (IIS) enabled. OsTicket will be installed locally and it needs IIS in order to function. To turn on IIS, open the Control Panel. 

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


<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
