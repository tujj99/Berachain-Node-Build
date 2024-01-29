# Berachain-Node-Build

Linux OS
amd64 or arm64 CPU
4 cores
16GB RAM
500GB storage

```
cd $HOME
sudo apt-get install golang -y
```
![image](https://github.com/tujj99/Berachain-Node-Build/assets/53027340/cada2033-ebc7-45a1-9d15-1737d193a7fa)

```
export PATH=$PATH:/usr/local/go/bin
export PATH=$PATH:$(go env GOPATH)/bin
```
![image](https://github.com/tujj99/Berachain-Node-Build/assets/53027340/e4915bd4-027d-4278-874f-b20f47e6ca97)

```
git clone https://github.com/berachain/polaris
cd polaris
git checkout main
go run magefiles/setup/setup.go
```
![image](https://github.com/tujj99/Berachain-Node-Build/assets/53027340/0dec774a-09a4-43fa-8126-d8d179d207be)

