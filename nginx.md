<!--
 * @Author: Lmmqxyx
 * @Date: 2022-02-10 13:47:27
 * @LastEditors: Please set LastEditors
 * @LastEditTime: 2022-04-08 17:40:15
 * @FilePath: \Learning_Note\nginx.md
 * @Description: 
-->
# The nginx core concepts
## 1. Transparent proxy
## 2. Load balance
## 3. High availability

## Common proxy concepts
### 1. Forward Proxy
The proxy is setted by client and the users know their requests are transferred

### 2. Reverse Proxy
The proxy is used by server and people can not know if the flow goes through the proxy server

# frequent commaand
``` nginx -s reload ```
restart the nginx server

``` nginx -t ```
test the nginx conf

# nginx.conf files
```mime.types``` indicates the different types.
``` default_type application/octet-stream```

# nginx deploy a html page
## deploy prefix router.
read these chapters [link1] [link2] [link3] [link4]
Pay more attention to the path.



[link1]: https://www.hangge.com/blog/cache/detail_3140.html
[link2]: https://juejin.cn/post/6920046170110689293
[link3]: https://segmentfault.com/a/1190000039046545
[link4]: https://juejin.cn/post/6926785971287490573