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
1. change directory to ```harajuku-class```
```
cd /Users/angelwang/Desktop/harajuku-class
```
2. run
```shell
make
```


## For Credit Card
1. create ```backend/.env``` and add this:
```
CODECOV_TOKEN=
STRIPE_API_KEY=sk_test_51IBWjhE4Xd0vI48XHDJBFbw4gYGSyFCG0Qk4g1whQjRDDgqWZRyoU2he7PVRDXhWL08lgSE2sJ3p3DhNsU3JrqFr003jIPRz43
```


## Frontend Testing
1. change directory to ```harajuku-class/frontend```
```
cd /Users/angelwang/Desktop/harajuku-class/frontend
```
2. test all
```
yarn test-all
```
3. update snapshot
```
yarn test -u
```


## Start a HTTP tunnel forwarding to local port 3000

```
cd /Users/angelwang/Desktop/Application
./ngrok http 3000
```


