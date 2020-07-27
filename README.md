## Instructions about install Python3 and use Virtual Machine on MacOS

Python is one of the most commonly used coding language. Compared to other coding language, Python has a cheaper learning cost. But having too much differences between versions is a obvious disadvantage in python language. For example, there are a lot of differences between Python2 and Python3. In most cases, some logic and features in Python3 cannot be implemented in Python2, vice versa. In order to reduce unnessary conflictions during software developing, every software developer needs to learn how to install lates version Python on their OS.
In this program, I will help with installing Python3 on MacOS specificly.

## Choosing your IDE for Python programming
Personally speaking, I suggest to use VScode for the beginner since VScode is a totally free source-code editor. Also, it has large amount of extension to help the user debugging, testing, and sharing with others. 
```
download link: https://code.visualstudio.com/download
```



## Install Python
For some users outside the U.S., such as China, the download speed of the official Python website may be extremely slow. To solve this question, I suggest to use the homebrew command to download Python via terminal. Homebrew is a free and open-source software package management system which can be easily install by typing (in a macOS Terminal or Linux shell prompt):
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```
After sucessfully installing homebrew, the user can type:
```
brew install pythonX
```
in the Terminal to install the python with different version they want. (the "X" of "pythonX" means the verson of python. If X = 3, homebrew will install python3).

## Setting flake 8 (pycodestyle)
Flake is a very useful extension to help with debugging python program. If your computer has installed this feature, it will help you detect the informal code in your file and give a warnning. Although most of warnning is related to format which does not affect the outcome of code, the developers still need to pay attention to the format problems since it will play an important rule in group work. If your partner follow a different rule of format, you may think his/her code unreadable even you guys use the same logic. So that's why we also suggest to set flake 8 for python. (If you think it hard to understand and you are confident in your formatting skill, you can just ignore this part.)



To set flake 8, Firstly, using 
```
brew list python
``` 
to get the location of python folder. In most cases, the default installation directory of homebrew is /usr/local/Cellar.
Open the folder python/bin and check if there is a exec named pip.

(picture)

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

## Setting yapf (Optional)
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



# I am still working on the Virtual Machine part. The format will be very similar to the python part. 

