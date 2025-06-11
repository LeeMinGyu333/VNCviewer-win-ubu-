# VNCviewer-win-ubu(Windows10- Ubuntu24.04, in 2025.06.11)

# 1. USE putty to remote access ubuntu
#(1). start window and ubuntu.
# turn on hotspot in windows and connect to ubuntu


#(2). open ubuntu and try to this

sudo apt update
sudo apt install openssh-server

sudo systemctl start ssh
sudo systemctl enable ssh
sudo systemctl status ssh
#now u can see active(running) in screen.


#(3). open window and start putty
# typing Host Name(IP address) and open. u can see ip address in hotspot settings.
 #ex)192.168.137.121
#accept
# typing ur ubuntu's ID and password. SO NOW UR PC CONNECTED SSH. 


##(ignore that, it is for my raspberry pi setting. But if u installed ubuntu in raspberry pi. u will need it.)##
sudo apt install git
git clone https://github.com/RPi-Distro/raspi-config.git
cd raspi-config
sudo ./raspi-config

# ENTER(PUSH), TAP(BACK)
## 6. Advanced Options -> A6 Wayland -> W1 X11 -> OK
## FINISH
## again (3)
## 3. Interface Options -> I2 VNC -> YES -> OK
## 2. Display Options -> D3 VNC Resolution -> 1600x1200 -> OK
## FINISH


#(4). install and boot vnc in windows
#don't sign it.
# File -> New connection
# VNC Server: ur IP Address(ex.192.168.137.121)
# Name: ~~
# ok
# doubleclick -> Identify check(continue)

#(5). make ur Username and Password.
#Then, u can use VNC Viewer!

