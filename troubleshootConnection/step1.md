*Using the ifconfig command*

This command is used to display or modify the current configuration of network interfaces. You can also use `ip` in place if `ifconfig`. Using the commands `ip addr`{{execute}} or `ip link`{{execute}} will have similar displays. Try each of the following commands in the terminal as well. You will need to type in each command:

Command | Description
__________|___________________
`ifconfig` | Display the current configuration of actyive interfaces only
`ifconfig -a` | Display all interfaces information with are available, active or inactive
`ifconfig eth0` | Display the configuration of the interface eth0
`ifconfig eth0 up` | Activate eth0


On a Windows operating system, `ifconfig` would be replaced with `ipconfig`

