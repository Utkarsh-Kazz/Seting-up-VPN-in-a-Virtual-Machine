# Seting-up-VPN-in-a-Virtual-Machine
<p align="center">
<img src="https://i.imgur.com/MntON5Q.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<h1>VPN - Prerequisites and Installation</h1>
This guide walks through the essential requirements and installation process for using a VPN.<br />

<h2>Environments and Technologies Used</h2>

- A VPN Service (Proton VPN)
- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop connection
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>STEPS INCLUDED</h2>

- STEP 1 - Check Local IP Address
- STEP 2 - Deploy a Virtual Machine on Azure
- STEP 3 - Get Public IP from Inside the VM
- STEP 4 - Connect to a VPN from the VM
- STEP 5 - View VPN IP from New Location

<h2>Installation Steps</h2>

STEP 1 - Check Your Local IP Address.
To begin, open a web browser on your local computer and visit “www.whatismyipaddress.com.” This site will display your current public IP. Take note of it for comparison later.
<p>
<img src="https://i.imgur.com/qDgu5K6.png)" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Set Up a Virtual Machine Using Azure  
</p>
<br />
Next, go to www.portal.azure.com and search for "Virtual Machines." If you're new, you can sign up and receive $200 in free credits.
Refer to EXAMPLE 2A for the Virtual Machine setup page.
<p>
<img src="https://i.imgur.com/K9oaS2z.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
During VM setup, name the machine “VM-FranceCentral” and choose France Central as the region. Make sure your configuration matches the settings above.
<p>
<img src="https://i.imgur.com/u3vclL3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
You can enter a custom username and password here. Make sure to save these details for later use.  
</p>
<br />
<p>
<img src="https://i.imgur.com/rXIj3Zb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Click the “Networking” tab at the top of the page and match your configuration with what is shown below 
  
</p>
<br />
<p>
<img src="https://i.imgur.com/OgYgNLK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After completing the configuration, select “Review + Create.” Once validated, click “Create” to launch the VM.

Once the deployment is done, go to the VM overview page. You’ll find the public IP assigned to the machine — e.g., “20.216.176.18”
</p>
<br />
<p>
<img src="https://i.imgur.com/ZlH9zI5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Log Into VM and Identify Its Public IP
<p>
Now that your VM is up and running, open Remote Desktop Connection on your PC.
Use the VM’s IP from EXAMPLE 2E and input the login credentials created earlier.

Once you’re logged in, open a browser within the VM and visit www.whatismyipaddress.com again.
You’ll see the VM is accessing the internet from France. 
</p>
<br />
<p>
<img src="https://i.imgur.com/YPBkMau.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
<p>
<img src="https://i.imgur.com/oPJr2w2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
When we look up the IP address for this VM through www.whatismyipaddress.com we see that this VM is showing the location for France.
</p>
<br />
<p>
<img src="https://i.imgur.com/nWlX2UM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Connect to VPN from Inside the VM

On your local computer, go to protonvpn.com and register for a free account.
(Note: Avoid using the VM browser for this step as the website may appear in French.)

After registering, copy the ProtonVPN link and paste it into the browser on the VM.
</p>
<br />
<p>
<img src="https://i.imgur.com/orO2O5y.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Once logged into ProtonVPN inside the VM, go to the Downloads section and install the Windows version of the app.
After installation, open ProtonVPN and log in with the same credentials used earlier.
Then, connect to a server of your choice — in this case, Japan.  
</p>
<br />
<p>
<img src="https://i.imgur.com/oqPHozb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
From the left panel in ProtonVPN, select the country you want to connect through.
The screenshot below shows a successful connection to a Japanese IP.  
</p>
<br />
<p>
<img src="https://i.imgur.com/6Rdgg6B.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
With VPN now active, go back to www.whatismyipaddress.com in the VM browser to confirm the new IP location.
You should now see a different IP, reflecting your Japan-based VPN connection.
</p>
<br />
<p>
<img src="https://i.imgur.com/lQsISWb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
By the end of this setup, you will have observed and used three different IP addresses:

Home IP (USA) – e.g., 137.103.51.136

VM Public IP (France) – e.g., 20.216.176.18

VPN IP (Japan) – e.g., 212.102.51.251 
</p>
<br />
If you're done using the Virtual Machine, don't forget to delete it from your Azure dashboard to avoid ongoing charges.

END OF TUTORIAL
