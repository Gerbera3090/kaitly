FROM node:18-alpine

RUN npm install -g pnpm

WORKDIR /app

COPY . .

# 루트 디렉토리에서 의존성 설치
RUN pnpm install -r

WORKDIR /app/packages/frontend

# 포트 20064 노출
EXPOSE 20064

# dev 모드로 실행
CMD ["pnpm", "run", "dev"]
