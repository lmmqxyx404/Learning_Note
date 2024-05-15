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