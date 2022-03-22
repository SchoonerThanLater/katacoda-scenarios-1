## Using the tracepath command ##

`tracepath` is used to trace the path from origin to a destination. 

Try the following commands in the terminal by typing them in
If process are taking too long, use `^C`{{execute ctrl-seq}} to interrupt the sequence:

Command | Description
----------------------------|-----------------------------
`tracepath canvas.nbps.org` | trace the path to canvas
`tracepath -h`| show the options for tracepath

On a Windows operating system, `tracepath` would be replaced with `pathping`


[Source](https://www.oreilly.com/library/view/centos-quick-start/9781789344875/bad42240-4036-445f-997b-87d399deb57e.xhtml)

> `traceroute` is a deprecated version of `tracepath`
> ## Using the traceroute command ##
>
> traceroute is deprecated but is used on some older unix based OS.
>
> `traceroute` is used to trace a network packet as it travels your network. It can be used to troubleshoot network delays and errors
>
> Try the following commands in the terminal by typing them in:
> 
> Command | Description
> ----------------------------|-----------------------------
> `traceroute 8.8.8.8` | traces the route to google
> `traceroute canvas.nbps.org` | traces the route to canvas
> `traceroute 0.0.0.0` | trace route to an unspecified address
> 
> 
> On a Windows operating system, `traceroute` would be replaced with `tracert`
> 
> [Source1](https://www.oreilly.com/library/view/mastering-windows-server/9781789804539/bc2eae11-335a-4603-8959-d044a41bbf13.xhtml)
> [Source2](https://www.oreilly.com/library/view/centos-quick-start/9781789344875/a9b91e07-9534-485b-ae15-cd05d35f42a0.xhtml)