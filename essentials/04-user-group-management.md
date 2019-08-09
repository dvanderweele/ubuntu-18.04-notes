# User & Group Management
## Essentials 

To add a new user called [username]:
```bash
sudo adduser [username]
```
To delete a user called [username] and 
retain their home directory:
```bash
sudo userdel [username]
```
To delete a user called [username] and 
also delete their home directory:
```bash
sudo userdel -r [username]
```
The config file containing info on user
accounts, such as account number or 
default shell:
```bash
/etc/passwd
```
The command to view the groups the currently
logged in user is a part of:
```bash
groups
```
To view the groups that a user 
called [username] is a part of:
```bash
groups [username]
```
To add a user called [username] to a group 
called [groupname]:
```bash
sudo gpasswd -a [username] [groupname]
```
As an example, to add user jdoe to the sudo group:
```bash
sudo gpasswd -a jdoe sudo
```
The config file containing the list of all groups 
on the system:
```bash
/etc/group
```
To create a new group called [groupname]:
```bash
sudo groupadd [groupname]
```
To remove a user called [username] from 
a group called [groupname]:
```bash
sudo gpasswd -d [username] [groupname]
```
To delete a group called [groupname] from the 
system:
```bash
sudo groupdel [groupname]
```
If you are logged in, but not as root, and you 
want to log in as user [username] via that user's
password:
```bash
su [username]
```
If you are logged in, but not as root, and you 
want to log in as user [username] NOT via that user's
password:
```bash
sudo su - [username]
```
IF you are logged in, but not as root, and you 
want to log in as the root user:
```bash
sudo su -
```

