#Enable Linux subsystem in service windows.

https://techcommunity.microsoft.com/t5/windows-11/how-to-install-the-linux-windows-subsystem-in-windows-11/m-p/2701207

#install kali Linux from Microsoft store.

https://albany.atlassian.net/wiki/spaces/askit/pages/52366312/Install+Kali+Linux+from+the+Microsoft+Store

PowerShell commands to fix the issues:

wsl --update

dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart

dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart

wsl --set-default-version 2

dism.exe /online /enable-feature /featurename:Microsoft-Hyper-V-All /all /norestart

#reboot the system

then open kali and set username and password.

#update the kali Linux

sudo apt-get update -y

sudo apt-get upgrade -y

sudo apt-get dist-upgrade -y

#installing kali all tools

sudo apt-get install kali-defaults
sudo apt-get install kali-linux-large
sudo apt-get install --reinstall kali-menu
sudo apt-get install -y kali-desktop-gnome


#enable RDP 

sudo apt install -y xrdp

sudo apt-get install dbus-x11

echo "gnome-session" > ~/.xsession

sudo systemctl enable xrdp

sudo /etc/init.d/xrdp start

sudo /etc/init.d/xrdp status




