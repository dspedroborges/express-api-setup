# Express API with TS, Prisma and JWT

## Start the project

```shell
mkdir express-api && cd express-api
```

```shell
npm init -y
```

## Install libs

```shell
npm install express @prisma/client jsonwebtoken bcryptjs uuid dotenv
```

```shell
npm install -D typescript ts-node-dev @types/express @types/node prisma
```
## Start TS

```shell
npx tsc --init
```

## Start Prisma

```shell
npx prisma init
```

### tsconfig.json:

```json
{
  "compilerOptions": {
    "target": "es2020",
    "module": "commonjs",
    "rootDir": "./src",
    "outDir": "./dist",
    "strict": true,
    "esModuleInterop": true,
    "skipLibCheck": true,
    "forceConsistentCasingInFileNames": true,
    "sourceMap": true,
    "types": ["node", "express"]
  }
}
```

## Scripts to the package.json

```json
"scripts": {
  "dev": "ts-node-dev --respawn --transpile-only src/server.ts",
  "build": "tsc",
  "start": "node dist/server.js"
},
```
