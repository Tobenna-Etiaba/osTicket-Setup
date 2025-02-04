<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

# <h1>osTicket-Setup</h1>
I will be outlining how I was able to set up osTicket.


# <h2>Tools Used</h2>
 - Microsoft Azure
 - Remote Desktop
 - Internet Information Services

# <h2>Operating Systems Used</h2>
 - Windows 10 Pro (22H2)

# <h2>Step By Step Process</h2>
- I started by creating a Windows 10 virtual machine in Azure with 2vcpus & 8GB of memory
<img width="357" alt="Screenshot 2025-02-03 at 21 01 17" src="https://github.com/user-attachments/assets/aab7990e-3778-498f-bcb1-751ad5b30886" />

- From there I used remote desktop to access the virtual machine created in Azure.
<img width="1148" alt="Screenshot 2025-02-03 at 21 10 05" src="https://github.com/user-attachments/assets/9430e270-634a-474a-a03e-5e27920a1c03" />

- After downloading the osTicket setup folder I typed my VMs loopback address and got the error below due to IIS(Internet Information Services) not being enabled so I proceeded to do so via CGI (Common Gateway Interface)
<img width="1123" alt="Screenshot 2025-02-03 at 21 20 50" src="https://github.com/user-attachments/assets/b44b19a9-6525-4b01-bba1-1bdf4ec04f62" />

<img width="413" alt="Screenshot 2025-02-03 at 21 21 12" src="https://github.com/user-attachments/assets/c58ad520-3e4a-4f2f-95d7-70bca56783dc" />

<img width="425" alt="Screenshot 2025-02-03 at 21 22 12" src="https://github.com/user-attachments/assets/f758dee0-c25e-4565-a40a-d4d7eb388f74" />

<img width="1726" alt="Screenshot 2025-02-03 at 21 24 14" src="https://github.com/user-attachments/assets/714b4ca4-c119-4af0-b331-65fc10596f34" />

- Once that was sorted out there were several things from the osTicket installation folder that needed to be installed such as PHP Manager, and Rewrite Module.
<img width="498" alt="Screenshot 2025-02-03 at 21 24 48" src="https://github.com/user-attachments/assets/76b165cd-6ed8-4ecb-b867-0179becda4c0" />

<img width="494" alt="Screenshot 2025-02-03 at 21 25 10" src="https://github.com/user-attachments/assets/b863f47a-369e-4130-a3f0-2f323344b09a" />


