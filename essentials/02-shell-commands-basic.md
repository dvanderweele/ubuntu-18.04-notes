ls is to list files. To give a long listing of all files 
in a directory, use these flags:
```bash
ls -al
```
Use the -h flag to have ls convert output to more human
friendly output:
```bash	
ls -alh
```
A command to list all commands executed by the logged in user:
```bash
history
```
Search command history for all commands involving 'apt':
```bash
history | grep apt
```
If you want to execute, e.g. the second to last command again, and
you find out via the history command its history # is 151, this is 
a shorthand way of executing it again:
```bash
!151 
```
Create an alias so that typing turtle runs the command ls -l:
```bash
alias turtle="ls -l"
```
The file to save your aliases in so they persist even after you
log out of your shell:
```bash
~/.bashrc
```
Search the /var/log directory for any files that ends with .log:
```bash
find /var/log -name "*.log"
```
Perform the same above search, but case-insensitive:
```bash
find /var/log -iname "*.LOG"
```
Search the /var/log directory for any files that DON'T end with .log:
```bash
find /var/log ! -name "*.log"
```
A commmand to search the /etc directory for directories only:
```bash
sudo find /etc -type d
```
A command to search the /etc directory for any files that have been 
modified in the last 10 days:
```bash
sudo find /etc -mtime 10
```
A command to search the /etc directory for any files that have been 
modified in the last 10 minutes:
```bash
sudo find /etc -cmin -10
```
A command to search the current directory for all directories that do not
have their permission string set to 755, and change all those directories 
to the permission string 755
```bash
find . -type d ! -perm 755 -exec chmod {} \;
```
A command to search the current directory for all files that do not
have permission string set to 644, and change all those files to 
that permission string:
```bash
find . -type f ! -perm 644 -exec chmod {} \;
```
Search the /var/log directory recursively for any lines in any files that 
contain the word "error":
```bash
grep -r "error" /var/log/
```
Redirect the standard output of the command 'echo "hello world"' to 
a file called stdout.log:
```bash
echo "hello world" 1> stdout.log
```
Redirect the standard error of the command 'find / -name "log"' so that you don't 
have to view the errors in your terminal:
```bash
find / -name "log" 2> /dev/null
```
Redirect the standard output of the command 'find / -name "log"' into the 
file results.txt, and redirect the standard error to wherever standard output 
is being redirected:
```bash
find / -name "log" 1> results.txt 2>&1
```
Redirect the contents of the file results.txt to the cat command:
```bash
cat < results.txt
```
A command to redirect the contents of a mysql dump file [dump.sql] to a mysql command
which will ask the password for user [username] and restore the dump file 
into database called [dbname]:
```bash
mysql -u [username] -p [dbname] < [dump.sql]
```

