# LUBUNTU 20.04LTS Operating System (OS)
## 1) Problem: Pressing POWER ON Button does NOT cause OS to START
--> <b>Additional Note:</b> No excess SOUND heard due to Random Access Memory (RAM) Card NOT correctly connected<br/> 

### Solution: 
Disconnect POWER and DATA Cables from the Harddisk Storage; Reconnect. Press POWER ON.

## 2) Problem: No "1280x1024" Resolution in Monitor Settings

<img src="https://github.com/usbong/ITAMS/blob/main/Notes/res/computerMonitorResolution1280x1024Notification20220710T1257.jpg" width="60%">

--> <b>Additional Note:</b> added: recycled NVIDIA Inno3D Graphics Acceleration Card (1GB) to Motherboard (Amd64 System Processor)

<img src="https://github.com/usbong/ITAMS/blob/main/Notes/res/am64CPUMotherboard20220710T1332.jpg" width="30%">

<img src="https://github.com/usbong/ITAMS/blob/main/Notes/res/NVIDAInno3DAcceCard20220710T1333.jpg" width="30%">

<img src="https://github.com/usbong/ITAMS/blob/main/Notes/res/NVIDAInno3DAcceCardInsertedToMotherboard20220710T1337.jpg" width="30%">


### Solution (Part 1): 

#### Step 1.1: Execute the following COMMANDS in Terminal Window
COMMAND#1:<br/> 
<b>xrandr --newmode "1280x1024_60.00"  109.00 1280 1368 1496 1712  1024 1027 1034 1063 -hsync +vsync</b> <br/>
<br/>
COMMAND#2: <b>xrandr --addmode VGA-1 1280x1024_60.00 </b><br/> 
<br/>
COMMAND#3: <b>xrandr --output VGA-1 --mode 1280x1024_60.00 </b><br/> 
<br/>
COMMAND#4: <b>sudo featherpad /usr/share/X11/xorg.conf.d/10-monitor.conf</b><br/> 

#### Step 1.2: <b>Copy-paste the following; SAVE file</b>

> Section "Monitor"<br/> 
> Identifier "Monitor0"<br/> 
>  Modeline "1280x1024_60.00"  109.00  1280 1368 1496 1712  1024 1027 1034 1063 -hsync +vsync<br/> 
> EndSection<br/> 
> Section "Screen"<br/> 
>  Identifier "Screen0"<br/> 
>  Device "VGA1"<br/> 
>  Monitor "Monitor0"<br/> 
>  DefaultDepth 24<br/> 
>  SubSection "Display"<br/> 
>    Depth 24<br/> 
>    Modes "1280x1024_60.00" "1024x768" "800x600"<br/> 
>  EndSubSection<br/> 
> EndSection

#### Step 3: <b>Reboot Operating System</b>

<img src="https://github.com/usbong/ITAMS/blob/main/Notes/res/computerMonitorResolutionSettingInLinuxUbuntuSoftwareOK20220710T1354.jpg" width="60%">

DONE!

### References
1) https://askubuntu.com/questions/235207/max-resolution-available-is-1024x768-while-i-should-expect-1280x1024; last accessed: 20220710<br/>
--> answer by: gertvdijk, 20130103T0957<br/>
--> edited by: CommunityBot, 20170413T1223<br/>

2) https://askubuntu.com/questions/316221/resolution-hd-1920x1280-with-intel-graphics-in-ubuntu-12-04-lts; last accessed: 20220710<br/>
--> answer by: Lisa, 20140304T1224<br/>
--> edited by: David Edwards, 20140304T1310<br/>

### Solution (Part 2): 

<b>SPEC:</b> NVIDIA Inno3D Graphics Acceleration Card (1GB): GeForce  210

#### Objective
Install NVIDIA Card Machine Driver<br/>
<br/>
where: Driver : Software (set of computer instructions classified to be with 人工知能 (AI; Artificial Intelligence));<br/>
where: AI :  may Taong Pinabilis ang Kaalaman at Kakayahan

#### Step 2.1: Execute the following COMMANDS in Terminal Window

> sudo add-apt-repository ppa:kelebek333/nvidia-legacy<br/>
> sudo apt-get update<br/>
> sudo apt install nvidia-340 xorg-modulepath-fix 

### Reference
1) https://askubuntu.com/questions/1365396/ubuntu-21-04-no-proprietary-nvidia-driver-for-geforce-210-graphics-card; last accessed: 20220717<br/>
--> answer by: N0rbert, 20210923T1837



## 3) Problem: No Japanese Language (日本語) Input

### Solution:

#### Part3.1) Execute the following COMMANDS in Terminal Window:<br/>

<b>
sudo apt-get install gnome-control-center <br/>

sudo gnome-control-center region
</b> 

#### Part3.2) Region & Language -> Managed Installed Languages<br/>

<img src="https://github.com/usbong/ITAMS/blob/main/Notes/res/lubuntu20Dot04JapaneseLanguageSupportV20230104T0951.jpg" width="60%"><br/>

--> Step1) Install/Remove Languages -> Japanese<br/>
--> Step2) Keyboard input method system: `fcitx`<br/>
--> Step3) Close<br/>

--> Step4) Input Sources -> + -> Add -> Japanese<br/>
--> Step5) Close via "X" Mark<br/>
<br/>
--> Step6) Logout -> Login<br/>

#### Part3.3) Click KEYBOARD icon @BOTTOM-RIGHT of screen to change it into GEAR icon;<br/>
--> notes: OUTPUT is equal with CTRL + SPACEBAR INPUT COMMAND<br/>

よくできました。

--> reminder: KEYBOARD icon causes INPUT to be the default, e.g. Filipino 

DONE!

### References
1) https://askubuntu.com/questions/1266905/why-is-region-and-language-missing-from-the-gnome-control-center; last accessed: 20230103<br/>
--> answer by: rubicks, 20200813T2035<br/>
--> question by: rubicks, 20200813T1537<br/>

2) https://askubuntu.com/questions/316221/resolution-hd-1920x1280-with-intel-graphics-in-ubuntu-12-04-lts; last accessed: 20230103


