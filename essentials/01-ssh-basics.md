# SSH Basics 
## Essentials

openssh-server should be installed by default on ubuntu 18.04.

If it isn't, update your package list:	
```bash
sudo apt update
```
Then install via apt:
```bash
sudo apt install openssh-server
```
The other package that should be installed by default is
the ssh client package, which is for connecting to other
openssh-servers.

If it isn't installed, install it with:
```bash
sudo apt install ssh
```
To view the ip address of the machine you're on, type:
```bash
ip a
```
That command is short for:
```bash
ip addr show
```

## SSH for GitHub
Generate a new ssh key, substituting your email address:
```bash
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```
Start ssh-agent in background:
```bash
eval "$(ssh-agent -s)"
```
Add your private ssh key to the agent:
```bash
ssh-add ~/.ssh/id_rsa
```

