# Berachain-Node-Build

1. 去阿里云、百度云或者搬瓦工租一台vps，家里闲置电脑/服务器也可以，要求16G内存, 200G硬盘, 6 核cpu
安装ubuntu 22.04 server或者desktop都行，开启openssh服务，硬件部分就搭建完了
2. 用FinalShell（其他ssh工具都可以）登录服务器
3. 安装Go 1.20+以上版本，我用的1.21.6：
```
cd ~
wget https://go.dev/dl/go1.21.6.linux-amd64.tar.gz
sudo tar -xzf go1.21.6.linux-amd64.tar.gz -C /usr/local/
echo 'export PATH=$PATH:/usr/local/go/bin' | tee -a ~/.bashrc
source ~/.bashrc
go install github.com/onsi/ginkgo/v2/ginkgo@v2.14.0
echo 'export PATH=$PATH:$(go env GOPATH)/bin' | tee -a ~/.bashrc
source ~/.bashrc
```
   
5. 安装以下软件：
```
sudo apt-get install jq -y
```
   
6. 安装Foundry：
```
curl -L https://foundry.paradigm.xyz | bash
source ~/.bashrc
foundryup
```

8. Clone源码并执行：
```
cd ~
git clone https://github.com/berachain/polaris
cd polaris
git checkout main
make test-unit
```
9. 启动测试网：
```
screen -S polaris
cd ~/polaris
make start
```

成功后出现以下界面：

![image](https://github.com/tujj99/Berachain-Node-Build/assets/53027340/4ae8869b-225e-4ede-9750-a87b761d16a3)

