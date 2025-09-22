# How to Install Fedora KDE on your PC from scratch. - Drafting

## Creating Installation Media
**Step 1.** Open your browser and navigate to  https://fedoraproject.org/kde/download

**Step 2.** When on the page there is a toggle to download the Beta currently open at the time of this document creation you can chose to download the beta or chose to download the stable version. (Currently Stable is Fedora 42 / Beta is Fedora 43). Make sure to Download the ISO and the Fedora Media Writer.
<img width="1438" height="1289" alt="image" src="https://github.com/user-attachments/assets/16b71778-b545-4949-aa9d-7bcd76b53219" />

**Step 3.** Install the Media Writer on Windows. Note that you can also use Rufus or Balena Etcher as an alternative. Once you have installed the Media Writer Open it and Click Select .iso file. 
<img width="640" height="480" alt="image" src="https://github.com/user-attachments/assets/bf62470c-6250-49ff-8838-00e06cc48d81" />

**Step 4.** Burn the iso to your USB when done you are finished in Windows. Optionally you could also burn a secondary drive with a Windows 10 Install if you ever wish to go back. Once Complete reboot and move to prepare your Bios


## Prepare your Bios

**Step 1.** Navigate to your bios. Depending on your system, this could require you to press any of the following buttons while the system is starting up. [F2, F4, F8, F11, F12, Del, Backspace, Esc] Consult your Motherboards manual for information. 

**Step 2.** In the Bios, Disable the Following Items:
- Fast Boot: Fast Boot is a feature in computers and devices that allows for quicker startup times by saving the operating system's state to a hibernation file, enabling a faster boot process. It essentially keeps some components powered to avoid a full shutdown, which can speed up the launch time of your system.

- Secure Boot: Secure Boot is a security feature that ensures your PC only loads trusted software during startup, helping to protect against malware. It is usually recommended to turn off during Nvidia Graphic Driver install as there can be challenges due to the proprietary drivers. You can use secure boot if you wish however you will have to sign your own drivers. I would also note that sometimes Disabling Secure Boot may say Legacy instead of actually Disable either is fine.

**Step 3.** Adjust your boot order to boot from the USB Media you created before.   
  
