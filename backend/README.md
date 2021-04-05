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
brew install postgresql@9.6
```


## Setup
1. change directory to ```harajuku-class/backend```
```
cd /Users/angelwang/Desktop/harajuku-class/backend
```
2. install

```
export PATH=/Library/PostgreSQL/9.6/bin:$PATH
poetry env remove $(poetry env info -p)/bin/python && poetry install
```
export PATH=/usr/local/Cellar/postgresql/9.6.1/bin:$PATH


* If not work, run this:
```
xcode-select --install
env LDFLAGS="-I$(brew --prefix openssl)/include -L$(brew --prefix openssl)/lib" poetry install
```
Source: 
<br/>
https://stackoverflow.com/questions/26288042/error-installing-psycopg2-library-not-found-for-lssl/39244687#39244687




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
<br/>
https://www.codingforentrepreneurs.com/blog/changing-default-python-3-in-terminal-for-mac-os
<br/>
https://flaviocopes.com/python-installation-macos/
<br/>
https://levelup.gitconnected.com/a-guide-to-upgrade-your-python-to-3-9-44ccb3eae31a




## PostgreSQL
1. 查詢 Port:3000 狀態，若被 postgre 佔用
```
sudo lsof -i:3000 
```
2. 更改 postgresql.conf 的 port
```
sudo -u postgres nano /Library/PostgreSQL/9.6/data/postgresql.conf
```
```
# - Connection Settings - 
listen_addresses = ‘*’
port = 5432
```
3. restart
```
sudo su postgres -c "/Library/PostgreSQL/9.6/bin/pg_ctl restart -D /Library/PostgreSQL/9.6/data"
```

Source:
<br/>
https://www.jamescoyle.net/how-to/3019-how-to-change-the-listening-port-for-postgresql-database
<br/>
https://dba.stackexchange.com/questions/220700/how-to-edit-postgresql-conf-with-pgadmin-4
<br/>
https://stackoverflow.com/questions/7990539/how-to-restart-postgresql-server-on-macos


