# Network File System

## Steps
***For Server Side***<br>
1. Install & Enable the packages required like(nfs-kernel-server, Bind etc) <br>
2. Create directory to share files `mkdir /home/share` & `chmod 777 folderName` <br>
3. Edit `/etc/exports` below line<br>
```bash
/home/share client_ip(rw,sync,no_subtree_check)
sudo exportfs -rav #apply effect
sudo exportfs -v #check status
```
4. Configure firewall for client
```bash
sudo ufw allow from client_ip to any port 2049 proto tcp
sudo ufw status
```
***For Client Side***
1. install packages & enable like (nfs-common) 
2. check mountpoint of server
```bash
showmount -e srever_ip
sudo mkdir -p /mnt/nfs #create mount point
```

### Create NFS mount
```bash
sudo mount server_ip:/home/share /mnt/nfs
df -h /mnt/nfs #test the changes
```

### Make permanent

Edit `/etc/fstab` on the client:
```bash
sudo nano /etc/fstab
#Add:
server_ip:/home/share /mnt/nfs nfs defaults,_netdev 0 0
#Test the configuration without rebooting:
sudo mount -a
```