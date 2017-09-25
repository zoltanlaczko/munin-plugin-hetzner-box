# NAME

hetzner_box - Munin Plugin to monitor Hetzner StorageBox/Backup disk usage

# DEPENDENCIES

fstab entry:
```
curlftpfs#u123456:secret@u123456.your-storagebox.de /mnt/mybox1 fuse auto,user,uid=0,allow_other,_netdev 0 0
curlftpfs#u987654:secret@u987654.your-storagebox.de /mnt/mybox2 fuse auto,user,uid=0,allow_other,_netdev 0 0
curlftpfs#u456789:secret@u456789.your-backup.de /mnt/mybackup1 fuse auto,user,uid=0,allow_other,_netdev 0 0
```

packages:
```
php curlftpfs openssh-client sshpass mount grep
```

# INSTALLATION

Copy the plugin file into the munin plugins directory. For customization create a file in plugin-conf.d directory.

# CONFIGURATION

The plugin works without any configuration.

You can customize the alias name and warning/critical levels.

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

# CHANGELOG

### 1.1

* add inclusive backup support (your-backup.de)
* fix dependencies list
* minor fixes

### 1.0

* initial version

# MAGIC MARKERS

```
#%# family=auto
#%# capabilities=autoconf
```
