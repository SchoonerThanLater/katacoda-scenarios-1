## Using the nmblookup command ##

Use the link below to install nmblookup

`apt install samba-common-bin`{{execute}}

`nmblookup` is used to resolve NetBIOS computer names into IP addresses.

**Syntax:**
`nmblookup [options] netbios_name`

Try the following commands in the terminal by typing them in:

Command | Description
----------------------------|-----------------------------
`nmblookup -A canvas.nbps.org` | gets the IP address for canvas.nbps.org
`nmblookup -A wikipedia.org`| gets the IP address for wikipedia.org

On a Windows operating system, `nmblookup` would be replaced with `nbtstat`, `nslookup` or `dig`


[Source](https://www.oreilly.com/library/view/using-samba-second/0596002564/re320.html)
