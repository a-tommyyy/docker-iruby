# Dockerのインストール
## 古いバージョンのdockerを削除

```bash
sudo yum remove docker \
                docker-client \
                docker-client-latest \
                docker-common \
                docker-latest \
                docker-latest-logrotate \
                docker-logrotate \
                docker-selinux \
                docker-engine-selinux \
                docker-engine
```

## yumリポジトリの更新

```bash
sudo yum install -y yum-utils \
                    device-mapper-persistent-data \
                    lvm2

sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
```

## docker-ceのインストール

```
sudo yum install docker-ce
```

## dockerサービスの起動

```
sudo systemctl start docker
```

