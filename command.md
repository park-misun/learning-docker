
# docker 

docker 파일 생성
```
FROM ubuntu:18.04
MAINTAINER Demo example@demo.com

# Avoiding user interaction
ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update -y
RUN apt-get install -y apache2 # install Apache web server (Only ‘yes’)

EXPOSE 80

CMD ["apachectl", "-D", "FOREGROUND"]
```

docker 이미지 빌드
```
docker build -t user07httpd3 .
```

docker 이미지 빌드(docker hub up)
```
docker build -t alldaypass/user07newhttpd:1.0. .
```

docker 허브 접속
```
docker loging
```



# docker-compose

docker compose 설치
```
sudo curl -L "https://github.com/docker/compose/releases/download/1.29.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```

docker 설치
```
apt install docker.io
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
az group create --name myResourceGroup1 --location eastus
```

Azure ACR 생성
```
az acr create --resource-group myResourceGroup1 --name david20acrdemo --sku Basic
```

소스코드 다운로드
```
git clone https://github.com/Azure-Samples/azure-voting-app-redis.git
```

azure-voting-app-redis 로 이동 후 docker compose 실행
```
cd azure-voting-app-redis/
docker-compose up -d
```

리소스 정리
```
docker-compose down
```


ACR URL확인
```
az acr list --resource-group myResourceGroup1 --query "[].{acrLoginServer:loginServer}" --output table
```
