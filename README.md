# psad-munin-plugin
Wildcard plugin for Munin to monitor count of banned IPs via psad (https://cipherdyne.org/psad/)

## CONFIGURATION

This is a wildcard plugin.  The symlink name extension is the type of monitoring.

### Example:

 **ln -s /usr/share/munin/plugins/psad_ /etc/munin/plugins/psad_banned**

 Currently supports only this type of monitoring.

 This plugin must run with root privileges.

 For example, this or another plugins config file **/etc/munin/plugin-conf.d/00-default** must contain:

[psad_\*]<br/>
user root


Optionally, you can specify the path to the psad log file.

 [psad_*] <br/>
 user root <br/>
 env.psad_log_file /var/log/psad/auto_blocked_iptables


Known issues:

Known issues:
- [ ] works only with IPv4 addresses