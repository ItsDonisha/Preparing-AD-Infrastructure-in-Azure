<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Preparing Activty Directory (Azure)</h1>

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

After creating the **resource group** and **virtual network**, we will set up two virtual machines: **DC-1** (Windows Server 2022) and **Client-1** (Windows 10). Both will be connected to the same **VNet** for communication.  

Once **DC-1** is created, we need to set its **private IP address** to static. In the **Azure Portal**, go to **DC-1 > Networking > Network Interface > IP Configurations**, then change the **Private IP Address** from **Dynamic** to **Static** and save the changes.  

Next, log in to **Client-1** using **Remote Desktop** and disable the **Windows Firewall**. Open the **Start Menu**, search for **Windows Defender Firewall**, and turn it **off** for both **Private** and **Public** networks.  

To check the connection, open **Command Prompt** on **Client-1** and ping **DC-1’s private IP address** using:  
```cmd
ping [DC-1 Private IP]
```  
If the ping is successful, open **PowerShell** and run:  
```powershell
ipconfig /all
```  
Make sure **DC-1’s private IP** appears as the **Primary DNS Server**. If everything checks out, the setup is complete, and the network is ready for **Active Directory** configuration.

<h2>Picture Data </h2>

![image](https://github.com/user-attachments/assets/04440e5b-4f88-44b1-b797-cb43e9b99ddc)

![image](https://github.com/user-attachments/assets/a40717e8-2589-4895-a10a-3798b1cf5c1d)

![image](https://github.com/user-attachments/assets/12deed06-10a3-4e73-a68b-a3df0ceda6db)

![image](https://github.com/user-attachments/assets/f4ee8709-f483-4f02-92b6-1020920dc140)

![image](https://github.com/user-attachments/assets/69f5dda8-a67a-4d55-a1aa-8935f9f9dde4)

![image](https://github.com/user-attachments/assets/af3e916e-28c8-4706-8526-f32ba13a30ee)

![image](https://github.com/user-attachments/assets/0fa8d805-cbcf-430f-b2a7-f1996ec28a96)

