# watch out
When you install some extentions or set some PATH value. The VS code could not take effect at once.
You can reopen the VS code to solve the problem.

# Toggle between terminal and editor
``` ctrl+alt+t ```
Focus on terminal

``` ctrl+1 ```
Focus on the first editor

``` Ctrl + Shift + 5 ```
New a terminal while focusing the terminal

``` Alt + arrow(←) ```
Toggle the terminal

# Editor shortcuts
- ``` ctrl+shift+` ```
 Oprn the terminal window

- ``` shift + alt + arrow(↓) ```
 copy the current line content to the next line and the cursour focus on the next line.The content is not from the paste.

- ``` alt + i ```
 Give code intelligence(trigger suggest)

- ``` ctrl + G ``` 
 Then write down the number,number and press enter, so you can run to that line,column the default column number is 0

- ``` ctrl + D ```
 Select the variable quickly and it is editable.

- ``` ctrl + [shift] + arrow(←) ```
 Toggle between the word without shift.If press shift you can select many words as you can.
 The command is useful mixed with ctrl+d.

- ``` ctrl|shift +  enter ```
 'ctrl' means adding a new line and the mouse toggled to the new line.

- ``` [shift] + home|end ```
 select from the current position to the head or the end

``` ctrl+shift+e ```
Toggle to the file manager.

``` F1``` Open Help window

```ctrl+alt+-```
go back in ubuntu vscode
```Alt + -```
in windows,get the same effect
`canNavigateBack` reverse is `canNavigateForward`.

# The meaning of .vscode dir
It indicates the configuration of current project.
## pay attention to the name of each conf.
`settins` not `setting`


# about devContainer
The method would be more and more popular

## think about the relation of local env and container.
- 本地环境中有VSCode和项目源代码。开发者会在本地的VSCode中编写代码。之所以将源代码放在本地的文件系统中，因为我们将代码和容器分离，即使我们删除了容器，代码的修改也不会丢失。
- 容器除了包含编译/运行项目代码的环境之外，会挂载(mount)项目源代码，除了挂载源代码，我们很多时候还会挂载数据、编译结果输出文件夹、git credentials等等，VSCode的默认配置会替我们做了。容器中会有VSCode的服务端，服务端将相关信息传递给本地的VSCode，本地VSCode只有一个UI的功能。我们还可以在容器中安装相关的VSCode插件，由于开发环境全部都在容器中，和源代码有关的插件都被安装在容器中。


[link]: https://blog.csdn.net/Jeffxu_lib/article/details/86651173


[The article][link] taught me how to toggle between powershell and editor area!
ctrl + k + s then write down focus terminal
