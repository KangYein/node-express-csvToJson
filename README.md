package.json 파일 생성 등의 프로젝트 생성

`npm init -y`
개발에 필요한 패키지 설치

`npm i -D typescript ts-node nodemon`
tsconfig.json 파일 생성을 위해 다음 명령 수행

`npx tsc --init`
tsconfig.json에 다음 내용 추가

{
  ...
  "target": "es6",
  "module": "commonjs",
  "outDir": "./dist",
  "rootDir": "./src",
  "strict": true,
  "moduleResolution": "node",
  "esModuleInterop": true,
  ...
}
dist와 src 폴더를 생성하고 src에 index.ts 파일 생성

packagejson에 다음 내용 추가

{
  ...
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "start": "node dist/index.js",
    "build": "tsc -p .",
    "dev": "nodemon --watch \"src/**/*.ts\" --exec \"ts-node\" src/index.ts"
  },
  ...
}

개발 시작

`npm run dev` 

localhost:4000

http://localhost:4000/public/list


csv -> json

npm install csv-parser
