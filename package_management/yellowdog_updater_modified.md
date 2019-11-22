## Introduction
This document contains frequently used command and the corresponding used cases for package management software Yellowdog Updater, Modified (YUM). For simplification, all the variables are written in parenthesis, e.g. (package), (version). The optional parameters are written in sqaure brackets, e.g. [--versions], [--mixed]

&nbsp;
## Table of Content
* [Environment Setting](#environment-setting)
* [Package Explorer](#package-explorer)
* [Package Installation](#package-installation)
* [Upgrade Installed Package](#upgrade-installed-package)

&nbsp;
## Environment Setting
<sub>[Back to Top](#introduction)</sub>
#### Show all repositories YUM has tracked
```
sudo yum repolist [enabled/disabled/all] [--verbose]
```
#### Track new repository
```
sudo yum-config-management --add-repo (url)
```
#### Enable/disable new repository
```
sudo yum-config-management (--enable/disable) (repository)
```
#### Removed tracked repository
```
sudo rm /etc/yum.repos.d/(repository)
```

&nbsp;
## Package Explorer
<sub>[Back to Top](#introduction)</sub>
#### Show installed packages
```
yum list installed
```
#### Show outdated packages
```
yum check-update [packages]
```
#### Search available packages in tracked repository
```
yum list available (regex)
```
#### Search available packages (with all available versions) in tracked repostitory
```
yum --showduplicates list available (regex)
```
#### Show packages that are locked (not being upgraded)
```
yum versionlock list [packages]
```

&nbsp;
## Package Installation
<sub>[Back to Top](#introduction)</sub>
#### Install specific package
```
sudo yum install (package)[-(version)]
```
#### Install specific package from local file
```
sudo yum localinstall (RPM file)
```
#### Reinstall specific package
```
sudo yum reinstall (package)
```
#### Uninstall specific package (remove the dependencies as well)
```
sudo yum remove (package)
```

&nbsp;
## Upgrade Installed Package
<sub>[Back to Top](#introduction)</sub>
#### Upgrade specific package
```
sudo yum update (package)
```
#### Upgrade all packages except for locked packages
```
sudo yum update
```
#### Upgrade all packages with temporary exceptions
```
sudo yum update --exclude (package A)[,(package B),(package C)]
```
#### Upgrade and remove obsolete packages
```
sudo yum upgrade [package]
```
#### Disallow package to be upgraded
```
sudo yum versionlock add (package)
```
#### Allow package to be upgraded
```
sudo yum versionlock delete (package)
```
