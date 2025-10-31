# Express API with TS, Prisma and JWT

## Start the project

```shell
mkdir express-api && cd express-api
```

```shell
npm init -y
```

## In package.json, change main from index.js to

```json
"main": "src/server.ts",
```

## And below "main", add

```json
"type": "module"
```

## vercel.json

```json
{
  "version": 2,
  "builds": [
    { "src": "dist/server.js", "use": "@vercel/node" }
  ],
  "routes": [
    { "src": "/(.*)", "dest": "dist/server.js" }
  ]
}
```

## Install libs

```shell
npm install express @prisma/client uuid dotenv
```

```shell
npm install jsonwebtoken @types/jsonwebtoken
```

```shell
npm install bcryptjs @types/bcryptjs
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

### Uncomment these lines from the tsconfig.json file:

```json
"rootDir": "./src",
"outDir": "./dist",
```

## Scripts to the package.json

```json
{
    "dev": "tsx watch src/server.ts",
    "build": "tsc",
    "start": "node dist/server.js"
}
```
