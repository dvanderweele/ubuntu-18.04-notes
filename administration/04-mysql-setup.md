# Setting Up MySQL
## Administration

A command to install the mariadb server package:
```bash
sudo apt install mariadb-server
```
A command to isntall the mysql server package:
```bash
sudo apt install mysql-server
```
Whether you are using mariadb or mysql, you should use the following command to secure your database server:
```bash
sudo mysql_secure_installation
```
A command to check if mariadb is running and enabled:
```bash
sudo systemctl status mariadb
```


