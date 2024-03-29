# Permissions 
## Essentials 

To change the user owner of [filename] 
so that [username] owns it:
```bash
sudo chown [username] [filename]
```
To change ownership of file [filename] 
so that user [username] owns it,
and group [groupname] owns it:
```bash
sudo chown [username]:[groupname] [filename]
```
A shorthand version of the last command to specify
that the personal group of user [username] will 
also own [filename]:
```bash
sudo chown [username]: [filename]
```
To specify that you want the ownership of directory
called [directory], as well as all of its contents
recursively, to change to user [username] and that 
user's personal group:
```bash
sudo chown [username]: -R [directory]
```
To specify that you want to give read-access for 
[filename] to the user owner:
```bash
sudo chmod u+r [filename]
```
To specify that you want to take away write-access for
[filename] from the group owner:
```bash
sudo chmod g-w [filename]
```
To specify that you want to give read, write, & execute 
access for [filename] to everyone other than user and group
owners:
```bash	
sudo chmod o=rwx [filename]
```

