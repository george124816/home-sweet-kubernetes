# home sweet ~~home~~ kubernetes

#### enable nfs on main server

$ apt install nfs-kernel-server
add following lines on `/etc/exports`
```
/mnt/hd1	192.168.18.0/24(rw,wdelay,insecure,no_root_squash,no_subtree_check,sec=sys,rw,insecure,no_root_squash,no_all_squash)
```

#### enable nfs client on workers

$ apt install nfs-common
add following lines on `/etc/fstab`
```/etc/fstab
192.168.18.100:/mnt/hd1		/mnt/hd1	nfs	defaults	0	0
```

loadbalancer: [metalLB](https://github.com/metallb/metallb)

- gitea
- postgres
- hakatime
- plex
- drone.io
