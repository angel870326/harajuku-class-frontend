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
**3. install react-swipeable-views**
```
npm install --save react-swipeable-views
``` 


## Developing server

```shell
make
```
or
```shell
yarn dev
```


## Frontend


|Frontend|File|
|---|---|
|**TOP**|pages / index.tsx <br/>components/Header <br/>styles/Header|
|**講師一覽（teachers）**| |
|**課程費用（price）**| |
|**常見問題（question）**| |
|**聯絡我們（contact）**| |
|**註冊/登入（login）**| |



