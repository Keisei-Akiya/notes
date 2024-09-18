---
Author: "Keisei Akiya"
date: 2024-09-18
tag:
  [
    "TypeScript",
    "Node.js",
    "Backend",
    "Server",
    "nodemon",
    "Express",
    "ES Module",
  ]
---

# How to start server with TypeScript and Node.js

I show you to start server with TypeScript and Node.js.

I use ES Module.

## package.json

```json
{
  "name": "08_bookshelf_backend_ts",
  "version": "1.0.0",
  "main": "dist/server/app.js",
  "type": "module",
  "scripts": {
    "start": "node dist/app.js",
    "build": "tsc",
    "dev": "tsx src/app.ts"
  },
  "ts-node": {
    "esm": true,
    "experimentalSpecifierResolution": "node"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "dependencies": {
    "express": "^4.21.0"
  },
  "devDependencies": {
    "@types/cors": "^2.8.17",
    "@types/express": "^4.17.21",
    "@types/node": "^22.5.5",
    "nodemon": "^3.1.5",
    "ts-node": "^10.9.2",
    "ts-node-dev": "^2.0.0",
    "tsx": "^4.19.1",
    "typescript": "^5.6.2"
  },
  "description": ""
}
```

## tsconfig.json

```json
{
  "compilerOptions": {
    "target": "ESNext",
    "module": "ESNext",
    "moduleResolution": "Node",
    "strict": true,
    "esModuleInterop": true,
    "skipLibCheck": true,
    "forceConsistentCasingInFileNames": true,
    "outDir": "./dist",
    "rootDir": "./src"
  },
  "include": ["src/**/*"],
  "exclude": ["node_modules", "**/*.spec.ts"]
}
```

## app.ts

`app.ts`file is in `my-project/src/app.ts`

```typescript
import express, { NextFunction, Request, Response } from "express";

const app = express();
const PORT = process.env.PORT || 8080;

app.use(express.json());

app.listen(PORT, () => {
  console.log(`Server is running on port: http://localhost:${PORT}`);
});
```
