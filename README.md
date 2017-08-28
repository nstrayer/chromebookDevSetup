# chromebookDevSetup
A simple set of steps to go from fresh chromebook to active dev environment


## Termux
Go to the android appstore and install `termux`. Once its installed, open it and run the following commands. 

```bash
apt update   
apt upgrade
apt install coreutils
pkg upgrade
pkg install termux-tools proot util-linux net-tools 
pkg install openssh tree git
termux-setup-storage # allows access to chromebook's file system. Kinda important. 
```


## Chrome Apps

_Most likely these will just auto install after you've done this the first time so you will only have to do this once._

[__Web Server For Chrome__](https://chrome.google.com/webstore/detail/web-server-for-chrome/ofhbbkphhbklhfoeikjpcbhemlocgigb?hl=en). This is a fantastic little app that allows you to spinup a super simple dev server. (Alternatively you could just run a server using `termux` but this is less command line. 

[__Caret Editor__](https://chrome.google.com/webstore/detail/caret/fljalecfjciodhpcledpamjachpmelml?hl=en) This is a great and lightweight text editor that has good syntax highlighting and basic linting for javascript. 


__Bonus__: create an ssh key.

If you're going to be using the chromebook for any extended period of time it's nice to have an ssh key installed for termux to access git or a server you may want to ssh into. This is rather simple. We already installed the package for generating ssh keys so just run `ssk-keygen` and press enter a bunch of times. Then `cat .ssh/id_rsa.pub` and paste that into github. 

