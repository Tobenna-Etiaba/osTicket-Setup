<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket-Setup</h1>
I will be outlining how I was able to set up osTicket.


<h2>Tools Used</h2>

- Microsoft Azure

- Remote Desktop

- Internet Information Services

<h2>Operating Systems Used</h2>
 - Windows 10 Pro (22H2)

<h2>Step By Step Process</h2>
- I started by creating a Windows 10 virtual machine in Azure with 2vcpus & 8GB of memory to ensure that the VM ran a reasonable speed.
<img width="357" alt="Screenshot 2025-02-03 at 21 01 17" src="https://github.com/user-attachments/assets/aab7990e-3778-498f-bcb1-751ad5b30886" />

- From there I used remote desktop to access the virtual machine created in Azure.
<img width="1148" alt="Screenshot 2025-02-03 at 21 10 05" src="https://github.com/user-attachments/assets/9430e270-634a-474a-a03e-5e27920a1c03" />

- After downloading the osTicket setup folder I typed my VMs loopback address and got the error below due to IIS(Internet Information Services) not being enabled so I proceeded to do so via CGI (Common Gateway Interface)
<img width="835" alt="Screenshot 2025-02-03 at 21 20 24" src="https://github.com/user-attachments/assets/77427f60-f2fa-4635-9dcb-ab711b9c9aee" />

<img width="1123" alt="Screenshot 2025-02-03 at 21 20 50" src="https://github.com/user-attachments/assets/b44b19a9-6525-4b01-bba1-1bdf4ec04f62" />

<img width="413" alt="Screenshot 2025-02-03 at 21 21 12" src="https://github.com/user-attachments/assets/c58ad520-3e4a-4f2f-95d7-70bca56783dc" />

<img width="425" alt="Screenshot 2025-02-03 at 21 22 12" src="https://github.com/user-attachments/assets/f758dee0-c25e-4565-a40a-d4d7eb388f74" />

<img width="1726" alt="Screenshot 2025-02-03 at 21 24 14" src="https://github.com/user-attachments/assets/714b4ca4-c119-4af0-b331-65fc10596f34" />

- Once that was sorted out there were several things from the osTicket installation folder that needed to be installed such as PHP Manager, and Rewrite Module.
<img width="498" alt="Screenshot 2025-02-03 at 21 24 48" src="https://github.com/user-attachments/assets/76b165cd-6ed8-4ecb-b867-0179becda4c0" />

<img width="494" alt="Screenshot 2025-02-03 at 21 25 10" src="https://github.com/user-attachments/assets/b863f47a-369e-4130-a3f0-2f323344b09a" />

- I proceeded to go to the c:\ drive section of the VM and create a new folder called PHP and from there, I went back into the osTicket setup folder and extracted the PHP zip file into the PHP folder.
<img width="659" alt="Screenshot 2025-02-03 at 21 25 48" src="https://github.com/user-attachments/assets/e8120653-0ebd-4ae6-a491-a2820d627abd" />

<img width="576" alt="Screenshot 2025-02-04 at 03 21 50" src="https://github.com/user-attachments/assets/b19a76b3-6999-4c65-b89e-7664d141ffd8" />

<img width="606" alt="Screenshot 2025-02-03 at 21 26 23" src="https://github.com/user-attachments/assets/53939dea-7b6a-49cc-84e7-0862f22ff358" />

- Following from there I proceeded to install Microsoft Visual C++ Redistributable (2015) and MySQL
<img width="481" alt="Screenshot 2025-02-03 at 21 27 26" src="https://github.com/user-attachments/assets/356ecb19-e33d-40ae-b649-9ae63dca00e3" />

<img width="494" alt="Screenshot 2025-02-03 at 21 28 03" src="https://github.com/user-attachments/assets/32fbd601-717b-495e-8afe-90f438f8749d" />

- Most of the things in the osTicket setup folder had been installed however some somethings needed to be done before everything could be installed, one of them involved registering PHP, which I did via IIS as an administrator.
<img width="747" alt="Screenshot 2025-02-03 at 21 29 51" src="https://github.com/user-attachments/assets/6f2ce7db-95c2-4b51-a4c7-527320e814d4" />
 
<img width="1279" alt="Screenshot 2025-02-03 at 21 30 42" src="https://github.com/user-attachments/assets/7f32965a-24fc-42cd-a366-45228cd693bd" />

<img width="1099" alt="Screenshot 2025-02-04 at 03 27 44" src="https://github.com/user-attachments/assets/a2f8771a-8fe1-4875-b209-a9ae4deb9687" />

- I followed up by extracting the osTicket zip folder and from that folder there was another within called upload which was then cut and pasted to c:\inetpub\wwwroot and renamed to osTicket.
<img width="749" alt="Screenshot 2025-02-03 at 21 34 53" src="https://github.com/user-attachments/assets/eab9f4f7-9513-4a23-aae2-03e2ddc88b35" />

<img width="641" alt="Screenshot 2025-02-03 at 21 35 04" src="https://github.com/user-attachments/assets/65316118-567b-4138-bcad-b90a4769a4c8" />

<img width="799" alt="Screenshot 2025-02-03 at 21 35 58" src="https://github.com/user-attachments/assets/9f298780-3dcb-448b-952b-17a072a6f775" />

- Within the pasted folder there was a file called "ost-sampleconfig.php" which I renamed to "ost-config.php", and from there I disabled inheritance and assigned new permissions.
<img width="944" alt="Screenshot 2025-02-03 at 21 36 17" src="https://github.com/user-attachments/assets/71e9a60e-a7dd-444b-8615-a1efbc0c3be2" />

<img width="1389" alt="Screenshot 2025-02-03 at 21 37 18" src="https://github.com/user-attachments/assets/fadfe088-ba29-4b39-b7cd-1f029bfa9e29" />

<img width="1274" alt="Screenshot 2025-02-03 at 21 38 08" src="https://github.com/user-attachments/assets/13e0a9ab-92f9-454c-b84d-762d1da30ed1" />

<img width="916" alt="Screenshot 2025-02-03 at 21 38 27" src="https://github.com/user-attachments/assets/5ee55162-a641-4b29-9864-245347b097ff" />

<img width="766" alt="Screenshot 2025-02-03 at 21 38 45" src="https://github.com/user-attachments/assets/0e5348a9-ce51-4743-b8d5-9626754a9ed1" />

<img width="1140" alt="Screenshot 2025-02-03 at 21 39 29" src="https://github.com/user-attachments/assets/5c04a115-0227-4651-a691-04a279e744d1" />

<img width="1718" alt="Screenshot 2025-02-03 at 21 39 42" src="https://github.com/user-attachments/assets/6305d9fb-8f31-4196-9d29-6580e7bbc458" />

- There were some extensions (php_imap.dll, php_intl.dll, php_opcache.dll) that needed to be enabled before installation process could continue.
<img width="501" alt="Screenshot 2025-02-03 at 21 40 07" src="https://github.com/user-attachments/assets/adf8d296-3141-4a3b-93c6-1878344e9593" />

<img width="1139" alt="Screenshot 2025-02-03 at 21 40 33" src="https://github.com/user-attachments/assets/1f37fd5c-a246-40a9-b586-ca9fedc12edf" />

- After that there were just a few things left to sort which were, installing Heidi SQL which was the last component in the setup folder, and creating a new database.
<img width="1689" alt="Screenshot 2025-02-03 at 21 41 24" src="https://github.com/user-attachments/assets/625eb7af-d5ba-4a33-a611-ef08a1b31a2d" />

<img width="1129" alt="Screenshot 2025-02-03 at 21 46 13" src="https://github.com/user-attachments/assets/ac74d5e4-38d2-4920-9b0a-36595fcbf9e2" />

<img width="683" alt="Screenshot 2025-02-03 at 21 47 08" src="https://github.com/user-attachments/assets/96dbf1de-6089-4297-bac3-27348b6ca37e" />

<img width="934" alt="Screenshot 2025-02-03 at 22 16 14" src="https://github.com/user-attachments/assets/7118895f-ac11-4a1f-abaf-59825601d9bb" />

<img width="452" alt="Screenshot 2025-02-03 at 22 16 27" src="https://github.com/user-attachments/assets/5e9d53a7-eef9-4a1d-9c40-e483291468ab" />

- And with this the installation could now be finalised.
<img width="830" alt="Screenshot 2025-02-03 at 22 16 52" src="https://github.com/user-attachments/assets/d55dbb9e-34c8-4e64-95b8-b860a97eb29d" />

<img width="1472" alt="Screenshot 2025-02-03 at 22 17 12" src="https://github.com/user-attachments/assets/e7a153d3-99f7-4e83-99bb-6f3d339dc959" />

- And with this osTicket had been successfully installed.
<img width="1277" alt="Screenshot 2025-02-04 at 03 48 33" src="https://github.com/user-attachments/assets/e5f950e1-29eb-48ac-9ec2-18f7d36851cd" />
