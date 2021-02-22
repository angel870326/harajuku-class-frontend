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


|Page|Content|File|
|---|---|---|
|**TOP**|關於我們（About us）<br/>課程費用（price）-> plan to change it to 課程資訊（course info: time and price）<br/>如何預約課程？（How to make an appointment?）|pages / index.tsx <br/>components/Header <br/>components/NavPills <br/>styles/Header<br/>styles/NavPills|
|**講師一覽（teachers）**| | |
|**課程費用（price）**| | |
|**常見問題（question）**| | |
|**聯絡我們（contact）**| | |
|**註冊/登入（login）**| | |



## Color


|Color|Img|Hex|RGB|Link|
|---|---|---|---|---|
|**primary**|<img src="https://www.colorhexa.com/b19c8f.png" width="100" height="100"/>|#b19c8f|rgb(177,156,143)|https://www.colorhexa.com/b19c8f|
|**primary_light**|<img src="https://www.colorhexa.com/c6b7ad.png" width="100" height="100"/>|#c6b7ad|rgb(198,183,173)|https://www.colorhexa.com/c6b7ad|
|**purple**|<img src="https://www.colorhexa.com/ded6f5.png" width="100" height="100"/>|#ded6f5|rgb(222,214,245)|https://www.colorhexa.com/ded6f5|
|**pink**|<img src="https://www.colorhexa.com/f5d6ed.png" width="100" height="100"/>|#f5d6ed|rgb(245,214,237)|https://www.colorhexa.com/f5d6ed|
|**green**|<img src="https://www.colorhexa.com/d6f5de.png" width="100" height="100"/>|#d6f5de|rgb(214,245,222)|https://www.colorhexa.com/d6f5de|
|**lightgreen**|<img src="https://www.colorhexa.com/edf5d6.png" width="100" height="100"/>| | | |
|**blue**|<img src="https://www.colorhexa.com/d6edf5.png" width="100" height="100"/>| | | |

