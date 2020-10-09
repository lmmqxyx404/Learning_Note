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


# NVM relative command
``` nvm proxy http://example.com:8080 ``` set the proxy

# uninstall node.js and relative package
here is the [link][link1]

# remove the node_modules in current project
``` npm install rimraf -g ```
``` rimraf node_modules  ```

[link1]: https://blog.csdn.net/lewky_liu/article/details/87959839