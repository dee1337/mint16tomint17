mint16 to mint17
==============

####update linux mint16 petra to mint17 qiana 
(the 'evil' way - safety not guaranteed)

1.) open '/etc/apt/sources.list.d/official-package-repositories.list' with your fav. texteditor, e.g. :
```bash
gedit /etc/apt/sources.list.d/official-package-repositories.list
```
2.) copy paste this into it:
```
#deb http://packages.linuxmint.com petra main upstream import 
#deb http://extra.linuxmint.com petra main
#deb http://archive.ubuntu.com/ubuntu saucy main restricted universe multiverse
#deb http://archive.ubuntu.com/ubuntu saucy-updates main restricted universe multiverse
#deb http://security.ubuntu.com/ubuntu/ saucy-security main restricted universe multiverse
#deb http://archive.canonical.com/ubuntu/ saucy partner

deb http://packages.linuxmint.com qiana main upstream import 
deb http://extra.linuxmint.com qiana main
deb http://archive.ubuntu.com/ubuntu trusty main restricted universe multiverse
deb http://archive.ubuntu.com/ubuntu trusty-updates main restricted universe multiverse
deb http://security.ubuntu.com/ubuntu/ trusty-security main restricted universe multiverse
deb http://archive.canonical.com/ubuntu/ trusty partner
```

3.) save it, open a terminal and run:
```bash
sudo apt-get update && sudo apt-get dist-upgrade
```
#### some notes:

it will take some time, depending on your machine & your internet connection - took me around an hour
it will try to replace older with newer files/configs - saying 'Y' to each worked for me and installed me a stable version

#####ps: use at your own risk
