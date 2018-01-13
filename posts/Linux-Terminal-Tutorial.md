title: Linux Terminal Tutorial
author: Amit Chambial
tags:
  - Linux
  - Terminal
categories:
  - Open Source
  - Linux
date: 2017-11-09 05:09:00
---
### Basics GNU/Linux Commands
![terminal](http://www.dwmkerr.com/content/images/2017/06/clear-screen-2.gif)
#### 1. ls :list directory contents
``` bash
ls
```
if you want to see hidden files/directories(beginning with dot .),use -a flag.
``` bash
ls -a
```
To know more about ls:
``` bash
man ls
```
#### 2. cd:Change Directory
``` bash
cd ../
cd /home/Desktop
```
> . respresents the current directory
..represents the parent directory
~represents the home directory(of the user)

#### 3. pwd : print the current/working directory

``` sh
pwd
/home/Desktop/scripts
```
#### 4. mkdir : make/create directory.
``` sh
mkdir my_directory
```
#### 5. rm : remove/delete file/directory
If directory useless is empty
``` sh
rm file1.txt
rm useless
```
if directory useless contain files then use
``` sh
rm -r useless
```
#### 6. sudo : superuser do, to gain root privilege
``` bash
sudo apt-get install gnome-shell
```
Then enter your user account password, and you would be able to do administrative tasks like root. So if you’re getting any permission error using a command, then adding sudo as a prefix, might help.

To use sudo with previously used command without sudo use this
``` bash
sudo !!
```
#### 7. mv : rename or move a file/directory
``` bash
mv file1 ~/Downloads/Archive/
```
the above command will move the file from the current directory to target directory.
``` sh
mv logo_2.jpg new_logo.jpg
```
it will rename the file to new_logo.jpg.
#### 8. cat : View File contents
``` sh
cat install.log
```
#### 10. cp : Copy Files/Directories
``` sh
cp movie_name.mp4 ~/Downloads/movies/
```
The above command will copy the movie_name.mp4 to the specified directory.
#### 11. Know Your Ip address
``` sh
ifconfig
```
#### 12. Open inbuit terminal text editor Nano
```
nano newfile.md
```
#### 13. Compiling C/C++ Program 
``` bash
g++ amit.c
./a.out 
g++ amit.cpp
./a.out
```
a.out is the object file generated after compilation.To run this we use

    ./a.out
### Package Management
These are Ubuntu Specific commands. It Requires root privilege, so just add the sudo prefix before each command (it will ask for the user password and you’re done!).
#### 14. apt-get : Command Line Tool for handling packages
There are various options such as

*install* – To install package.  
e.g Install the program PyRoom (A distraction Free Text Editor)
``` sh
sudo apt-get install pyroom
```
*remove* – To remove package
```sh
sudo apt-get remove kate
```
*update* – To update the package cache
``` sh
sudo apt-get update
```
 

####15. add-apt-repository – To add a PPA (for your favorite Application)

e.g add the PPA for the App Eidete (Screencasting program)
```sh
sudo add-apt-repository ppa:shnatsel/eidete-daily
```
After, adding the PPA, <code>apt-get update command</code> is required.

 

#16. apt-cache : To access the Package details from cache

search : search for the related packages in the apt-cache
e.g
``` sh
apt-cache search image editor
```

> use <code>man</code> to more about the commands