# How to Install Windows Server 2022 on VirtualBox

## Check for Virtualization


 **Using Task Manager**:
   - Go to `Start`, open `Task Manager`.
   - Look for `Virtualization` and ensure it says enabled.
![check Virtualization](https://github.com/user-attachments/assets/ecbf67c6-e2cf-401a-9f1f-39cf2afbffda)

## Download Windows Server 2022 ISO

- Go to [Microsoft's Download Page](https://www.microsoft.com/en-us/evalcenter/download-windows-server-2022?msockid=21a32a8c5fc66b5b1dff3fdd5ea96a8f).
- Select the ISO download for the 64-bit edition.
![download server 2022](https://github.com/user-attachments/assets/e80a6343-9d3b-474f-bc06-51c5b9c3f12c)

## Download VirtualBox

1. Go to the [VirtualBox Downloads Page](https://www.virtualbox.org/wiki/Downloads).
2. Under platform packages, select **Windows hosts**.
3. Once downloaded, go to your Downloads folder and double click `VirtualBox-7.1.4-165100-Win`.
4. A pop-up will appear asking, "Do you want to allow this app to make changes to your device?" Select **Yes**.
5. You will arrive at the "Welcome to the Oracle VirtualBox Setup Wizard", click **Next**.
6. At the End-User License Agreement screen, select "I accept the terms in the License Agreement", then click **Next**.
7. At the Custom Setup screen, click **Next**. If you see a warning about Network Interfaces, click **Yes**.
8. At the Missing Dependencies (Python Core/Win32api), click **Yes**.
9. At the next screen, leave it at the default and click **Next**.
10. At the Ready to Install screen, click **Install**.
11. Lastly, you will see a message that "Oracle VirtualBox 7.1.4 installation is complete". Click **Finish**.
![installing VB](https://github.com/user-attachments/assets/d4a76465-a928-421d-b019-199846310b53)

## Create a New Virtual Machine

1. Once VirtualBox opens, click **New**. A screen titled "Create Virtual Machine" should appear.
2. At the name input, name it.
3. Under ISO Image, click the down arrow and select **Other**. Go to your Downloads folder and choose the `SERVER_EVAL_x64FRE_en-us.iso`, then click **Open**.
4. Select **Skip Unattended Installation** (this skips setting up an Unattended Guest), then click **Next**.
5. At the hardware window, allocate resources to your VM:
   - **RAM**: To check how much RAM your system has, click `Start > Settings icon > About`. The RAM size is displayed under Installed RAM.
   - **Processors**: To check how many processors your system has, click `Start > System > Task Manager`. Under the Performance tab, select CPU, and it will show the number of cores.
![adding ram and cores](https://github.com/user-attachments/assets/b4e292a5-fa68-4dbf-a770-f19bb23cab38)

6. Stay within the green zone when sharing your system's RAM and processors.

   - **Virtual Hard Disk**: At the Virtual Hard Disk window:
   To check how much free space your hard drive has, select `Start > Settings > Storage`. Under Local Disk, you will see the available free space.
   
2. Allocate as much space as you need but avoid exceeding half of your physical hard drive's capacity.
3. You will reach the Summary screen. Review your selections, and if satisfied, click **Finish**.
![adding harddrive and finalizing vm install](https://github.com/user-attachments/assets/29708f85-23e8-49a0-9766-97cb001445b0)

## Starting the Server

1. Select **Start**. You will see the Microsoft Server Operating System Setup. Click **Next**, then click **Install Now**.
2. At the next window, select the OS option: **Windows Server 2023 Standard Evaluation (Desktop Experience)**, then click **Next**.
3. Accept the license terms and click **Next**.
4. When asked, "Which type of installation do you want?", select **Custom** (since we are not updating).
5. Click **Next** when prompted to select the installation drive (it will select the only available drive).
6. The installation will begin.
7. Once done, Windows will restart.
![completing server installation](https://github.com/user-attachments/assets/e9815292-1ae7-4c40-bdad-196e5983febc)

## Completing the Installation

1. You will be prompted to set a password for the admin. Enter a password.
2. Press `Ctrl+Alt+Delete` to unlock. In VirtualBox, go to `Input > Keyboard > Insert Ctrl+Alt+Delete`.
3. Log in using the admin credentials.

Congratulations! You have successfully installed Windows Server 2022 on VirtualBox.
