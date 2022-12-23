
### Install dpkg-repack Install dpkg-repack and fakeroot Install fakeroot (to avoid being root to repackage). Or from the terminal:
```
sudo apt-get install dpkg-repack fakeroot
```
### Repackge installed package
```
fakeroot -u dpkg-repack <package name>
```
### can view the contents of that deb file using command:
```
dpkg --contents hello-world_0.0.1_amd64.deb
```
### restore package on new system 
```
apt install -f ./hello-world_0.0.1_amd64.deb
```
