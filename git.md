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

live server is important