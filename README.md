# docker-compose

docker compose 설치
```
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```

docker compose 권한 부여
```
sudo chmod +x /usr/local/bin/docker-compose
```

Azure CLI 설치
```
apt install azure-cli
```

Azure 컨테이너 이미지 저장을 위한 ACR(Azure Container Registry) 생성
```
az group create --name user20acr --location eastus
```
