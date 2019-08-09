To update the index that apt/ubuntu has so that
it knows about the latest available software:
```bash
sudo apt update
```
To search for a package, using any [keyword], 
via apt:
```bash
sudo apt search [keyword]
```
To add a repository called universe to apt:
```bash
sudo add-apt-repository universe
```
To install a package called [name] via apt:
```bash
sudo apt install [name]
```
To remove a package called [name] via apt:
```bash
sudo apt remove [name]
```
To remove a package called [name] along with
any of its config files in the /etc directory:
```bash
sudo apt remove --purge [name]
```
To upgrade all packages that have available upgrades
which do not require the installation or removal of 
other packages:
```bash
sudo apt upgrade 
```
To upgrade all packages that have available upgrades 
including those which require the installation or removal 
of other packages:
```bash
sudo apt upgrade
sudo apt dist-upgrade
```

