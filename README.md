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


#(5). open ubuntu and install vnc-server
##searching realvnc server and copy download link.

wget [https://downloads.realvnc.com/download/file/vnc.files/VNC-Server-7.13.1-Linux-ARM64.deb](https://downloads.realvnc.com/download/file/vnc.files/VNC-Server-7.13.1-Linux-ARM64.deb?lai_vid=99PO2KRbqSjzn&lai_sr=5-9&lai_sl=l)

sudo apt install /home/User/VNC-Server-7.13.1-Linux-ARM64.deb

systemctl enable vncserver-x11-serviced.service

systemctl start vncserver-virtuald.service

sudo apt install xserver-xorg-video-dummy
sudo cp /etc/X11/vncserver-virtual-dummy.conf /etc/X11/xorg.conf

sudo nano /etc/gdm3/custom.conf

#WaylandEnable=false, remove #



#(4). install and boot vnc in windows
#don't sign it.
# File -> New connection
# VNC Server: ur IP Address(ex.192.168.137.121)
# Name: ~~
# ok
# doubleclick -> Identify check(continue)

#(5). make ur Username and Password.
#Then, u can use VNC Viewer!

