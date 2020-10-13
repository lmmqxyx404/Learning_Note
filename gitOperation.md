# 建立本地仓库与远程空白仓库的联系
cd existing_git_repo
git remote add origin https://gitee.com/si_ma_song/cpractice.git
git push -u origin master

git checkout . #本地所有修改的。没有的提交的，都返回到原来的状态
git stash #把所有没有提交的修改暂存到stash里面。可用git stash pop恢复。
git reset --hard HASH #返回到某个节点，不保留修改。
git reset --soft HASH #返回到某个节点。保留修改

git clean -df #返回到某个节点
git clean 参数
    -n 显示 将要 删除的 文件 和  目录
    -f 删除 文件
    -df 删除 文件 和 目录


git branch --set-upstream-to=origin/master master

配置本地与远程仓库，请参考这篇博客
https://blog.csdn.net/u012145252/article/details/80628451
最终要的是收获这个命令的参数使用
git pull origin master --allow-unrelated-histories

git commit --amend -m "new message"

# .gitignore file
.gitignore file
以斜杠“/”开头表示目录；
以星号“*”通配多个字符；
以问号“?”通配单个字符；
以方括号“[]”包含单个字符的匹配列表；
以叹号“!”表示不忽略(跟踪)匹配到的文件或目录；

git config 记录git的本地配置
git config --list 列出了相应的信息

git log   observe relative commit log record;

git branch -f master HEAD~3
change the master branch to indicate to the 3rd ancestor of the HEAD;
# change the branch name
```git branch -m <oldname> <newname>```
```git branch -m <newname>```
# delete the branch 
```git branch -d <branchName>```
```git push origin --delete <branchName> ```

# clear the git tree cached
``` git rm -r --cached . ```
清除git中所有文件的缓存，进而使得.ignore文件生效
``` git rm --cached filename ```
清除指定文件的缓存

git log   observe relative commit log record;

# git branch -f master HEAD~3
change the master branch to indicate to the 3rd ancestor of the HEAD;

# git tag command
```git tag -a v0.1 -m "comment" [hash5]``` Set the tag for specific git commit and add the relative comment.If the hash5 is void, then the command will add a tag for current commit
---------------------
live server is important


warning: LF will be replaced by CRLF in .gitignore.
solve the above problem to [here][link]

[link]: https://stackoverflow.com/questions/5834014/lf-will-be-replaced-by-crlf-in-git-what-is-that-and-is-it-important