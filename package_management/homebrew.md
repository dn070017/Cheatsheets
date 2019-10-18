## Introduction
This document contains frequently used command and the corresponding used cases for package management software Homebrew. For simplification, all the variables are written in parenthesis, e.g. (package), (version). The optional parameters are written in sqaure brackets, e.g. [--versions], [--mixed]

&nbsp;
## Table of Content
* [Environment Setting](#environment-setting)
* [Install Homebrew](#install-homebrew)
* [Package Explorer](#package-explorer)
* [Package Installation](#package-installation)
* [Update Installed Package](#update-installed-package)

&nbsp;
## Glossary
|Term|Explanation|Example|
|:---|:---|:---|
|Formula|A pacakge|Git|
|Keg|Where formulae are installed|/usr/local/Cellar/git/2.21.0/|
|Cellar|Where kegs are placed |/usr/local/Cellar/|
|Tap|Repository of tracked formulae |/usr/local/Homebrew/Library/Taps/mongodb/homebrew-brew/|
|Bottle|Precompiled binary for keg|qt-4.8.4.mavericks.bottle.tar.gz|
|Cask|Extension of Homebrew to install MacOS apps||

&nbsp;
## Environment Setting
<sub>[Back to Top](#introduction)</sub>
#### Install Homebrew
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
#### Update Homebrew
```
brew update
```
#### Show installation paths
```
brew --cellar [(package)]
```
#### Show all repository (of packages) Homebrew has tracked
```
brew tap
```
#### Track new repository
```
brew tap [url]
```
#### Removed tracked repository
```
brew untap [tap]
```

&nbsp;
## Package Explorer
<sub>[Back to Top](#introduction)</sub>
#### Show installed packages
```
brew list [--versions] [--pinned]
```
#### Show outdated packages
```
brew outdated
```
#### Show packages that are not dependencies of another package
```
brew leaves
```
#### Search available packages in Homebrew Formulae
```
brew search (package)
```
```
brew search /(regex)/
```
#### 

&nbsp;
## Package Installation
<sub>[Back to Top](#introduction)</sub>
#### Install specific package
```
brew install (package)[@(version)]
```
#### Reinstall specific package
```
brew reinstall (package)
```
#### Uninstall specific package
```
brew uninstall (package)
```
#### Uninstall specific version of installed package
```
rm -rf (keg)
```
#### Uninstall old versions of installed package
```
brew cleanup (package)
```
&nbsp;
## Update Installed Package
<sub>[Back to Top](#introduction)</sub>
#### Update specific package
```
brew upgrade (package)
```
#### Show what will be update
```
brew upgrade --dry-run
```
#### Update all packages except for pinned packages
```
brew upgrade
```
#### Disallow package to be updated
```
brew pin (package)
```
#### Allow package to be updated
```
brew unpin (package)
```
