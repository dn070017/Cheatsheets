## Introduction
This document contains frequently used command and the corresponding used cases for package management software Advanced Packaging Tool (APT). For simplification, all the variables are written in parenthesis, e.g. (package), (version). The optional parameters are written in sqaure brackets, e.g. [--versions], [--mixed]

&nbsp;
## Table of Content
* [Environment Setting](#environment-setting)
* [Package Explorer](#package-explorer)
* [Package Installation](#package-installation)
* [Upgrade Installed Package](#upgrade-installed-package)

&nbsp;
## Environment Setting
<sub>[Back to Top](#introduction)</sub>
#### Update APT package index
```
sudo apt update
```
#### Show all personal package archives (PPA) repository APT has tracked
```
apt policy
```
#### Track new PPA repository
```
sudo apt-get install software-properties-common # if add-apt-repository is not available
sudo add-apt-repository ppa:(PPA repository/PPA)
```
#### Removed tracked PPA repository
```
sudo add-apt-repository --remove ppa:(PPA repository/PPA)
```

&nbsp;
## Package Explorer
<sub>[Back to Top](#introduction)</sub>
#### Show installed packages
```
apt list --installed
```
#### Show outdated packages
```
apt list --upgradable
```
#### Search available packages in tracked PPA repository
```
apt search [--names-only] (package/regex) 
```
#### Search available packages (with all available versions) in APT repostitory
```
apt list --all-versions (package)
```

&nbsp;
## Package Installation
<sub>[Back to Top](#introduction)</sub>
#### Install specific package
```
sudo apt install (package)[=(version)]
```
#### Reinstall specific package
```
sudo apt install [--reinstall] (package)
```
#### Uninstall specific package (but keep configuration files)
```
sudo apt remove (package)
```
#### Uninstall specific package (also remove configuration files)
```
sudo apt purge (package)
```

&nbsp;
## Upgrade Installed Package
<sub>[Back to Top](#introduction)</sub>
#### Upgrade specific package
```
sudo apt upgrade [package]
```
#### Upgrade all packages except for marked packages
```
sudo apt upgrade
```
#### Show marked packages
```
sudo apt-mark showhold
```
#### Disallow package to be upgraded
```
sudo apt-mark hold (package)
```
#### Allow package to be updated
```
sudo apt-mark unhold (package)
```
