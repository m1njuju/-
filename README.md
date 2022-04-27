# frontend

## Project setup
```
cd frontend
npm install
cd ..
cd backend
npm install
```

# backend

### Compiles and hot-reloads for development
### 반드시 backend 폴더에서 실행
### 첫 시작은 SET DEBUG=backend:* & npm start 으로 설정
```
SET DEBUG=backend:* & npm start
//or
node ./bin/www
//or
nodemon ./bin/www
```

### Compiles and minifies for production
### 프론트엔드를 수정했다면 frontend 폴더에서 빌드
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
