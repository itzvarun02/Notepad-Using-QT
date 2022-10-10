
# NotePad using QT Creatior 8.0.1

 Notepad is a simple text editor for Ubuntu .


## Ubuntu and Qt version
Distributor ID: Ubuntu
Description: Ubuntu 22.04.1 LTS
Release: 22.04
Codename: jammy

Qt --version 8.0.1


## Qt Creatior Installation For ubuntu 22.0.4

The 22.04 is based on Debian bullseye, which does not have qt5-default package in the repository.
so
If you are installing some package from third-party which requires qt5-default package on Ubuntu 
22.04 (or newer), then you can create fake package by using commands below:

```bash
sudo apt-get update
sudo apt-get install equivs

cd ~/Downloads
cat <<EOF > qt5-default-control
Package: qt5-default
Source: qtbase-opensource-src
Version: 5.99.99+fake-13ubuntu37
Architecture: all
Depends: qtbase5-dev, qtchooser
Suggests: qt5-qmake, qtbase5-dev-tools
Conflicts: qt4-default
Section: libdevel
Priority: optional
Homepage: http://qt-project.org/
Description: Qt 5 development defaults fake package
EOF
equivs-build qt5-default-control
sudo apt-get install ./qt5-default_5.99.99+fake-13ubuntu37_all.deb

```
After Installation Reboot your Terminal...

## How to run the code

1. Download the file using git
2. Follow the instruction Given Bellow 
```bash
$ cd Notepad
$ qmake Notepad.pro
$ make
//To run the Notepad
$ ./Notepad
```

## What has been done
1. Build a basic text-editing app with bold/unbold, Italic, Underline of an individual text
2. resume in a dialogue box

## Futurescope

1. superscript and subscript functionality

    
## Issues/challenges
QLineEdit wasn't really made for superscript and subscript functionality type of thing, as it was designed for simple text entry. 

## Features
1. All Basic Element of Note pad
2. New Icons
3. Better and stable 
4. Print Features
5. All Font functionality
