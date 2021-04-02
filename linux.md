# shell 
``` nohup script & ```
keep in mind that the path must be absolute.

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
1. get the user rsa.pub.key
2. try to put the content to the server ``` ~/.ssh/authorized_keys```
## get the linux system information
```cat /etc/xxx-release```
```uname -a```
```lshw``` show the all hardware
```lsmem``` show the memory info

## set the site
Keep in mind that port can only be used by one application.Otherwise it will be conflicted.