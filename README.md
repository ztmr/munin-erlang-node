munin-erlang-node
=================

Munin plugin for Erlang node memory usage monitoring.

Requirements
------------

**Erlang R15B01**

Usage
-----

```
wget https://github.com/Mendor/munin-erlang-node/blob/master/erlang-node
chmod +x erlang-node
mv erlang-node /usr/share/munin/plugins/
ln -s /usr/share/munin/plugins/erlang-node /etc/munin/plugins/
```

Tested for Debian.

Don't forget to edit ``erlang-node`` file on any stage and set your Erlang node name, cookie and warning/alert values.

License
-------

[WTFPL](http://sam.zoy.org/wtfpl/)
