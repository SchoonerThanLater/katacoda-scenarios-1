## Using the ping command ##

`ping` is used to verify network connectivty of a remote host. This tells us whether or not the machine is online and responding. It also gives stats for packet loss and latency.

Try the following commands in the terminal by typing them in.
If process are taking too long, use `^C`{{execute ctrl-seq}} to interrupt the sequence:

Command | Description
---------------------|----------------------------------------------------
`ping 8.8.8.8` | checks if the server google is online
`ping canvas.nbps.org`| checks if the canvas is online
`ping -I docker0 8.8.8.8` | checks google through the docker0 port



[Source](https://www.oreilly.com/library/view/centos-quick-start/9781789344875/0a85790c-f514-4e1a-b845-aee537cfb831.xhtml)

