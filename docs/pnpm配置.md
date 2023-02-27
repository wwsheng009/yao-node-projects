# 配置 pnpm

```sh
mkdir yao-node-projects
cd yao-node-projects

# 构建根目录项目 & 添加 workspace 配置
pnpm init -y

#在根目录建立一个packages目录来使用pnpm workspace
touch pnpm-workspace.yaml
# 构建子项目
mkdir packages
cd packages


mkdir yao-node-client
mkdir yao-node-server

#给yao-node-server项目增加依赖
cd yao-node-server
pnpm add yao-node-client --workspace

#或是在根目录
#使用以下命令，给yao-node-template添加yao-node-client依赖。
#–filter 后加上项目名称是指定对某个项目进行操作。
pnpm add yao-node-client --workspace --filter yao-node-server

```

turbo

```sh
pnpm i -D turbo -w
```

app

```sh
cd packages

mkdir yao-node-app
cd yao-node-app
pnpm init
```
