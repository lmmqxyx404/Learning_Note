# shell 


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