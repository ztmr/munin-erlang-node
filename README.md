munin-erlang-node
=================

Munin plugin for Erlang node memory usage monitoring.

Requirements
------------

* **Erlang R15B01** or newer
* **Perl 5.10** or newer

Usage
-----

Debian:

1. Download ``erlang_node_`` and move it to ``/usr/share/munin/plugins``. Check does the file have **+x** filesystem flag.
2. ``ln -s /usr/share/munin/plugins/erlang_node_ /etc/munin/plugins/erlang_node_mynode`` (replace ``mynode`` with your node short name; if the node is accessible only using long name, it would be set in configuration).
3. Create a new configuration file or edit existing one under ``/etc/munin/plugin.d`` directory. All the parameters are optional. Example:
```ruby
[erlang_node_mynode]
env.cookie darkside          # the secret cookie used for node calls
env.name   mynode@localhost  # node long name
env.warn   1073741824        # warn when used memory exceeds this value (in bytes)
env.crit   1610612736        # critical used memory amount for node
```

4. Restart Munin node (``invoke-rc.d munin-node restart``).
5. Enjoy.

License
-------

[WTFPL](http://sam.zoy.org/wtfpl/)
