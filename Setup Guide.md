# ESE519-lab2-SEtUP GUIDE
Chongyuan Zhang
https://www.linkedin.com/public-profile/settings?trk=d_flagship3_profile_self_view_public_profile
Test on: Lenovo Legion (R9000X), windows 11

## Setup Guide for SDK on Windows
In lab2, I will practice modeling my embedded systems based on the example from lecture 3. So I will firslty set up my laptop for RP2040 development using the official SDK(Softwawre Development Kit) for C/C++ programming.


The setup steps I followed is below:
## 1.Install the Toolchain
• Arm GNU Toolchain 

• CMake

• Build Tools for Visual Studio 2022

• Python 3.10

• Git

### 1)Arm GNU Toolchain
• Choose the filname ending with -arm-none-eabi.exe.
<img width="622" alt="a638aee6ec134e3daeefd8f1162b1b2" src="https://user-images.githubusercontent.com/114255407/195625445-60fb7e48-99a9-4af2-bd6a-474d7540d810.png">

• During installation, I tick the box to register the path to the Arm compiler as an environment variable in the Windows shell when prompted to do  so. 
<img width="375" alt="39c675ee062e1b5af89f1b03a5f8c35" src="https://user-images.githubusercontent.com/114255407/195626084-3f726495-fa1b-42ee-aedd-717471a8be1f.png">

### 2)CMake
• I downloaded the file 'cmake-3.24.2-windows-x86_64.msi' mentioned below.
<img width="556" alt="216013bd70e285c5c6ea523382e8053" src="https://user-images.githubusercontent.com/114255407/195626743-d3e69cc1-c018-4bd4-88a4-4632e115ddfd.png">

• During the installing, I add CMake to the system PATH for all users when prompted by the installer.
<img width="354" alt="d89116e82ac55e242544c2020192544" src="https://user-images.githubusercontent.com/114255407/195627616-5d9f118f-70fc-496e-9b68-ba3e06fd3e90.png">

• After that, I continued installation and accomplished.
<img width="356" alt="80ea19658fcc0c7d331ce0455a0291e" src="https://user-images.githubusercontent.com/114255407/195627962-6a47c568-6ca2-4655-8b98-22f459eec847.png">

### 3)Build Tools for Visual Studio 2022
• I install the C++ build tools.
<img width="942" alt="e4461f5799fe9f20207f2b0fcca8d1c" src="https://user-images.githubusercontent.com/114255407/195629724-1abeefb5-8d01-4629-bfff-ae8175f14f1c.png">


### 4)Python3.10
• I install Python 3.10.6(64-bit) "for all users", and choose "Add to Path" option.
<img width="498" alt="e583886f48e0698f4b8fe6f43c64f18" src="https://user-images.githubusercontent.com/114255407/195629928-b945d1f0-4058-43a5-8eb8-2af09ccda125.png">


### 5)Git
• I downloaded Git as the "64-bit Git for Windows Setup".
<img width="532" alt="eefa67935faa6e165f3438df299bfa3" src="https://user-images.githubusercontent.com/114255407/195631697-f3ed2b27-7a06-472b-93cb-230d8164794e.png">

• I chose Notepad as Git's default editor.
<img width="561" alt="cd20daef991dbf345b005cec807ba31" src="https://user-images.githubusercontent.com/114255407/195640289-e2ad8122-6855-4cda-a397-a5212b35dca8.png">

• Select "Checkout as is, commit as-is"
<img width="539" alt="d2946d77a6fe1c76447c21d76e98a69" src="https://user-images.githubusercontent.com/114255407/195639969-8953a433-4b7e-480d-a208-5cc4c3cc582c.png">

• Select "Use Windows' default console window"
<img width="566" alt="15c628c4178e0b903540691f3dabfb0" src="https://user-images.githubusercontent.com/114255407/195640020-bc7f4190-dd2d-4fac-b83e-e3c007a45eb5.png">

• Select "Enable experimental support for pseudo consoles"
<img width="563" alt="49c976dbc9d251af1c69bf6d86b7a6a" src="https://user-images.githubusercontent.com/114255407/195640062-0a8a229d-9c30-4dfe-ba8a-fe13570a8a11.png">

## 2.Getting the SDK and examples
I used the Powershell to executed the commands in the command line.
![image](https://user-images.githubusercontent.com/114255407/195643970-053aa4eb-5ce3-47b8-80f4-4dcb206d1fad.png)

## 3.Building "Hello World" from Visual Studio Code
•  I opened the VC Code via inputing 'code' at the "Developer Command Prompt for VS2022".
![image](https://user-images.githubusercontent.com/114255407/195644375-46f6e21d-cc8b-47a2-8c9c-3e90da8a5b05.png)

• I install the "CMake Tools" extension.  Click on the Extensions icon in the left-hand toolbar (or type Ctrl + Shift + X), and search for "CMake Tools" and click on the entry in the list, and then click on the install button.

• I select "Settings" and click on "Extensions" and then "CMake Tools". Then scroll down to "Cmake:
Configure Environment". Click on "Add Item" and set the PICO_SDK_PATH to be ..\..\pico-sdk
![image](https://user-images.githubusercontent.com/114255407/195647434-c892f5aa-3832-43c0-9bf0-5cbff919e799.png)

• And I scroll down to "Cmake: Generator" and enter "NMake Makefiles" into the box.
![image](https://user-images.githubusercontent.com/114255407/195648745-92be8ead-17d0-475c-b3ab-0d62b863e80c.png)

• Then I close the Settings page and go to the File menu and click on "Open Folder" and navigate to pico-examples repo and click "Select Folder"

<img width="232" alt="1665677508(1)" src="https://user-images.githubusercontent.com/114255407/195649630-577b6286-6371-4d99-8977-b98ddf27ba80.png">

• After thta, select "GCC for arm-none-eabi".
![image](https://user-images.githubusercontent.com/114255407/195650156-c3f9a9cd-8d16-47f7-b180-8423134c96cb.png)
 
## 4.Connect the RP2040
• Reset the RP2040: Keep both of the button presssed for a while.
  ![image](https://user-images.githubusercontent.com/114255407/195654405-919f99f5-2026-4a16-8fa8-fd762f265012.png)

• Drag and drop the 'hello_usb.uf2' U2F file into the drive.
![image](https://user-images.githubusercontent.com/114255407/195657289-8f80451d-8748-4387-b4d2-314b8b9caf09.png)

## 5.Install MobaXterm
• MobaXterm has the same function as Putty.

• Select "Serial", change the "Speed". Here the USB to UART Serial converter is on COM5.

• And see the result.
<img width="667" alt="c60126f676c4d6c2fa45099c2a5d718" src="https://user-images.githubusercontent.com/114255407/195656752-043ce496-84cb-401f-87db-de8a8be0feac.png">
