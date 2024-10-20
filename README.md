# 실행 방법

### 개발 환경

```
docker-compose -f docker-compose.yml -f docker-compose.dev.yml up --build
```

개발환경과 mysql 컨테이너를 동시에 실행합니다.

### 배포 환경 (애플리케이션)

```
docker-compose -f docker-compose.yml -f docker-compose.prod.yml up --build
```

배포 환경 애플리케이션 컨테이너를 생성 후 실행합니다.

### 배포 환경 (db)

```
docker-compose -f docker-compose.mysql.yml up -d
```

배포 환경 데이터베이스 (mysql) 컨테이너를 실행합니다.
배포 환경에서는 데이터베이스를 많이 실행할 일이 없으므로 따로 사용합니다.
