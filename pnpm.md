## add a node version
### ```pnpm env use --global latest```
Install the latest version of Node.js

### ``` pnpm env use --global 16``` 
Install Node.js v16

### ```pnpm env use --global lts```
Install the LTS version of Node.js

### ``` pnpm env remove --global 14.0.0```
remove the specific node version.

### Print remotely available Node.js v16 specific versions:
```pnpm env list --remote 16[option]```

## opearaations about package
### ``` pnpm add -g package```
add a package globally.

### ``` pnpm up ```
upgrade the packages of the current project.

## pnpm upgrade itself
``` pnpm add -g @pnpm/exe ```

## pnpm set or get registry
``` pnpm config set registry <registry-url> ```
https://registry.npm.taobao.org/ 

## filter setting
```pnpm --filter packageName run start```

## `--recursive` to run relative command


与 yarn 相比有什么优缺点
优点， pnpm层级依赖是正确的， yarn 全部平铺开是错误的

缺点  在nextjs 中，结合 workspace 功能，pnpm必须做一些额外配置，才能确保目录访问正确
