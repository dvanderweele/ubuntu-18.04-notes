# Managing SYSTEMD Units
## Essentials
Get the status of a systemd unit, for example apache2:
```bash
systemctl status apache2
```
Stop a systemd unit, for example apache2:
```bash	
sudo systemctl stop apache2
```
Start a systemd unit, for example apache2:
```bash
sudo systemctl start apache2
```
To configure a systemd unit, for example apache2,
to start up when the system boots:
```bash
sudo systemctl enable apache2
```
To configure a systemd unit, for example apache2,
so it doesn't start up when the system boots:
```bash
sudo systemctl disable apache2
```

