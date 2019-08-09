# Checking System Vitals 
## Essentials 

A command to view the disk usage and availability
for different filesystems, in human-readable format
```bash
df -h
```
A command to view disk space used in current directory
with human readable output:
```bash
du -h
```
A command to view which directories within the /lib 
directory are taking up how much space, with 
human readable output: 
```bash
sudo du -hsc /lib/*
```
A great package to install via apt to monitor disk 
usage: 
```bash
ncdu
```
Use the above command to scan starting at root filesystem
and skip any network or external drives it encounters:
```bash
sudo ncdu -x /
```
The best command to monitor things like CPU usage, RAM usage,
SWAP Usage, and processes:
```bash
htop
```
A command to quickly see how long the system has been up, 
how many users are logged in, and the load average:
```bash
uptime
```
A command to see how much memory (RAM & SWAP) is being used
in megabytes:
```bash
free -m
```

