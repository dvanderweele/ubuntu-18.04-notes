# Adding Storage 
## Essentials 

A command to see what storage volumes you currently 
have available on the system:
```bash
sudo fdisk -l
```
If the above command revealed you have an available 
storage device at /dev/sdb, use this command to 
start partitioning the device:
```bash
sudo fdisk /dev/sdb
```
If the above command resulted in a GPT partition on 
/dev/sdb called /dev/sdb1, how do you format that 
partition so that it uses the ext4 filesystem:
```bash
sudo mkfs.ext4 /dev/sdb1
```
A command to list the current filesystems attached:
```bash
df -h
```
A command to mount your /dev/sdb1 partition at /mnt:
```bash
sudo mount /dev/sdb1 /mnt
```
A command to unmount the filesystem mounted at /mnt:
```bash
sudo umount /mnt
```
A command to mount your /dev/sdb1 partition at 
/mnt/newdisk1/:
```bash
sudo mount /dev/sdb1 /mnt/newdisk1
```
The file that defines filesystems that should be 
permanently mounted (i.e. on every system boot):
```bash
/etc/fstab
```
The line to add to the above file if you want 
/dev/sdb1 to automount on every boot right after 
the root filesystem is mounted, and to be mounted 
at /mnt/newdisk1:
```bash
/dev/sdb1 /mnt/newdisk1 ext4 default 0 1
```
A command to tell the system to check /etc/fstab 
and mount everything in there that isn't already 
mounted, as a way of checking if changes to the 
file are correct:
```bash
sudo mount -a
```

