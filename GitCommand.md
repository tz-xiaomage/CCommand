## 提交修改：
### 添加所有文件
git add .
### 添加某文件
git add a.txt<file>       
### 已添加git的文件忽略提交
git update-index --assume-unchanged FILENAME       路径+文件名   
### 已添加git的文件忽略后取消忽略提交
git update-index --no-assume-unchanged FILENAME     
### 恢复文件改变前
git checkout -- xbd.md<file>
### 删除某文件
git rm a.txt
### 提交文件
git commit -m "test"
### 追加修改提交文案
git commit --amend -m "test2"
### 删除远端保留本地文件
git rm --cached settings.gradle
### 删除远端文件夹保留本地文件夹
git rm -r --cached gradle
### 放弃此次rebase操作
git rebase --abort
## 状态查询：
### 查询当前状态
git status
### 查询提交日志
git log

## 版本回退：
### 执行git add前执行放弃本地修改，恢复上次提交
git checkout a.txt
### 回退到上一版本
git reset HEAD a.txt
### 回退到某个版本
git reset --hard 39952e15bce582b3
### 删除上个commit记录
git reset --soft HEAD^


## 暂存操作
### 暂存本地变动并revert
git stash "暂存当前变动，revert到上次代码"
### 恢复本地变动
git stash pop stash@{0}


## 分支操作：
### 拉取最新
git pull
### 查看分支
git branch
### 新增分支
git branch dev
### 创建新的空白分支
git checkout --orphan test
### 删除分支
git branch -d dev
### 切换分支
git checkout dev
### 拉取并切换远程分支
git checkout -b dev(本地分支名) origin/dev(远端分支名)
### 合并分支
git merge master
git rebase master
### 查看远程分支
git branch -r
### 推送分支
git push origin dev  
git push origin master:master
### 远程克隆分支
git clone -b dev ssh://git@xxx.xxx.cn/xxx/test.git
### 替换分支
git reset –-hard dev // 将本地当前分支重置成本地dev分支

## Tag操作
### 查看Tag
git tag
### 新增Tag
git tag version0
### 删除Tag
git tag -d version
### 
git tag -a v0.1.2 -m “v0.1.2”
### push某个tag到远端服务器
git push origin v0.1.2
### push所有tag到远端服务器
git push [origin] --tags
### 删除Github上某个tag
git delete 0.1.1
git push origin :0.1.1

### 查看某个文件的包含提交人员，日期、版本号等记录信息，不包括修改详情
git whatchanged <filename>

## Git Commit规范
Angular 的 commit 规范：https://github.com/angular/angular/blob/master/CONTRIBUTING.md#-commit-message-guidelines    
如下：
- build: 改变构建流程，新增依赖库、工具等（例如webpack修改）
- ci: 自动化流程配置修改
- docs: 修改文档
- feat: 新功能
- fix: 修复bug
- perf: 改善性能和体现的修改
- refactor: 代码重构
- style: 仅仅修改了空格、缩进等，不改变代码逻辑
- test: 测试用例的修改

例如：feat(*): add new function.    


         
Arcanist基本使用教程：
https://www.5288z.com/1469.html




