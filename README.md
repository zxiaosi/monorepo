## lerna8-npm-workspaces-umi

### 开启 `npm workspaces`

- `lerna.json` 中添加下面配置

  ```json
  {
    "npmClient": "npm",
    "packages": ["packages/*"]
  }
  ```

- `package.json` 中添加下面配置

  ```json
  {
    "workspaces": ["packages/*"]
  }
  ```

### 注意：`packages` 下的项目中每个包的 `package.json` 都要配置 `name`，否则会报错

### 常用命令

```bash
# 安装依赖
npm install

# 启动项目
npm run dev -w=app
npm run dev --workspace=app
npm run dev --workspace=demo1 --workspace=demo2
lerna run dev --scope app

# 所有项目安装依赖
npm i typescript

## 安装某个项目的依赖
npm i typescript -w=app
npm i typescript -D -w=app
npm install typescript --workspace=app
```

## 参考文档

- [lerna+pnpm+workspaces](https://www.lernajs.cn/docs/recipes/using-pnpm-with-lerna#getting-started)

```

```
