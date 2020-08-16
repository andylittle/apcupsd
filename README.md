# apcupsd

This is config to run two instances of apcupsd on a raspberry pi. Should work on debian versions.

Not completely sure about the PIDfile and forking in unit files


`apt update && apt upgrade -y && apt install apcupsd
stop apcupsd.service
disable apcupsd.service
cp apcupsd/etc/systemd/system/apc?upsd.service /lib/systemd/system
cp apcupsd/etc/udev/rules.d/ups.rules /etc/udev/rules.d/
cp apcupsd/etc/apcupsd/apc?upsd.conf /etc/apcupsd/
`
