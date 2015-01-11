munin-7dtd
==========

[Munin](http://munin-monitoring.org) plugins to monitor a 7 days to die dedicated instance through telnet console.

Available plugins :

* Currently online and known users
* Memory usage

![Memory usage](https://cloud.githubusercontent.com/assets/990787/5695656/1dccf362-99ae-11e4-899f-cbb2cf0cbc7c.png)
![Users](https://cloud.githubusercontent.com/assets/990787/5695657/1fb6ca86-99ae-11e4-89db-6eeeffb1ff69.png)

Installation
------------

Download latest stable or [master](//github.com/pygillier/munin-7dtd/archive/master.zip) zipball. Extract it somewhere on you disk and link 7dtd_* file from your munin plugins folder.

You need to restart your munin-node instance to activate plugins.

Configuration
-------------

Plugins are configured to connect to a server instance listening on `127.0.0.1` IP address and `8081` port. If your instance doesn't listen on this address, you must create a file in [plugins-conf.d](http://munin-monitoring.org/wiki/plugin-conf.d) on your munin master. 

This file must contains the following parameters

```
[7dtd_users]
env.host ip_address
env.port port_number

[7dtd_mem]
env.host ip_address
env.port port_number
```

[Apache licence](//github.com/pygillier.munin-7dtd/master/LICENSE) &copy; Pierre-Yves Gillier
