# Nvidia Drivers Setup on Fedora 42/43

## Pre-Driver Install Steps
**Step 1.** Open Konsole

<img width="674" height="584" alt="image" src="https://github.com/user-attachments/assets/a15aa173-37e7-4fc9-ac0e-ae8f1c9984d5" />

**Step 2.** Enter the following in Konsole
```bash
sudo dnf update --refresh
```

<img width="949" height="618" alt="image" src="https://github.com/user-attachments/assets/8954a4c9-8868-4e5a-935d-7e58314fc431" />

**Step 3.** Type in your password. 
<img width="954" height="622" alt="image" src="https://github.com/user-attachments/assets/f560caa3-c5bf-4def-a93e-04ba865182c3" />

**Step 4.** You will get a list of everything it will install.. once it asks. Press y and Enter to start the process
<img width="981" height="668" alt="image" src="https://github.com/user-attachments/assets/2a8daff0-ed7f-46a7-a725-9544e874109e" />

**Step5.** You may be prompted to add keys to your OpenPGP this is normal, just press y and enter anytime this happens.  
<img width="921" height="594" alt="image" src="https://github.com/user-attachments/assets/eb7ff9de-8e30-40f4-b2c2-67944accc403" />


**Step 6.** You should see that this is done. It will say complete, and show the command prompt again. 
<img width="943" height="640" alt="image" src="https://github.com/user-attachments/assets/ee116faa-513a-4281-ae0c-18453e052858" />

**Step 7.** You can reboot at this point to refresh your system. Type the below in the Konsole.
```bash
reboot
```

Once the system has rebooted move on to step 8.

------Reboot----------

**Step 8.** Open Welcome Center. Open the Start Menu and type in Welcome and click Welcome Center
<img width="676" height="572" alt="image" src="https://github.com/user-attachments/assets/bc8d3686-72ac-41e9-8422-65626616f461" />

This screen should pop-up

<img width="659" height="613" alt="image" src="https://github.com/user-attachments/assets/12540e69-37f0-4ae0-b291-5c256be0fcbb" />

**Step 9.** Click Next on the screen till you get to the 3rd Party Repos. Click the button to ENABLE THIRD PARTY REPOS
<img width="702" height="667" alt="image" src="https://github.com/user-attachments/assets/c8e9ac6c-1b82-413e-8ebb-931b25631f01" />

**Step 10.** Enter your password.

<img width="769" height="688" alt="image" src="https://github.com/user-attachments/assets/3c218012-6212-4da3-8fd0-7e3bfe98289c" />

**Step 11.** Click Next and Finish to close the window
<img width="711" height="674" alt="image" src="https://github.com/user-attachments/assets/e62e1174-74cc-4a4e-8354-499b5c5a88df" />

## Setting Up RPM Fusion
### RPM Fusion is a third party repository for proprietary software, like STEAM, DISCORD, and NVIDIA Drivers.

**Step 12.** Ok, open Konsole, and open Firefox. Navigate to RPMFusion.org
<img width="1826" height="1256" alt="image" src="https://github.com/user-attachments/assets/ca967449-de4a-424f-9518-4f9715efcdda" />

**Step 13.** Click on Enable RPM Fusion on your system link 
<img width="793" height="530" alt="image" src="https://github.com/user-attachments/assets/88f5746c-20cf-4288-992c-7dd2660fc044" />

**Step 14.** You will scroll down to Command Line Setup using rpm. You will find a line to enter into Konsole. 

<img width="2154" height="309" alt="image" src="https://github.com/user-attachments/assets/c00725fa-6936-481b-adef-1dae36965f59" />

Copy* and Paste* it into Konsole and press ENTER:
```bash
sudo dnf install https://mirrors.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm https://mirrors.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm
```
*Note that in Linux Copy and Paste CONTROL+C works in all places but the terminal. To paste into terminal you have to hit CONTROL+SHIFT+V not Control+V as it will create an error. Also if you ever needed to copy from the terminal you would hit CONTROL+SHIFT+C

<img width="1056" height="770" alt="image" src="https://github.com/user-attachments/assets/913939e7-f52e-4aec-b6d9-e478078c542c" />

**Step 15.** Enter your password and hit ENTER"
<img width="1083" height="781" alt="image" src="https://github.com/user-attachments/assets/ec7c8016-4bd9-495a-83d2-a28222a16e9d" />

**Step 16.** Review that its adding the two repositories and press y and ENTER:
<img width="1109" height="870" alt="image" src="https://github.com/user-attachments/assets/f3e01ecd-901f-4fad-a5e7-9547e0cc999b" />

Should say Complete! when done, and show the command prompt
<img width="1002" height="804" alt="image" src="https://github.com/user-attachments/assets/8419c983-fc97-4d65-8282-42d1bbb7bf0c" />

## Setting Up Nvidia Driver

**Step 17.** Scroll up the RPM Fusion page to Howto and click it. 
<img width="874" height="446" alt="image" src="https://github.com/user-attachments/assets/4da40e1d-3dec-411e-ba57-96bde5af2982" />


**Step 18.** Click on Howto/NVIDIA. This will contain instructions for NVIDIA Cards from long ago and other versions of Fedora. 
<img width="661" height="689" alt="image" src="https://github.com/user-attachments/assets/40c5764a-825f-43fa-a795-7f01828b46d5" />


**Step 19.** Your Card is like made in the last 10 years you are probably on the Current Geforce Section of the page. You will find instructions here to enter. You have already done the update earlier in this process so you can ignore the: 
```bash
sudo dnf update -y
```
As you already did it. 

<img width="1203" height="385" alt="image" src="https://github.com/user-attachments/assets/2c54a8a4-0776-4364-be40-7e791fead21a" />


**Step 20.** You should enter the next line though of the RPM Fusion Instructions:
```bash
sudo dnf install akmod-nvidia
```
This is the actual driver.

You can also install:
```bash
sudo dnf install xorg-x11-drv-nvidia-cuda
```
However this is OPTIONAL. It is used for AI Processes. If unsure you should install both by combining the commands like this:
```bash
sudo dnf install akmod-nvidia xorg-x11-drv-nvidia-cuda
```
<img width="786" height="165" alt="image" src="https://github.com/user-attachments/assets/9e389f26-d325-42ff-98fa-0d6192146688" />

**Step 21.** You will be prompted for your password and asked if its ok to install the packages obviously type y and ENTER till its completed
<img width="786" height="165" alt="image" src="https://github.com/user-attachments/assets/65237066-9e2c-4d43-92be-cbb7a87f6d21" />

**Step 22.** When the install is complete. **DO NOT REBOOT OR TURN OFF POWER**. Go to Konsole and type:
```bash
sudo dnf install btop
```
This will install a program to monitor the system called BTOP.
<img width="786" height="165" alt="image" src="https://github.com/user-attachments/assets/135594e8-bb50-490d-851f-5f00957e254f" />

**Step 23.** Once installed type btop in consol to run it. 
```bash
btop
```
Should look like this:
<img width="2559" height="1318" alt="image" src="https://github.com/user-attachments/assets/77f0543e-c851-454f-8e92-9bd76ad529b1" />

Step 24. After a nvidia install, or a Kernel update. You should always look at btop. 
<img width="1416" height="1229" alt="image" src="https://github.com/user-attachments/assets/801932d1-eb16-4e98-a14f-060fa95327ea" />
**If you see the CPU being used heavily, and a process where the user is AKMOD, running do not REBOOT till it is completed. Once you no longer see the AKMOD programs running and the CPU is idle, then it is safe to reboot. If you reboot before hand or lose power you will screw up the driver completion.**

**Step 25.** If everything is good in btop. You can press Q to quit and type:
```bash
reboot
```
Into the Konsole to restart the PC. If you did it correct you should return to the desktop. 



