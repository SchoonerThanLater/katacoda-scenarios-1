## Using the ping command ##

`ping` is used to verify network connectivty of a remote host. This tells us whether or not the machine is online and responding. It also gives stats for packet loss and latency.

`gping` can display a ping graphically. Click the following set of commands to install gping: 

```echo "deb http://packages.azlux.fr/debian/ buster main" | sudo tee /etc/apt/sources.list.d/azlux.list
wget -qO - https://azlux.fr/repo.gpg.key | sudo apt-key add -
sudo apt update
sudo apt install gping```{{execute}}

Try the following commands in the terminal by typing them in.
If process are taking too long, use `^C`{{execute ctrl-seq}} to interrupt the sequence:

Command | Description
---------------------|----------------------------------------------------
`ping 8.8.8.8` | checks if the server google is online
`gping 8.8.8.8` | shows graphical ping for google
`ping canvas.nbps.org`| checks if the canvas is online
`gping canvas.nbps.org` | shows graphical ping for canvas
`ping -I docker0 8.8.8.8` | checks google through the docker0 port



[Source](https://www.oreilly.com/library/view/centos-quick-start/9781789344875/0a85790c-f514-4e1a-b845-aee537cfb831.xhtml)

