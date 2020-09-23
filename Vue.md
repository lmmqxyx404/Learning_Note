
子组件的数据可以在父组件创建的时候进行请求与加载

特别是子组件初始设置为false的情况下，可以让用户无感知加载

带来的编码问题就是，子组件请求数据的方法，在父组件中重写。

并且在父组件中请求好后，先赋值给子组件同名变量，父组件也设置一个同名变量

之后通过ref的方式传递给子组件。子组件加载好方法

可以在package.json文件中，按照如下方法设置serve属性，可以解决前端大型项目中内存溢出问题,不同框架解决思路大同小异。具体可以搜索一下
"serve": "node --max_old_space_size=4096 node_modules/@vue/cli-service/bin/vue-cli-service.js serve ",
``` FATAL ERROR: Ineffective mark-compacts near heap limit Allocation failed - JavaScript heap out of memory ```

# 当生命周期函数没有执行的时候，切记要记得检查大括号的位置

# 注意组件嵌套的时候，记得定时清空缓存，刷新浏览器，重新获取数据