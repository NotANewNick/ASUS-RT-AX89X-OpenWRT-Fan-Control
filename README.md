This script is based on https://github.com/jjack-zz/openwrt-fancontrol

Its has some modifications and custom parts from OpenWRT forum thread https://forum.openwrt.org/t/add-support-for-asus-rt-ax89x-ax6000/137003/819


A replacement for default fan control for ASUS RT-AX89X running OpenWRT.

####To use it:

Download the new fan controller, save it to /etc/, and make it executable.

    wget --no-check-certificate https://github.com/NotANewNick/ASUS-RT-AX89X-OpenWRT-Fan-Control/blob/main/fancontrol.sh -O /etc/fancontrol.sh
    chmod +x fancontrol.sh

Test it to make sure that it runs correctly.

    /etc/fancontrol.sh verbose

Let it run in the background to keep your router cool.

    cd /etc && sh fancontrol.sh $

####Disable the orginal fan controller.

 This is done automatically in the script.

####Optional

Have this run on boot.
Add this to /etc/rc.local (In LuCI, it's System > Startup)

    cd /etc && sh fancontrol.sh $

