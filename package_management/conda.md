## Introduction
This document contains frequently used command and the corresponding used cases for package management software Conda. For simplification, all the variables are written in parenthesis, e.g. (package), (version). The optional parameters are written in sqaure brackets, e.g. [--versions], [--mixed]

&nbsp;
## Table of Content
* [Environment Setting](#environment-setting)
* [Channels](#channels)
* [Package Explorer](#package-explorer)
* [Package Installation](#package-installation)
* [Upgrade Installed Package](#upgrade-installed-package)
* [Export and Import](#export-and-import)

&nbsp;
## Environment Setting
<sub>[Back to Top](#introduction)</sub>
#### Install Conda package manager (on Linux)
```
wget https://repo.anaconda.com/archive/Anaconda3-(year).(month)-Linux-x86_64.sh
sh Anaconda3-(year).(month)-Linux-x86_64.sh
```
#### Update Conda package manager
```
conda update conda
```
#### Show Conda environments
```
conda info --envs
```
#### Create Conda environment
```
conda create -n (name) [package A][, package B...]
```
#### Switch Conda environment
```
conda activate (environment)
```
#### Return to Conda base environment
```
conda activate base
```
#### Remove Conda environment
```
conda remove --all -n (environment)
```

&nbsp;
## Channels
<sub>[Back to Top](#introduction)</sub>
#### Show all channels Conda has tracked
* use `--env` to show only activated environment
```
conda config [--env] --get channels
```
#### Disable channel priorities
* the packages will be installed with the newest version in any listed channel
* use `--env` to set only activated environment
```
conda config [--env] --set channel_priority false
```
#### Enable channel priorities
* use `--env` to set only activated environment
```
conda config [--env] --set channel_priority true
```
#### Track new channel with the highest priority
* use `--env` to set only activated environment
```
conda config [--env] --prepend channels (channel.url)
```
#### Track new channel with the lowest priority
* use `--env` to set only activated environment
```
conda config [--env] --append channels (channel.url)
```
#### Removed tracked channel
* use `--env` to set only activated environment
```
conda config [--env] --remove channels (channel)
```

&nbsp;
## Package Explorer
<sub>[Back to Top](#introduction)</sub>
#### Show installed packages
```
conda list -n (environment)
```
#### Show outdated packages
```
conda search --outdated
```
#### Search available packages in tracked channels
```
conda search (package/regex) 
```


&nbsp;
## Package Installation
<sub>[Back to Top](#introduction)</sub>
#### Install specific package in the activated environment
```
conda install (package)[=(version)]
```
#### Reinstall specific package in the activated environment
```
conda install [--force-reinstall] (package)
```
#### Uninstall specific package in the activated environment
* use `-n` to uninstall the pacakge only in given environment
```
conda remove [-n (environment)] (package)
```

&nbsp;
## Upgrade Installed Package
<sub>[Back to Top](#introduction)</sub>
#### Upgrade specific package in the activated environment
* use `-n` to update the pacakge only in given environment
```
conda update [-n (environment)] [package]
```
#### Upgrade all packages except for pinned packages
* use `-n` to update the pacakge only in given environment
```
conda update [-n (environment)] --all
```
#### Edit pinned packages
```
# console
vim $conda-root/conda-meta/pinned

# vim 
[package A==version]
[package B==version]
...
```

&nbsp;
## Export and Import
<sub>[Back to Top](#introduction)</sub>
#### Export packages
* use `-n` to export the pacakges in given environment
```
conda list [-n (environment)] --export [> packages.txt]
```
#### Import packages
```
conda install --file (packages.txt)
```
#### Create environment with given packages
```
conda create -n (name) --file (packages.txt)
```