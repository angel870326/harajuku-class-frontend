# Harajuku-class frontend
This is the frontend stack for the Harajuku-class project.


## Install yarn
Fix the "Missing write access" error
```
sudo chown -R $USER /usr/local/lib/node_modules
npm install -g yarn
```


## Clone

```
cd /Users/angelwang/Desktop
git clone https://github.com/aeroworks-io/harajuku-class.git
```
```
git clone https://github.com/aeroworks-io/harajuku-class.git -b angel870326-patch-1
```


## Setup
1. change directory to ```harajuku-class/frontend```
```
cd /Users/angelwang/Desktop/harajuku-class/frontend
```
2. install
```
make install
``` 
or 
```
yarn install
```
(install react-swipeable-views)
```
yarn add react-swipeable-views
``` 


## Developing server

```shell
make
```
or
```shell
yarn dev
```


## Start a HTTP tunnel forwarding to local port 3000

```
cd /Users/angelwang/Desktop/Application
./ngrok http 3000
```


## Frontend


|Page|Content|File|
|---|---|---|
|**TOP**|關於我們（About us）<br/>課程資訊（Course info）<br/>如何預約課程？（How to make an appointment?）|pages / index.tsx <br/>components/Header <br/>components/NavPills <br/>styles/Header<br/>styles/NavPills|
|**講師一覽（teachers）**| 預約講師(make an appointment）<br/>|pages / teachers.tsx|
|**課程費用（price）**| |pages / pricing.tsx |
|**常見問題（question）**| | |
|**聯絡我們（contact）**| | |
|**註冊/登入（register/login）**| 忘記密碼（forget password）|pages / login.tsx <br/>pages / register.tsx |



## Color


|Color|Img|Hex|RGB|Link|
|---|---|---|---|---|
|**primary**|<img src="https://www.colorhexa.com/b19c8f.png" width="100" height="100"/>|#b19c8f|rgb(177,156,143)|https://www.colorhexa.com/b19c8f|
|**primary_light1**|<img src="https://www.colorhexa.com/c6b7ad.png" width="100" height="100"/>|#c6b7ad|rgb(198,183,173)|https://www.colorhexa.com/c6b7ad|
|**primary_light2**|<img src="https://www.colorhexa.com/e4dad2.png" width="100" height="100"/>|#e4dad2|rgb(228,218,210)|https://www.colorhexa.com/e4dad2|
|**grey**|<img src="https://www.colorhexa.com/a4a09d.png" width="100" height="100"/>|#a4a09d|rgb(164,160,157)|https://www.colorhexa.com/a4a09d|
|**purple_g**|<img src="https://www.colorhexa.com/ded6f5.png" width="100" height="100"/>|#ded6f5|rgb(222,214,245)|https://www.colorhexa.com/ded6f5|
|**pink_g**|<img src="https://www.colorhexa.com/f5d6ed.png" width="100" height="100"/>|#f5d6ed|rgb(245,214,237)|https://www.colorhexa.com/f5d6ed|
|**green_g**|<img src="https://www.colorhexa.com/d6f5de.png" width="100" height="100"/>|#d6f5de|rgb(214,245,222)|https://www.colorhexa.com/d6f5de|
|**applegreen**|<img src="https://www.colorhexa.com/deff7e.png" width="100" height="100"/>|#deff7e|rgb(222,255,126)|https://www.colorhexa.com/deff7e|
|**applegreen_l**|<img src="https://www.colorhexa.com/f2ffcc.png" width="100" height="100"/>|#f2ffcc|rgb(242,255,204)|https://www.colorhexa.com/f2ffcc|
|**lake_g**|<img src="https://www.colorhexa.com/d1fefb.png" width="100" height="100"/>|#d1fefb|rgb(209,254,251)|https://www.colorhexa.com/d1fefb|
|**blue_b**|<img src="https://www.colorhexa.com/ccf2ff.png" width="100" height="100"/>|#ccf2ff|rgb(204,242,255)|https://www.colorhexa.com/ccf2ff|
|**purple_b**|<img src="https://www.colorhexa.com/e4daff.png" width="100" height="100"/>|#e4daff|rgb(245,214,255)|https://www.colorhexa.com/e4daff|
|**pink_b**|<img src="https://www.colorhexa.com/f5d6ff.png" width="100" height="100"/>|#f5d6ff|rgb(245,214,255)|https://www.colorhexa.com/f5d6ff|
|**orange**|<img src="https://www.colorhexa.com/ffda9c.png" width="100" height="100"/>|#ffda9c|rgb(255,218,156)|https://www.colorhexa.com/ffda9c|

<br/>

<br/>

# Integrate with backend
This is the backend stack for the Harajuku-class project.


## Install poetry (for backend)
```
curl -sSL https://raw.githubusercontent.com/python-poetry/poetry/master/get-poetry.py | python -
source $HOME/.poetry/env
```


## Install Homebrew
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```


## Before Setup
```
brew install postgresql@9.6.1
```


## Setup
1. change directory to ```harajuku-class/backend```
```
cd /Users/angelwang/Desktop/harajuku-class/backend
```
2. install

```
export PATH=/usr/local/Cellar/postgresql/9.6.1/bin:$PATH
poetry env remove $(poetry env info -p)/bin/python && poetry install
```
* If not work, run this:
```
xcode-select --install
env LDFLAGS="-I$(brew --prefix openssl)/include -L$(brew --prefix openssl)/lib" poetry install
```
Source: https://stackoverflow.com/questions/26288042/error-installing-psycopg2-library-not-found-for-lssl/39244687#39244687


## Reinstall Python
* Setting PATH for Python 3.9 (downloaded from https://www.python.org/downloads/)
```
nano ~/.bash_profile
```
```
# Setting PATH for Python 3.9
# The original version is saved in .bash_profile.pysave
PATH="/Library/Frameworks/Python.framework/Versions/3.9/bin:${PATH}"
export PATH
```

* Set default python to python3 each time
```
alias python=python3
```
or
```
set PATH ~/Library/Python/3.9/bin $PATH
```

Source:
https://www.codingforentrepreneurs.com/blog/changing-default-python-3-in-terminal-for-mac-os
https://flaviocopes.com/python-installation-macos/
https://levelup.gitconnected.com/a-guide-to-upgrade-your-python-to-3-9-44ccb3eae31a






