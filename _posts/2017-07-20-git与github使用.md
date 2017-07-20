## git的使用
#### git常用命令
| 行为 | 命令 | 备注 |
| :-- | :-- | :-- |
| 初始化 | [init](#init) | 在本地的当前目录里初始化git仓库 |
|  | [clone 地址](#clone) | 从网络上某个地址拷贝仓库(repository)到本地 |
| 查看当前状态 | [status](#status) | 查看当前仓库的状态。碰到问题不知道怎么办的时候，可以通过看它给出的提示来解决问题 |
| 查看不同 | [diff](#diff) | 查看当前状态和最新的commit之间不同的地方 |
|  | diff 版本号1 版本号2 | 查看两个指定的版本之间不同的地方。这里的版本号指的是commit的hash值 |
| 添加文件 | [add -A](#add) | 这算是相当通用的了。在commit之前要先add |
| 撤回stage的东西 | [checkout -- .](#checkout) | 这里用小数点表示撤回所有修改，在`--`的前后都有空格 |
| 提交 | [commit -m "提交信息"](#commit) | 提交信息最好能体现更改了什么 |
| 删除未tracked | [clean -xf](#clean) | 删除当前目录下所有没有track过的文件。不管它是否是.gitignore文件里面指定的文件夹和文件 |
| 查看提交记录 | [log](#log) | 查看当前版本及之前的commit记录 |
|  | [reflog](#reflog) | HEAD的变更记录 |
| 版本回退 | [reset --hard 版本号](#reset) | 回退到指定版本号的版本，该版本之后的修改都被删除。同时也是通过这个命令回到最新版本。需要reflog配合 |
#### 常用步骤
增删改》add》commit》pull