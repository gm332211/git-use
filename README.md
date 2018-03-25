# git 的 使用 #
###  ###
##### 创建一个空文件夹进入目录下初始化
<pre><code>git init</code></pre>
##### 添加提交内容 ###
<pre><code>git add filename</code></pre>
##### 提交commit
<pre><code>git commit -m "this is txt"</code></pre>

##### 查看历史提交
<pre><code>git log</code></pre>

##### 查看最近的历史提交
<pre><code>git log --pretty=oneline</code></pre>

##### 查看历史命令
<pre><code>git reflog</code></pre>

##### 回退上个版本
<pre><code>git reset --hard HEAD^ </code></pre>

##### 回退上上个版本
<pre><code>git reset --hard HEAD^^ </code></pre>

##### 恢复版本
<pre><code>git reset --hard e8ffe</code></pre>

##### 查看文件状态(暂存区)
<pre><code>git status</code></pre>

##### 查看工作区和版本区的不同(根据修改提交)
<pre><code>git diff HEAD -- test.txt</code></pre>

##### 丢弃工作区的修改
<pre><code>git checkout -- text.txt</code></pre>

##### 丢弃暂存区的修改(add后)
<pre><code>
git reset HEAD readme.txt
git checkout -- text.txt</code></pre>
##### 回退版本(commit后)(远程无效)
<pre><code>git reset --hard HEAD^^ </code></pre>

##### 删除git库内容
<pre><code>git rm text.txt</code></pre>

##### 创建ssh key
<pre><code>ssh-keygen -t rsa -C "youremail@example.com"</code></pre>

##### 关联远程github仓库
<pre><code>git remote add origin https://github.com/gm332211/test.git</code></pre>

##### 本地仓库推送到远程仓库(第一次空库提交)
<pre><code>git push -u origin master</code></pre>

##### 以后提交
<pre><code>git push origin master</code></pre>

##### 克隆远程仓库
##### 创建分支并切换
<pre><code>git checkout -b dev</code></pre>
##### 创建分支
<pre><code>git branch dev</code></pre>

##### 切换分支
<pre><code>git checkout dev</code></pre>

##### 查看分支
<pre><code>git branch dev</code></pre>

##### 合并分支内容
<pre><code>git merge dev</code></pre>

##### 删除分支
<pre><code>git branch -d dev</code></pre>

##### 合并出现的问题
##### Git用<<<<<<<，=======，>>>>>>>标记冲突的地方
##### 解决冲突后才能继续合并
##### 不丢弃分支合并
<pre><code>git merge --no-ff -m "merge with no-ff" dev</code></pre>

##### 查看合并分支历史
<pre><code>git log --graph --pretty=oneline --abbrev-commit</code></pre>

##### 保存当前为保存的进度
<pre><code>git stash</code></pre>

##### 查看当前保存进度
<pre><code>git stash list</code></pre>

##### 返回保存进度
<pre><code>git stash pop
git stash apply stash@{0}</code></pre>

##### 强行删除丢弃没有合并的分支
<pre><code>git branch -D feature-vulcan</code></pre>

##### 远程推送分支
<pre><code>
git push origin dev</code></pre>
##### 创建一个标签
<pre><code>git tag v1.0</code></pre>

##### 查看标签
<pre><code>git tag</code></pre>

##### 通过commit_id打标签
<pre><code>git tag v0.9 25b6</code></pre>

##### 查看标签信息
<pre><code>git branch --set-upstream dev origin/dev</code></pre>

##### 打签名标签
<pre><code>git tag -s v0.2 -m "signed version 0.2 released" 25b6</code></pre>

##### 签名采用PGP签名，因此，必须首先安装gpg（GnuPG），如果没有找到gpg，或者没有gpg密钥对，就会报错：
##### 删除标签
<pre><code>git tag -d v0.1</code></pre>

##### 推送标签到远程git库
<pre><code>git push origin v1.0</code></pre>

##### 推送所有标签
<pre><code>git push origin --tags</code></pre>

##### 删除远程标签(预先删除本地标签)
<pre><code>git push origin :refs/tags/v0.9</code></pre>

##### 查看远程关联
<pre><code>git remote -v</code></pre>

##### 删除远程关联
<pre><code>git remote rm origin</code></pre>
