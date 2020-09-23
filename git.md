# <strong>每天离开时提交代码的流程</strong>
```
git checkout dev
git pull origin dev
git checkout mybranch
git merge --no-ff dev
git push origin mybranch
```
# <strong>每天早上来的时候拉取代码的流程</strong>
```
git checkout dev
git pull origin dev
git checkout mybranch
git merge --no-ff dev
```

# 公共文件不要使用代码格式化,提交后必然导致其他人的公共文件代码紊乱

git log   observe relative commit log record;

git branch -f master HEAD~3
change the master branch to indicate to the 3rd ancestor of the HEAD;
=======
git branch -m <oldname> <newname>
git branch -m <newname>
change the branch name

live server is important   