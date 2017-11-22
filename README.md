ansible-role-nrpe
======

This role will install nagios-nrpe-server, /etc/nagios/nrpe.cfg, and any glob-matched files to /etc/nagios/nrpe.d/\*


Variables
------

```
ansible_role_nrpe_cfg_file: /path/to/group_files/nrpe/nrpe.cfg
ansible_role_nrpe_cfg_d: /path/to/group_files/nrpe/nrpe.d
```


Notes
------

All files will be copied statically (no templates)

ansible_role_nrpe_cfg_file points to nrpe.cfg

ansible_role_nrpe_cfg_d points to a directory with nrpe configs (e.g. checks.cfg) that will be globbed and transferred to /etc/nagios/nrpe.d/

If either of the two variables (ansible_role_nrpe_cfg_file, ansible_role_nrpe_cfg_d) are undefined, its respective install play will not run.
