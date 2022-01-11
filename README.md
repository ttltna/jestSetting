## Frontend - Perset

### npm init

- [x] npm init

    - 명령어
        - npm init
        - npm init -y

### gitignore

- [x] gitignore

    - extension -> gitignore 검색 (가장 조회수 많은거 다운)
    - ctrl + shift + p -> add gitignore 검색
    - node 검색 -> 실행

### nodemon

- [x] nodemon
    - npm install -D nodemon
    ```json
        "scripts":{
            "start": "nodemon ./index.js"
        },
    ```

    - npm (run) start

### babel

- [x] babel
    -npm i -D @babel/core @babel/preset-env @babel/cli @babel/node
        -만약 오류 발생시 npm -g install -D @babel/core @babel/preset-env
        @babel/cli @babel/node
    -루트 디렉터리에 **babel.config.json** 파일 생성
    ```json
        {
            "presets": ["@babel/preset-env"]
        }
    ```
    ```json
        "scripts": {
            "start": "nodemon --exac babel-node ./index.js"
        },
    ```
    - npm (run) start

### ESlint & Prettier

- [x] ESlint
- [x] Prettier

    - npm install eslint -D
    - npx eslint --init
    - lint 설정
    - npm install -D eslint-config-prettier eslint-config-tui eslint-plugin-prettier
    - npm install -D prettier
    ```json
        "lint": "eslint ./index.js --fix"
    ```

    - .eslintrc.js
        ```javascript
            module.exports = {
                parserOptions: {
                    sourceType: "module"
                },
                env: {
                    browser: true,
                    es6:true
                },
                extends: ['eslint-config-tui', 'prettier'],
                plugins: ["prettier"],
                rules: {
                    "prettier/prettier": "error",
                }
            }
        ```

### Jest

- [x] Jest
    - npm install -D jest babel-jest
    - jest.config.json 파일 생성
    ```json
        {
            "clearMocks": true,
            "collectCoverage": true,
            "verbose": true,
            "testEnvironment": "jsdom"
        }
    ```
    -script 수정
    ```json
        "scripts": {
            "test:jest": "jest --watchAll --collect[=true] --logHeapUsage"
        }
    ```
    - test 폴더 하위에 (원하는 파일명).test.js 파일 생성
    - **주의사항!!**
        ```javascript
            // export할 함수 || 객체가 한개일 경우
            const sum = (a, b) => {
                return a + b;
            };

            export default sum;

            // 테스트 파일
            import sum from "../src/index.js";
                // 테스트 코드
        ```
        ```javascript
            // export할 함수 || 객체가 다수일 경우
            export const sum = (a, b) => {
                return a + b;
            };

            export const minus = (a, b) => {
                return a - b;
            };

            // 테스트 파일
            import {sum, minus} from "../src/index.js";
                //테스트 코드
        ```

### parcel

- [x] parcel
    - npm install --save-dev parcel
    - npx parcel src/index.html (만약 src 폴더 하위에 index.html 파일이 있다면)
    ```json
    "srcitps": {
        "start": "parcel",
        "build": "parcel build"
    },
    ```
    - script 실행시 localhost:1234가 호출 됐다면 ctrl + click

### Cypress

- [ ] Cypress