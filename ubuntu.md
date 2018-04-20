# Dockerのインストール
[ここ見てね(公式)](https://docs.docker.com/install/linux/docker-ce/ubuntu/)
## 古いバージョンのdockerを削除

```bash
sudo apt-get remove docker docker-engine docker.io
```

## yumリポジトリの更新

```bash
sudo apt-get update

sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    software-properties-common

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

sudo apt-key fingerprint 0EBFCD88

sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"
```

## docker-ceのインストール

```bash
sudsudo apt-get install docker-ce
```
