# Harajuku-class 


## Clone
```
cd /Users/angelwang/Desktop
git clone https://github.com/aeroworks-io/harajuku-class.git
```
```
git clone https://github.com/aeroworks-io/harajuku-class.git -b angel870326-patch-1
```


## Backend Setup
1. change directory to ```harajuku-class/backend```
```
cd /Users/angelwang/Desktop/harajuku-class/backend
```
2. install

```
export PATH=/Library/PostgreSQL/9.6/bin:$PATH
poetry env remove $(poetry env info -p)/bin/python && poetry install
```

* If not work, run this:
```
env LDFLAGS="-I$(brew --prefix openssl)/include -L$(brew --prefix openssl)/lib" poetry install
```


## Frontend Setup
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


## Developing server

```shell
make
```


## Start a HTTP tunnel forwarding to local port 3000

```
cd /Users/angelwang/Desktop/Application
./ngrok http 3000
```


