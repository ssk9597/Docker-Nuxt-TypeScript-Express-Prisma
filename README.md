## DEV

### Frontend

・Nuxt.js

・Composition-API

・TypeScript

### Backend

・Node.js(Express)

・TypeScript

## 手順

### ① クローンする

```
git clone git@github.com:ssk9597/Docker-Nuxt-TypeScript-Express-Prisma.git
```

### ② ディレクトリに移動する

```
cd Docker-Nuxt-TypeScript-Express-Prisma
```

### ③ 作成するテーブルを決める

`api/prisma/schema.prisma`に作成したいテーブルを記載する

```
model User {
  id    Int    @id @default(autoincrement())
  name  String
  email String @unique
}
```

### ④`make nuxt`を実行して、Nuxt.js の作成と Docker の起動を行う

```
make nuxt
```

### ⑤`nuxt.config.js`と`.env`と`pages/index.vue`を修正してバックエンドとの通信を図る
