# Notes: Remote Access

# Windows to Linux Server

## WinSCP

### Prerequisites

1) WinSCP-5.9.6-Setup.exe (in Windows machine)

2) OpenSSH-Server (in Linux machine)

> sudo apt-get install openssh-server

### Steps

1) Login

<img src="https://github.com/usbong/ITAMS/blob/main/Notes/RemoteAccess/20231019/winscpWinToLinuxLoginV20231019T1523.png" width="80%">

2) Edited -> Advanced -> Advanced Site Settings

<img src="https://github.com/usbong/ITAMS/blob/main/Notes/RemoteAccess/20231019/winscpWinToLinuxAdvancedSiteSettingsV20231019.png" width="80%">

3) Login -> Warning

<img src="https://github.com/usbong/ITAMS/blob/main/Notes/RemoteAccess/20231019/winscpWinToLinuxConnectAfterInstallingOpenSSHServerInLinuxV20231019T1433.png" width="80%">

4) Example Output

<img src="https://github.com/usbong/ITAMS/blob/main/Notes/RemoteAccess/20231020/winscpWinToLinuxConnectOutputV20231020T1119.png" width="100%">

DONE!

## Putty

### Prerequisites

1) putty-64bit-0.70-installer (in Windows machine)

2) OpenSSH-Server (in Linux machine)

> sudo apt-get install openssh-server

### Steps

1) Warning

<img src="https://github.com/usbong/ITAMS/blob/main/Notes/RemoteAccess/20231019/puttyWinToLinuxConnectAfterInstallingOpenSSHServerInLinuxV20231019T1535.png" width="80%">


2) Login

<img src="https://github.com/usbong/ITAMS/blob/main/Notes/RemoteAccess/20231019/puttyWinToLinuxLoginV20231019T1536.png" width="100%">


DONE!

# Windows to Windows Server

## Remote Desktop Connection

### Prerequisites

1) Turn ON

<img src="https://github.com/usbong/ITAMS/blob/main/Notes/RemoteAccess/Windows/remoteDesktopWinToWinRemoteDesktopOnV20231020T1402.png" width="80%">

### Steps

1) Login

<img src="https://github.com/usbong/ITAMS/blob/main/Notes/RemoteAccess/Windows/remoteDesktopWinToWinLoginV20231020T1432.png" width="80%">

2) Warning

<img src="https://github.com/usbong/ITAMS/blob/main/Notes/RemoteAccess/Windows/remoteDesktopWinToWinWarningV20231020T1401.png" width="80%">


3) Example Output

<img src="https://github.com/usbong/ITAMS/blob/main/Notes/RemoteAccess/Windows/remoteDesktopWinToWinRemoteDesktopOutputV20231020T1431.png" width="100%">

# Linux to Linux Server

### Prerequisites

1) OpenSSH Server in target Linux Server

<img src="https://github.com/usbong/ITAMS/blob/main/Notes/RemoteAccess/Linux/usbongRemoteAccessSSHLinuxToLinuxInstalOpenSSHServerInTargetV20231209T0921.jpg" width="100%">

2) OpenSSH Client

### Step

1) Login (to Linux Server with IP Address 192.168.10.99)

Enter the following COMMAND in the Terminal Window:

`ssh 192.168.10.99`
