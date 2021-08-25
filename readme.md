## 概要

-   nuxtjs環境の構築

## 手順

ルートディレクトリ配下で`docker-compose build` <br>
成功したことを確認して`docker-compose up -d` <br>
`docker ps` コマンドで起動中のコンテナを確認
```
> docker ps
CONTAINER ID   IMAGE              COMMAND                  CREATED          STATUS          PORTS                                       NAMES
6e40db4af261   nuxt-docker_nuxt   "docker-entrypoint.s…"   52 seconds ago   Up 50 seconds   0.0.0.0:3000->3000/tcp, :::3000->3000/tcp   nuxt-docker_nuxt_1
```

`docker exec -it nuxt-docker_nuxt_1 bash`
でコンテナ内に入る。コンテナ内で

```
$ yarn create nuxt-app myApp
```

nuxtの初期設定項目が聞かれるので任意のものを選択

```
✨  Generating Nuxt.js project in myapp
? Project name: myapp
? Programming language: TypeScript
? Package manager: Yarn
? UI framework: Tailwind CSS
? Nuxt.js modules: Axios - Promise based HTTP client
? Linting tools: ESLint
? Testing framework: None
? Rendering mode: Single Page App
? Deployment target: Server (Node.js hosting)
? Development tools: (Press <space> to select, <a> to toggle all, <i> to invert selection)
? Continuous integration: None
? Version control system: Git
```

初期処理が終了すると上記`Project name`で入力した名前のフォルダ内にnuxtjsで必要なものが展開されている

```
$ cd myapp
$ yarn dev ##起動
```

起動完了したら http://localhost:3000/ へアクセスするとnuxtjsの初期画面が表示される

