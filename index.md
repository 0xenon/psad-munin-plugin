## plugin for munin that monitoring blocked IPs by psad
Wildcard plugin for Munin to monitor count of banned IPs via psad (https://cipherdyne.org/psad/)

![graph preview](https://github.com/0xenon/psad-munin-plugin/blob/main/graph.png)

## CONFIGURATION

This is a wildcard plugin.
The possible wildcard values are the following: banned, levels

### Example:
```
 ln -s /usr/share/munin/plugins/psad_ /etc/munin/plugins/psad_banned
 ln -s /usr/share/munin/plugins/psad_ /etc/munin/plugins/psad_levels
```
 This plugin must run with root privileges.

 For example, this or another plugins config file **/etc/munin/plugin-conf.d/00-default** must contain:
```
[psad_\*]
user root
```

Optionally, you can specify the path to the psad log file.
```
 [psad_*]
 user root <br/>
 env.psad_log_file /var/log/psad/auto_blocked_iptables
```

Known issues:
- [ ] works only with IPv4 addresses
