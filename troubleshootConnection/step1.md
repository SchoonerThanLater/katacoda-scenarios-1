## Using the ifconfig command ##

This command is used to display or modify the current configuration of network interfaces. You can also use `ip` in place if `ifconfig`. Using the commands `ip addr`{{execute}} or `ip link`{{execute}} will have similar displays. Try each of the following commands in the terminal as well. You will need to type in each command:

Command | Description
----------------------------|-----------------------------
`ifconfig` | Display the current configuration of actyive interfaces only
`ifconfig -a` | Display all interfaces information with are available, active or inactive
`ifconfig docker0` | Display the configuration of the interface eth0
`ifconfig docker0 up` | Activate eth0


On a Windows operating system, `ifconfig` would be replaced with `ipconfig`

[Source](https://www.oreilly.com/library/view/centos-quick-start/9781789344875/a1c8676e-6880-43f2-a8d3-ec212f62cf6c.xhtml)