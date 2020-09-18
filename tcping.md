# install TCPING in linux
in the <u>tcping</u> index html, download the package
```
tar zxvf tcping-1.3.5.tar.gz
cd tcping-1.3.5
yum install -y gcc
make 
cp tcping /usr/bin/
```

# the parameter in tcping.exe
-4，优先使用IPv4

-6，优先使用IPv6

-h，使用http模式

-u，与-h命令连用，每一行输出目标的url

-t，让命令持续运行，直到使用ctrl + c指令退出

-n 数字，发送命令的次数，默认4次

-i 数字，发送ping命令的时间间隔，默认1s，可以为小数

-w 数字，等待响应的时间间隔，默认2s，可以为小数

-d，使输出的每一行显示时间和日期

-f，强制ping命令至少发送一个比特（byte）

-g 数字，失败指定次就放弃（注意默认是80端口，若其他端口没开也算失败）

-b 数字，开启蜂鸣器，参数4会一直响铃

-c，只显示改变的信息（ping时间很短一般不会改变）

-r 数字，每发送指定个数据包，就重新查找主机一次（通过DNS或路由查找）

-s，ping通就立即退出

-v，显示版本信息

-j，使用默认的方法，求ping的均值减小波动，网络有一定的不稳定性时，用此参数可以减小波动

-js 数字，用指定个实例求平均值减小波动，使用这个参数，系统会tcping 指定次，然后求出平均值作为一次结果显示，减小波动

–tee file_path，将结果输出到指定位置，tcping –tee /data/test.txt192.168.0.100，会把ping的结果保存在/data下的test文件中

–file，从文件中获得ping的来源；在/data下新建一个test.txt文件，并输入要tcping的所有ip或域名，一行一个，然后执行命令tcping –file /data/test.txt，就会依次tcping文件中指定的地址

destination，可以是DNS地址、IP地址、URL（需要使用-h，http模式）。使用http模式时，不要加https//或:port，例如：tcping http://www.elifulkerson.com:8080/index.html就会失败，使用tcping www.elifulkerson.com/index.html 8080就会成功

port 数字，指定tcp端口（1-65535），如果不指定，默认是80

–header，在头部显示时间和日期，与–tee显示的格式差不多

–block，tcping不通的等待时间，默认是20秒（很长）。–block可以把-w参数冲突掉 ，例如tcping --block www.baiu.com网址不正确，显然tcpping不通，默认会等待20s 。 tcping -w 0.5 –block www.baiu.com还是会等20s，而不是0.5s，因为–block选项会把-w选项冲突掉。

