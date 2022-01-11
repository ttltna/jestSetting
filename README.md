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
    -npm install -D nodemon
    ```json
        "scripts":{
            "start": "nodemon ./index.js"
        },
    ```

    -npm (run) start

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

- [ ] ESlint
- [ ] Prettier
- [ ] Jest
- [ ] Cypress