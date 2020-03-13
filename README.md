# nodejs-typescript-web

## 全域安裝TS
* npm install typescript -g

## 安裝 TypeScript

* 安裝 TypeScript
    * npm install typescript -s-d
* 加入 TypeScript 類別庫
    * npm install @types/node -s-d
* 加入 TypeScript 的設定檔案 tsconfig.json
    * npx tsc - init

## 建立開發環境 Live Compile + Run

* 加入即時編譯模組 ts-node
    * npm install ts-node -s-d
* 加入 .ts 檔案儲存自動觸發 ts-node
    * npm install nodemon -s-d
* 設定 package.json
```
"scripts": {
    "start": "npm run build:live",
    "build:live": "nodemon --exec ./node_modules/.bin/ts-node -- ./app.ts",
    "build": "tsc app.ts"
}
```

## Production 編譯 js
> tsc 是編譯 .ts 到 .js 的編譯工具
* npm run build