# git食用说明

`git init`:仓库初始化.

`git remote add origin git@github.com:yourName/yourRepo.git`:添加远程地址.

后面的yourName和yourRepo表示你再github的用户名和刚才新建的仓库，加完之后进入.git，打开config，这里会多出一个remote "origin"内容，这就是刚才添加的远程地址，也可以直接修改config来配置远程地址。

`git add .`

这是 git 基本工作流程的第一步；使用如下命令以实际提交改动：

`git commit -m "代码提交信息"`

并切换<branch>过去：

`git checkout -b <branch>`

切换回主分支：

`git checkout master`

再把新建的分支删掉：

`git branch -d <branch>`

除非你将分支推送到远端仓库，不然该分支就是 不为他人所见的：

`git push origin <branch>`


强推，即利用强覆盖方式用你本地的代码替代git仓库内的内容:

`git push -force`

先把git的东西fetch到你本地然后merge后再push

`git fetch`
`git merge`

这2句命令等价于

`git pull`

有时候remote有多个版本分支库，git pull需要指定开发版本的分支：

`git pull origin master`

要提高 Git 的下载速度，你可以考虑以下几个方法：
使用更快速的网络连接：确保你的网络连接速度良好。如果你使用的是无线网络，尽量保持稳定的信号强度和质量。
选择合适的远程仓库：有时候远程仓库的服务器可能位于离你较远的地方，选择一个距离较近的镜像仓库或者更快的远程仓库可以提高下载速度。
使用 SSH 协议：如果你使用 HTTPS 协议进行克隆或拉取操作，尝试使用 SSH 协议替代。SSH 协议通常比 HTTPS 协议更快。
使用加速代理或 CDN：一些地区可能有专门的 Git 加速代理或使用 CDN（内容分发网络）的服务，通过使用这些服务，可以加速从远程仓库下载的速度。
配置 Git 的压缩选项：Git 提供了一些压缩选项，可以在传输数据时减少文件大小，从而提高下载速度。你可以尝试设置以下选项：

`git config --global core.compression 9`

这会使用最大程度的压缩，但会增加 CPU 开销
使用 Git 的浅层克隆（shallow clone）：如果你只需要仓库的最新历史记录，可以考虑进行浅层克隆。这样只会下载最近的提交，而不是整个仓库的完整历史记录。

`git clone --depth 1 <repository_url>`

这将只克隆最近的一个提交。
请注意，下载速度还受到其他因素的影响，例如远程仓库的服务器性能、带宽限制等。在某些情况下，下载速度可能无法完全控制。