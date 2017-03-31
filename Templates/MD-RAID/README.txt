It was borrowed from https://github.com/linuxsquad/zabbix_mdraid

Zabbix template handles Software RAID (MD) on Linux
==================

Design and Implementaion:
-----------------

- auto-discovery for all active MDs
- no assumption made about MD name
- currently, only two HDD/SSD reported as members of the array
- trigger is constructed to monitor RAID State.
- to avoid flipping, the trigger will fire if state change sustain for  
 more than one collection cycle


TO DO list
------

- indtroduce items: failed device, number of failed devices
- auto-discover array devices


Append to zabbix_agentd.conf file
----------------

chmod 755 /etc/zabbix/scripts/zabbix_mdraid.sh

Note
----
**don't forget to add zabbix user to sudoers**


Referrence:
-------

- https://www.kernel.org/doc/Documentation/md.txt
- http://unix.stackexchange.com/questions/47163/whats-the-difference-between-mdadm-state-active-and-state-clean
- Zabbix LSI RAID template https://www.zabbix.com/wiki/templates/start

