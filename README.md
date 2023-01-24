### Install apt package which want to backup after configuration
```
apt install pdns-server
```
![Install pdns-server](https://github.com/shamim4s/Backup-Installed-Packages/blob/master/images/install%20pdns.png?raw=true)

### After install you can check which files are installed in which location
```
dpkg -L pdns-server
```

### Install dpkg-repack Install dpkg-repack and fakeroot Install fakeroot (to avoid being root to repackage). Or from the terminal:
```
sudo apt-get install dpkg-repack fakeroot
```
### Repackge installed package
```
fakeroot -u dpkg-repack <package name>
```
Check created deb files
```
ls -l
```

### can view the contents of that deb file using command:
```
dpkg --contents pdns-server_4.1.1-1_amd64.deb
```
### restore package on new system 
```
apt install -f ./pdns-server_4.1.1-1_amd64.deb
```
