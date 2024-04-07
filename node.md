# development Dependency
如果一个模块在运行的时候并不需要，仅仅在开发时才需要，就可以放到devDependencies中。
这样，正式打包发布时，devDependencies的包不会被包含进来。
If a module is not needed at runtime, but only at development time, it can be placed in devDependencies.
This way, packages from devDependencies will not be included in the official package release.

# show modules installed in global
``` npm list -g --depth=0 ```

# npx command
1. 首先搜索当前目录下的node_modules
2. 然后在全局进行搜索
3. 临时下载一个模块，最后卸载掉

# NPM NRM NVM CNPM N NPX definition
NPM node package manager
NRM node registry manager
NVM node version manager
commen useful command:  ``` xxx --help ```
## about nrm
```npm config ls```If the node is win32 program, Then try to change a file(See the error information)
``` const NRMRC = path.join(process.env.HOME, '.nrmrc')(Delete);```
``` const NRMRC = path.join(process.env.USERPROFILE, '.nrmrc')(New);```

# NVM relative command
``` nvm proxy http://example.com:8080 ``` set the proxy

# uninstall node.js and relative package
here is the [link][link1]

# remove the node_modules in current project
``` npm install rimraf -g ```
``` rimraf node_modules  ```

# npm install 
``` npm i [-g] [-d] [-s] ```
i indicates install
g means --global
s is --save   It will write the package name to the dependency in package.json
d means --save-dev   It will write the pacjage name to the dependency in package.json
The package will be added to the node_modules dir.If there is no parameter(d|s|g)

# get the command line parameter
``` process.argv[index] ``` in genereal,index is greater than 1.

# About package.json file
## ``` npm package name: major.minor.patch ```
major: New architechure.And in general, it mot be compatible with the old version
minor: Add some new features as planed
patch: fix some bugs

## ``` npm run script ```
In VUE, you can customize .env.name file to indicate the profile. So you can configure multiple environments.For instance, you can set a dev-mock file for simulation data. 

## ```yarn upgrade-interactive --latest```
upgrade the package

# npm package
## eslint

### eslint is a format tool
There is an [article][link2] about the tool

## prettier
format tool

## tsx
Not a file format. It is a useful tool to execute the ts directly.

## fp-ts
support Option syntax like Rust.

## zx
Write more powerful script in commad line.
But you must verify that your env support wsl.


[link1]: https://blog.csdn.net/lewky_liu/article/details/87959839
[link2]: http://obkoro1.com/web_accumulate/accumulate/tool/Eslint%E8%87%AA%E5%8A%A8%E4%BF%AE%E5%A4%8D%E6%A0%BC%E5%BC%8F%E9%94%99%E8%AF%AF.html#vscode%E4%BF%9D%E5%AD%98%E6%97%B6%E8%87%AA%E5%8A%A8%E4%BF%AE%E5%A4%8Deslint%E9%94%99%E8%AF%AF