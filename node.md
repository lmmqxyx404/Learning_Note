# development Dependency
如果一个模块在运行的时候并不需要，仅仅在开发时才需要，就可以放到devDependencies中。
这样，正式打包发布时，devDependencies的包不会被包含进来。

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

[link1]: https://blog.csdn.net/lewky_liu/article/details/87959839