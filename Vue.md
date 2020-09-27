
# vue react和原生H5开发的不同
原生更有利于做SEO

# 大型项目中的数据流
子组件的数据可以在父组件创建的时候进行请求与加载

特别是子组件初始设置为false的情况下，可以让用户无感知加载

带来的编码问题就是，子组件请求数据的方法，在父组件中重写。

并且在父组件中请求好后，先赋值给子组件同名变量，父组件也设置一个同名变量

之后通过ref的方式传递给子组件。子组件加载好方法

# 项目崩溃的解决思路
可以在package.json文件中，按照如下方法设置serve属性，可以解决前端大型项目中内存溢出问题,不同框架解决思路大同小异。具体可以搜索一下
"serve": "node --max_old_space_size=4096 node_modules/@vue/cli-service/bin/vue-cli-service.js serve ",
``` FATAL ERROR: Ineffective mark-compacts near heap limit Allocation failed - JavaScript heap out of memory ```

# 当生命周期函数没有执行的时候，切记要记得检查大括号的位置

# 注意组件嵌套的时候，记得定时清空缓存，刷新浏览器，重新获取数据

# 当页面卡死的时候，注意查看是否有网络请求，再来判断是前端问题还是后端问题

# Object.prototype.toString.call() 判断变量类型的唯一推荐的正确方法

# 后端返回的数据不是总是可靠的，实际开发中要考虑兼容性

# 前端设置代理，解决跨域类似问题后，注意要重新启动整个项目，否则请求地址不生效。 相应的也需要后端配合，查看是否有前端请求。尽量避免此类防呆问题