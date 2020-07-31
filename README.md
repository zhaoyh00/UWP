## Instructions about install Python3 and use Virtual Machine on MacOS

Python is one of the most commonly used coding languages. Compared to other coding languages, Python has a cheaper learning cost. But having too many differences between versions is an obvious disadvantage in python language. For example, there are a lot of differences between Python2 and Python3. In most cases, some logic and features in Python3 cannot be implemented in Python2, vice versa. In order to reduce unnecessary conflict during software development, every software developer needs to learn how to install the latest version Python on their Operating System(OS).
In this program, I will help with installing Python3 on MacOS specifically.

## Choosing your IDE for Python programming
Personally speaking, I suggest using VScode for the beginner since VScode is a free source-code editor. Also, it has a large amount of extension to help the user debugging, testing, and sharing with others. 
```
Download link: https://code.visualstudio.com/download
```



## Install Python
For some users outside the U.S., such as China, the download speed of the official Python website may be extremely slow. To solve this question, I suggest using the homebrew command to download Python via terminal. Homebrew is a free and open-source software package management system which can be easily installed by typing (in a macOS Terminal or Linux shell prompt):
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```
After successfully installing homebrew, the user can type:
```
brew install pythonX
```
in the Terminal to install the python with the different versions they want. (the "X" of "pythonX" means the verson of python. If X = 3, homebrew will install python3).

## Setting flake 8 (pycodestyle)
Flake 8 is a very useful extension to help with debugging the python program. If your computer has installed this feature, it will help you detect the informal code in your file and give a warning. Although the most warning is related to the format which does not affect the outcome of code, the developers still need to pay attention to the format problems since it will play an important rule in group work. If your partner follows a different rule of format, you may think his/her code unreadable even you and your partner use the same logic. So that's why we also suggest setting flake 8 for python. (If you think this part hard to understand and you are confident enough in your formatting skill, you can just ignore this part.)


To set flake 8, Firstly, using 
```
brew list python
``` 
to get the location of python folder. In most cases, the default installation directory of homebrew is /usr/local/Cellar.
Open the folder python/bin and check if there is a exec named pip.

![Alt text](https://github.com/zhaoyh00/UWP/blob/master/img/img1.png)

In this picture, you can see that I have pip3.7 in my folder.

In the Terminal, type
```
pip3.7 install pycodestyle
```
For the users who are now in China, if the download speed is extremly slow, I suggest to use the mirror website of Tinghua University.
Type this command in Terminal:
```
pip3.7 install -i https://pypi.tuna.tsinghua.edu.cn/simple pycodestyle
```

### Setting yapf (Optional)
Yapf is also an extension to help the developers format their code. After successfully install it, you can just type Alt+Shift+F to let the VScode help you format your code based on PEP8rules just in seconds. If you fail to do the flake8 extension, you can try this for a substitute.


Type in the Terminal:
```
pip3.7 install -i https://pypi.tuna.tsinghua.edu.cn/simple yapf

```


### Setting in VScode for flake8 and yapf.
```
    "python.linting.flake8Path": "pycodestyle",
    "python.linting.flake8Enabled": true,
    "python.formatting.provider": "yapf",

```

By the way, these two setting are based on VScode, if you are using Pycharm IDE, you can just type
```
ctrl+alt+L
```
after you select the entire code.



### Install Virtual Box
Most people install Virtual Box because it is hard to find a Linux OS on the computer which is commonly seen for selling. Virtual Box is one of a free and open-source virtual machine. Although it may only have limited performance, it is enough for individual developer usage. 
To download Virtual Box first, there is its website: 
```
https://www.virtualbox.org/
```
We can also find some offical document from this website. I will go deeper to analyze the steps and hits for installing Virtual Box.

After going to the download pages, you should select the version that fits your platform. It provides Windows hosts, OS X hosts, Linux distributions, and Solaris hosts. For most users, only Windows hosts and OS X hosts are needed for programming. 


### Setup Virutal Box
After clicking "Next" for serval times, we can easily finish the installation. After double-clicking the Virtual Box, we can see a window called VirtualBox Manager like this:

(picture)


We can click "New" to create an empty virtual machine. 
There are several important points to create a virtual machine.
1. Give an appropriate name for your virtual machine. It will be better if you named your virtual machine based on the information related to it. For example, the type of it (it is a Windows virtual machine, OS virtual machine, or a Linux virtual machine), the date it has been created.etc.

2. Also need to change the Machine Folder of your virtual. As students in computer science, we all know the outcome of always stored things in the same default folder. 

3. Selecting the operating system type. This step is really important for 64-bit guests. Please carefully choosing this carefully to meet the requirement of the software.

4. Select the Memory(RAM) that Virtual Machine will use for every time it starts. However, you should choose the RAM setting carefully. If you set a really large RAM for you Virtual Machine, your computer might stop running because there is no more memory for other software to open.

5. To specify a Virtual Hard Disk for your VM. In most of the cases, the developers always select "Use an existing virtual hard disk file" in order to form a specific developing environment. For example, when the developer wants to use Ubuntu to develop their software for Linux, they would download the hard disk of Ubuntu and load it into the Virtual Machine. Using Ubuntu hard disk to form a Linux developing system is much convenient than buying a computer with a built-in Linux system.

6. After giving it file location and size, we can finish building our virtual machine and use it.


### Tips for Running Your Virtual Machine
1. Do not store important files only on your Virtual Machine and always remember to frequently save files on your Virtual Machine. Compared with build-in OS, Virtual Machine is more unstable and sometimes it will directly stop running and cannot recover your files easily as your build-in OS.

2. Do not open too much software while using your Virtual Machine. It will directly shut down without any notice, which will cause a lot of loss if the user is doing something important at the same time.

3. Have a stable power supply while using your Virtual Machine. Running program on Virtual Machine always costs more power than using programs on build-in OS. Therefore a stable power supply is important. Personally speaking, a laptop or other mobile device is not a good choice for using a Virtual Machine. (Even though Virtual Machine can successfully run on some of it.)

### About the reference
Installing Python and setting it are basedmy own experience. (I also used my own picture for Python part)
Some pictures and important ideas are provided by the offical document of Virtual Machine https://www.virtualbox.org/manual/ch01.html 