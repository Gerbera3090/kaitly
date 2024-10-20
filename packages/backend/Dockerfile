# 1. Node.js 이미지를 사용
FROM node:18-alpine

# 2. pnpm 설치
RUN npm install -g pnpm

# 3. 컨테이너 내에서 사용할 작업 디렉토리 설정
WORKDIR /app

# 4. 로컬의 모든 파일을 컨테이너의 /app 폴더로 복사
COPY . .

# 5. 의존성 설치 (pnpm 사용)
RUN pnpm install

# 6. 애플리케이션 빌드 (NestJS의 경우, 별도의 빌드 단계 없이 실행)
# 7. 포트 노출
EXPOSE 21572

# 8. NestJS 애플리케이션 실행
CMD ["pnpm", "run", "start:dev"]
