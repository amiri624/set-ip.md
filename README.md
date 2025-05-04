




# set-ip.md
# how can we set ip?
```bash 
cd /etc/netplan/
```
```bash
ls 
```
### we see 50-cloud-init.yaml
```bash
vim 50-cloud-init.yaml
```
```bash 
network:
  version: 2
  renderer: networkd
  ethernets:
    enp0s3:
      dhcp4: no
      addresses:
        - 192.168.1.100/24
      gateway4: 192.168.1.1
      nameservers:
        addresses:
          - 8.8.8.8
          - 8.8.4.4
```

```bash
:wq
```
```bash
cat 50-cloud-init.yaml
```
