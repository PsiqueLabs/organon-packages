This repository hosts the PKGCONFIGS and databases of [Organon](https://github.com/fnk0c/organon)
-----

### PKGCONFIG
PKGCONFIG contains information used during the compilation process  

### Database
The database stores all packages name, version and description  

### Package_status
Conteins all packages and its status.  

* If its PKGCONFIG has been done  
* If it was tested  
* If it works  
* Which distribution it works, and which doesn't  

**Adding/Editing/Removing packages**  
Execute the Python script
`python gen_pkgconfig.py`  

![menu](http://imgur.com/d7AiYOel.png)

#### Create PKGCONFIG
Select option 1

```
Maintaner = Who's gonna keep the package up to date
Package Name = package name
arch = Which platform does the package run? (any, x86 or x86_64)
version = git (if github) x.x (if downloaded of other website)
source = url to fetch package source
process =
#here you insert all of the required commands and process
#use shell script syntax

exemple: 
./configure
make
sudo make install

After done type ":q" to exit

installer = (none or script)
type = It will only shows up if installer is different of "none" Here you must tell the type
        if application (python, perl...)

source_name = How the package is called after download
    exemple: package.tar.gz or package.zip
Os = Which distribuition runs it? Debian, Arch, Fedora
dependencies = Required dependencies (ntfs-3g, netools)
description = Package description
```

#### Update PKGCONFIG
Select option 2

```
Package Name = Name of the package that will be updated
Packet Name = It's like "source_name"
              How the package is called after download
              exemple: package.tar.gz or package.zip
Dependencies = Required dependencies (ntfs-3g, netools)
Update to version = Which version are you updating the package to?
URL = Like "source" 
      url to fetch package source
```

#### Deleting PKGCONFIG
Select option 3

```
Package Name = Name of the package that will be removed
```
