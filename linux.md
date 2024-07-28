# Ubuntu diary (based on Ubuntu22.04 LTS)

##  day1
### change the source
The default source address is not suitable for Chinese uses.So you'd better to change it.
<b>There are two ways:</b>
 - 1. change the config files(deprecated)
```
sudo vi /etc/apt/sources.list
```
- 2. use the GUI

### set proxy
1. set global proxy
You can set global proxy by changing the Settings/Network/Network Proxy.
You can use the following command to check your behaviour.
``` echo $https_proxy ```

2. set apt proxy
This is slightly more complex.
[This article][proxy] would help you a lot
When you complete relatice settings.Try the followings commands
``` sudo apt update && sudo apt upgrade ```
``` export ``` Show the global variable.
``` env ```
``` printenv ```
``` sudo vim /etc/environment ```
set proxy for all users

pay attention to delete the proxy if you do not want to use it.

## day2
### install the amd drives
I suffered a lot.

[This Chinese article][article] really helped a lot.
[Here][original] is the original author, Thanks a lot.
And if you must solve the software version problem.
Try the following command (pay attention to the =)
``` sudo apt install libc6=2.35-0ubuntu3 ```

## day3
#### about shell 
remember to add the shell file header
``` #!/bin/bash ```

#### adjust the default boot menu
注意，进入recovery模式，可以调整启动顺序

## day4
#### ctrl+alt+t open the shell
the default path is `/home/user_name/`.

## day5
#### soft and hard link

## day6 learn to write systemd files
##### 1. write down the service file(named first)
basic systemd service:
```
[Unit]
Description=my first service

[Service]
ExecStart=/bin/bash /user/xxx/Desktop/test.sh

# set for add to start menu
[Install]
WantedBy=multi-user.target
```
##### 2. move the service file to /etc/systemd/system
##### 3. ```systemctl daemon-reload```
##### 4. ```systemctl start first.service```
##### 5. ```systemctl status first.service```
##### 6. ```systemctl stop first.service```
##### 7. ```systemctl enable first.service```
##### 8. ```systemctl disable first.service```

## day7 study crontab(cron table)

## day8 clear the cargo cache
``` rm -rf .cargo/.package-cache ```
This can be useful for cargo blocked.

## day9 about ipv6
` vim /etc/gai.conf `
` sudo systemctl restart systemd-networkd `
Set the values of the relevant properties so that IPv6 is prioritized over IPv4 access.

## day10 solve the problem GLIBC_2.18 not found
upgrade the os.

## day11 get ip
```sudo dhclient interface(could be ignored)```

## day12 netplan
```sudo apt-get install netplan.io```
```sudo netplan apply```
Netplan is an indispensable software, without which there would be no related icons on the dock.

## day13 about ubuntu-desktop
If you mistakenly delete some dependencies, it's very likely that you will damage your desktop environment,
resulting in being unable to access the GUI subsequently, and can only enter the shell.
So you need to reinstall the `ubuntu-desktop`

I want to use python3.11, so i remove the python3.10 by mistake.Then I can not enter ubuntu22.04.
And get the error:
```Bluetooth: hci0: Malformed MSFT vendor event: 0x02```
Then I set the network use the `day11` knowledge first.
Secondly, I install the `ubuntu-desktop` to solve the problem

## day14 history
you can use `!index` to run the relative command.

## day15 file system
device->partition->mount point
each partition could be different file system type(`nfts` `ext4`)
each device could be splited to different partition

#### before you operate the partition(resize), you should unmount the partition.
so you cannot resize your partition basically.Because the partition is in used.

## top
The command can help us get system running information

## who(ami)
The command can help us know the current onlined user

## ```pkill -kill -t pts/2```
This command can help us kill the pts/2

## <font color=#880000> Centos7 </font>

 - #### frecuent software command
   - `yum install softwarename`   install target software
   - `yum list`   show installed software
   - `yum update`   update software
   - `yum remove softwarename`   remove software

## vmvare network setting
nat
host only
direct link

## set no password login
0. pay attention to the file permissions.
   The id_rsa (private) should be 600.
1. get the user id_rsa.pub key
2. try to put the content to the server ```~/.ssh/authorized_keys```

3. ### server ssh config files    ``` /etc/ssh/sshd_config ```
   - ```
        # useRsA verify
        RSAAuthentication yes
        PubkeyAuthentication yes
        # Do not allow the password
        PasswordAuthentication no
        # select filePath
        AuthorsizedKeysFile .ssh/authorized_keys
      ```

   - you can specify the ssh port in the file
4. restart the ssh service
   ``` /sbin/service sshd restart ```

5. test the ssh connection problem
   ```ssh -Tvvv git@github.com``` connect to the specofic server address and print debug info..      4

6. use rsa in a new machine.
pay attention to delete the knownhost files.

## get the linux system information
```cat /etc/xxx-release```
```uname -a```
```lshw``` show the all hardware
```lsmem``` show the memory info

## set the site
Keep in mind that port can only be used by one application.Otherwise it will be conflicted.

# linux tools
## ```nftables```
This tool is used for dealing with the data. nf means net filter.

# shell scripts
- ## type 
  This command can test whether the input command is a builtin.
  - ### builtin
    `cd` `pwd` `kill`
- ## read
  the command can read the input from the user and ```enter``` can break the string.
  There is a command named ```read-host```  as ```read```

- ## echo
  output the content. 

  ```
  a="hello"
  echo "$a world"
  ```
- ## ``` nohup script & ```
  keep in mind that the path must be absolute.

- ## ```ctrl+r```

  input former command fastly
- ## ``` xclip```
  ``` command | xclip -selection clipboard```
# about service
```
重新加载service文件：systemctl daemon-reload

启动一个服务：systemctl start nginx-1.13.0.service

关闭一个服务：systemctl stop nginx-1.13.0.service

重启一个服务：systemctl restart nginx-1.13.0.service

显示一个服务的状态：systemctl status nginx-1.13.0.service

在开机时启用一个服务：systemctl enable nginx-1.13.0.service

在开机时禁用一个服务：systemctl disable nginx-1.13.0.service

查看服务是否开机启动：systemctl is-enabled nginx-1.13.0.service

查看已启动的服务列表：systemctl list-unit-files|grep enabled

查看启动失败的服务列表：systemctl --failed
```

[article]: https://tsukkomi.org/post/install-amdgpu-on-ubuntu-22-04
[original]: https://github.com/RadeonOpenCompute/ROCm/issues/1713#issuecomment-1193100466
[proxy]: https://phoenixnap.com/kb/ubuntu-proxy-settings
