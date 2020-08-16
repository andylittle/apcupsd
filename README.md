# apcupsd

This is config to run two instances of apcupsd on a raspberry pi. Should work on debian versions.

Not completely sure about the PIDfile and forking in unit files


    apt update && apt upgrade -y && apt install apcupsd
    stop apcupsd.service
    disable apcupsd.service
    cp apcupsd/etc/systemd/system/apc?upsd.service /lib/systemd/system
    cp apcupsd/etc/udev/rules.d/ups.rules /etc/udev/rules.d/
    cp apcupsd/etc/apcupsd/apc?upsd.conf /etc/apcupsd/
    
Make needed changes to conf files if needed.     
   
    systemctl start apc1upsd.service
    systemctl start apc2upsd.service
    systemctl enable apc2upsd.service 
    systemctl enable apc1upsd.service
    
@@TODO
Have it actually shut down the systems
Fix the PID file
