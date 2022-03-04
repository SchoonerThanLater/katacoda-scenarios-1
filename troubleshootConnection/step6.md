## Using the arp command ##

`arp` is used to resolve the IP address of a system to its mac address. It stands for *Address Resolution Protocol*

**Syntax:**
`arp [-v] [-i if] [-H type] -a [hostname]`

Try the following commands in the terminal by typing them in:

Command | Description
----------------------------|-----------------------------
`arp -a` | displays all hosts
`arp -v`| displays the verbos infromation
`arp -n` | displays shows numerical address instead of symbolic host, port, or usernames
`arp -H ether` | checks for the ethernet ports
`arp -a` | displays the new host
`arp -d <enter an IP address from arp -a>` | deletes the specified host


[Source](https://www.geeksforgeeks.org/arp-command-in-linux-with-examples/)
