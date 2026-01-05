![Educational Project](https://img.shields.io/badge/Project%20Type-Educational-blue)
![Learning Project](https://img.shields.io/badge/Purpose-Learning-green)
# Test-fullstack-app
## Description
Learning fullstack web application consisting of frontend and backend services.
The project is designed to be run using Docker Compose from this main repository.
---
## Repositories
- [**Frontend**](https://github.com/Bitsulov/test-fullstack-app-frontend.git) - Web React Application
- [**Backend**](https://github.com/Bitsulov/test-fullstack-app-backend.git) - Spring boot Rest API Application
---
## Technologies Stack
- **Frontend:** React, TypeScript, Vite
- **Backend:** Java (Spring Boot)
- **Database:** PostgreSQL
- **Containerization:** Docker Compose
---
## Requirements
- **Docker**
- **Docker Compose**
> Local installation of Node.js, JDK or Maven is not required when running via Docker.
---
## Configuration
Create `.env` file(s) in the root of the project with variables:
1. `CRYPTO_KEY=`
    - Algorithm: AES-256
    - Base64-string
2. `API_BASE=`
    - dev: `http://localhost:8080/api`
    - prod: `/api`
3. `POSTGRES_URL=` - JDBC Postgres connection URL
4. `DB_NAME=`
5. `POSTGRES_USERNAME=`
6. `POSTGRES_PASSWORD=`
7. `JWT_ACCESS_TIME=` - JWT access token expires in (milliseconds)
8. `JWT_REFRESH_TIME=` - JWT refresh token expires in (milliseconds)
9. `JWT_SECRET=` - HMAC secret key used for JWT signing (HS256 / HS512)
---
## Installation and Run
### Development
```bash
  docker compose -p <COMPOSE_NAME_DEV> -f docker-compose-dev.yml --env-file <YOUR_DEV_ENV_FILE> up -d
```
### Production
```bash
  docker compose -p <COMPOSE_NAME_PROD> -f docker-compose-prod.yml --env-file <YOUR_PROD_ENV_FILE> up -d
```
---
## Links
- Frontend repository: [Test-fullstack-app-frontend](https://github.com/Bitsulov/test-fullstack-app-frontend.git)
- Backend repository: [Test-fullstack-app-backend](https://github.com/Bitsulov/test-fullstack-app-backend.git)
