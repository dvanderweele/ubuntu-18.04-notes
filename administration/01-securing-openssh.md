# Securing OpenSSH
## Administration

### Step One
After logging in as root is creating a regular, non-root user for yourself:
```bash
adduser [username]
```
A command to add the newly created [username] account to the sudo group:
```bash
usermod -aG sudo [username]
```
After logging in as regular account [username], which file do you edit to disable root login via ssh:
```bash
/etc/ssh/sshd_config
```
In the file above, the format of the line that does NOT allow root login via ssh:
```bash
PermitRootLogin no
```
Add a line in the same config file to whitelist the non-root [username] account as being allowed to login via ssh:
```bash
AllowUsers [username]
```
A command to restart the ssh service after editing the config file:
```bash
sudo systemctl restart ssh
```
**After editing the ssh config file and restarting the service, **before you logout**, open a separate terminal on your local machine and attempt to ssh into the server via the same [username] account, just to make sure everything still works.*
Step two of securing Ope

### Step Two
The command, on your local machine, to generate an ssh key for the purpose of automating the login process with your remote server so that password authentication can be disabled:
```bash
ssh-keygen
```
The command, on your local machine, to copy your public ssh key to the user account [username] on your server at ip address xxx.xxx.xxx.xxx:
```bash
ssh-copy-id -i ~/.ssh/id_rsa.pub [username]@xxx.xxx.xxx.xxx
```
The file to edit on your remote server in order to disable password authentication over ssh:
```bash
/etc/ssh/sshd_config
```
The format of the line in the file above which disables password authentication over ssh:
```bash
PasswordAuthentication no
```
The final step you must take regarding the ssh service after disabled password authentication in the config file:
```bash
sudo systemctl restart ssh
```

