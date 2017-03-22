# NAME

hetzner_box - Munin Plugin to monitor Hetzner StorageBox disk usage

# DEPENDENCIES

fstab entry:
```
curlftpfs#u123456:secret@u123456.your-storagebox.de /mnt/mybox1 fuse auto,user,uid=0,allow_other,_netdev 0 0
curlftpfs#u987654:secret@u987654.your-storagebox.de /mnt/mybox2 fuse auto,user,uid=0,allow_other,_netdev 0 0
```

packages:
```
php curlftpfs openssh-client sshpass
```

# CONFIGURATION

The plugin works without any configuration. But you can customize the alias name and warning/critical levels.

```
[hetzner_box]
   env.box_u123456_alias mybox1
   env.box_u123456_warning 92
   env.box_u123456_critical 98
   env.box_u987654_alias mybox2
```

# AUTHOR

Zoltan Laczko <zoltan@laczko.hu>

# LICENSE

GPLv3

# MAGIC MARKERS

```
#%# family=auto
#%# capabilities=autoconf
```
