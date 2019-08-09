# Checking Logs 
## Essentials

The directory in which all logs are stored:
```bash
/var/log
```
The log file containing login history for system:
```bash
auth.log
```
A kind of 'catch-all' log file that contains all kinds 
of logs pertaining to things that happen on the system:
```bash
syslog
```
Display the first ten lines of the syslog file:
```bash
head /var/log/syslog
```
Display the last ten lines of the syslog file:
```bash
tail /var/log/syslog
```
Display the first 100 lines of the syslog file:
```bash
head -n 100 /var/log/syslog
```
Display the last 50 lines of the syslog file:
```bash
tail -n 100 /var/log/syslog
```
Display the last ten lines of the syslog file, 
and continue to print any realtime updates to it:
```bash
tail -f /var/log/syslog
```
A newer command to view logs pertaining to a particular
systemd unit, say apache2:
```bash
journactl -u apache2
```
The version of the command immediately above that also 
continues to print any realtimes updates:
```bash
journalctl -fu apache2
```
