## 一 Markdown 
轻量级标记语言

可以通过某种方式转换为别的文本格式 
## 二 集中式版本控制 SVN
 - （1）使用总结： 版本控制管理系统  
源代码仓库 reposiitory  
检出代码 checkout   
更新最新代码 update  
提交修改 commit  
 - （2）使用建议：   解决了bug或者有成熟模块的时候再去提交 
每次commit之前都要update   检查有没有最新版本避免冲突  
每次commit的时候务必写上提交日志  
 - （3）TortoiseSVN 客户端基本操作流程 
   + 检出项目：checkout  
   + 在没有源代码的前提下，需要通过   tortoise-svn 客户端下载

   + 增加文件或目录：add（增加），删除、修改 源代码
    只是在你的本地做这样的操作
   + 提交修改：commit
    帮你记录当前开发的软件的状态
   + 更新文件或目录：update（更新）
    别的开发人员在已有源代码的前提下可以通过 update 更新服务器上最新的版本
   + 查看版本日志：log（日志）
## 三 GUI  VS  CLI
   图形用户界面（GUI）


   命令行界面（CLI）
## 四 Command Line(shell bash)
  Shell就是一个程序 它接受从键盘输入的命令，然后把命令传递到操作系统去执行
 几乎所有的Linux发行版都提供一个名为‘bash’的shell程序
## 五 终端仿真器
    当使用图形用户界面时，我们需要另一个和 shell 交互的叫做终端仿真器的程序。
在 Windows 上，一般使用操作系统自带的 `cmd` 或者 `powershell`。
在 Linux 上，如果是图形用户界面，那么可以使用 `terminal` 或者 `konsole`、`gnome-terminal` 之类
的终端仿真器，但基本上，它们都完成同样的事情，让我们能访问 shell，

## 六 使用终端操作文件系统
   - Pwd (prit working directory); 当前目录的根目录
   - Ls (list files) 列出当前目录文件 Ls -a 列出文件并显示隐藏文件目录
   - Cd(change directory) 切换到指定路径文件 
      + 在cmd或者powershhel中切盘符 ：盘符：回车即可
   - Cp (copy) cp 源路径  -r 递归复制 
   - Mv (move) 移动文件  可以重名文件
   -  Mkdir 创建目录
   - Rm 删除文件或者目录  -rf 直接删除整个目录包括里面的内容都删除 但是在cmd   powershell不支持
   - Clear 清屏  cmd使用的是cls
   - Touch  文件名根据文件名创建新的文件
   - Cat 文件名查看指定的文本文件
## 七 使用less命令浏览文件内容 
   - 插入模式 通过从命令模式按I进入编辑模式
   - 保存：从编辑模式退出到命令模式   ：w保存该文件
   - ：q  退出 如果没有保存会提示让你保存再退出
   - :q!  强制退出  ：wq 保存并退出 
## 八 PATH 环境变量
   目的就是为了可以在终端中的任意目录中使用该可执行文件
## 九 GIT 分布式版本控制系统
    （1）学习资源 
       http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000
    git - 简明指南
    猴子都能懂的Git入门
    菜鸟教程：Git 教程
    (2)流程
- 在本地当前项目初始化一个空的git仓库
    -  $ git init 
-  查看当前版本管理状态：未被版本管理的 已经修改的 删除的
    -  $ git status
- 将指定的文件添加到暂存区
     - $ git add 
     - $ git add  .
    - $ git add  --all
    - $ git add file file [file]
-  提交
      - $ git commit -m “提交注释 ”
-  查看提交日志
    - $ git log
-  对比文件变动差异
      +  $ git diff

 (3) 撤销
 - 恢复暂存区的指定文件到工作区
  + $ git checkout [file]
 - 恢复某个commit的指定文件到暂存区和工作区
  - $ git checkout [commit] [file]
- 恢复暂存区的所有文件到工作区
  - $ git checkout .
- 重置暂存区的指定文件，与上一次commit保持一致，但工作区不变
  - $ git reset [file]
-  重置暂存区与工作推送和获取远程仓库

   + $ git remote add
   + $ git push
   + $ git clone
   + $ git pull区，与上一次推送和获取远程仓库
   + $ git remote add
   + $ git push
   + $ git clone
    + $ git pullcommit保持一致
   + $ git reset --hard
+ 重置当前分支的指针为指定commit，同时重置暂存区，但工作区不变
  + $ git reset [commit]
-  重置当前分支的HEAD为指定commit，同时重置暂存区和工作区，与指定commit一致
   + $ git reset --hard [commit]
- 重置当前HEAD为指定commit，但保持暂存区和工作区不变
  + $ git reset --keep [commit]
-  新建一个commit，用来撤销指定commit
-  后者的所有变化都将被前者抵消，并且应用到当前分支
   + $ git revert [commit]
-  暂时将未提交的变化移除，稍后再移入
   + $ git stash
   + $ git stash pop
## 十 分支
   - 列出所有本地分支
      - $ git branch 
   - 列出所有远程分支
      - $ git branch -r
   - 列出所有本地分支和远程分支
      - $ git branch -a
   - 新建一个分支 但依然停留在当前分支
      - $ git branch [branch-name]
   - 新建一个分支 指向指定commit 
     - $ git branch [branch] [commit]
   - 切换到上一个分支
      - $ git checkout -
  -  合并指定分支到当前分支
   - $ git merge [branch]
   -  删除分支
   - $ git branch -d [branch-name]

+ 创建分支：`git branch <name>`
  + 基于某个分支创建分支
  + 先切换到基于的分支
  + 再创建分支
- 切换分支：`git checkout <name>`
- 交替切换分支：`git checkout -`
- 创建+切换分支：`git checkout -b <name>`
- 基于某个分支创建新的分支并切换到该分支：`git checkout -b <name> <name>`
- 合并某分支到当前分支：`git merge <name>`
- 合并某分支到当前分支并提交记录：`git merge --no-ff <name> -m "提交日志"`
- 删除分支：`git branch -d <name>`
- 以图表形式查看日志 `git log --graph`
## 十一 推送和获取远程仓库
  - $ git remote add
   - $ git push
   - $ git clone
   - $ git pull

## 十二 分支管理策略
   - （1）master   git主分支的名字 代码库仅且只有一个
   - （2）develop 日常开发应该在另一条分支上完成
   - （3）feature-特姓名 特性功能的分支
   - （4）release 预发布分支
   -（5）fixbug 修改bug分支
## 十三 获取和推送远程仓库
     第三方托管服务：github 码云 开源中国  coding   bitbucket
推送：
   如果已经有了一个本地仓库，可以通过下面的方式和线上的空仓库产生关联


 （1）cd 切换到当前的文件夹


 （2）初始化一个空目录 git init


  (3) 在本地添加新的文件 查看版本 git status


  (4) 添加到缓存区 git  add 


  (5) 提交到本地仓库 git commit -m “提交日志”

  (6) 将本地的仓库添加到线上仓库


     A 建立线上空仓库
     B 复制线上仓库地址
     C 使用git remote add  仓库名字（origin）仓库地址
         `git remote add origin 远程仓库地址``
         git 会自动将远程仓库地址起个别名 origin   
     D 将本地仓库的文件push到线上仓库
       Git push 仓库名字 master
       Git remote show (查看线上仓库的名字)
补充：git push -u origin master`或者 git push --set-upstream origin master 建立桑下文关联
  推送到名称为 origin 远程仓库地址下的 master 分支下
  -u 就是产生上下游关系，以后 push 会走你 -u 指定的


获取 ：如果已经创建了一个线上远程仓库 本地没有


   （1）git clone 仓库地址


 - Git 会自动将 origin设置为该远程的仓库地址的标示符


     （2）git pull 在进行push之前，最好pull 一下 拉取最新源代码

     （3）git add . 添加至缓存区

     （4）git commit -m “” 提交到本地仓库

      (5) git push 本地仓库提交到线上仓库、
## 十四 github介绍
（1）Github（https://github.com/）是为了开发者提供git仓库的托管

（2）Github与git区别
     Git是一个分布式版本控制系统的

        历史记录的问题  多人协作的问题

（3）Request + pull 功能
     通过pull request 修改了一个开源仓库的源代码 强求合并 
# Github 使用总结
## 仓库
### 假设本地有一个通过 `git init` 创建出来的仓库
需求：将这个本地仓库放到线上远程仓库。
1. 在第三方托管服务那里新建一个空仓库
2. 拿到空仓库的地址
   3. 使用 `git remote add abc https://github.com/itcast-aaa/hello.git`
4. 使用 `git push abc master`
5. 通过上面的操作之后，以后每次去 `push` 的时候都必须显示的写上 `git push 远端仓库地址别名 分支名称`
。。。。。。。。
如果不想每次  `push` 的时候都写那么长（没有多个远程仓库，也不需要频繁的去push不同的分支），
假设每次都是 `push` 到 abc master，那么可以通过 `git push --set-upstream abc master` 去推送一次。
那么在以后的 push 中，只要仓库地址没变、分支不变，就可以直接 `git push`。

### 本地没有，线上有
需求：想要获取远程仓库到本地
1. 使用 `git clone 远程仓库地址`
只要执行了上面的操作之后，git 会自动帮你通过网络去下载对应的远程仓库，
下载下来之后自动添加一个 remote，地址是你 clone 的那个地址，名字叫 origin。
之后只要你想要 push ，直接 git push 就可以了。原因是它已经自动帮你建立了上下游关系。


## 十五 NPM
（1）Npm是一个基于NOde开发的一个命令行工具，专门用来安装和管理javascript模块或者包的 
例如 jquery bootstrap等前端包以及node相关包

（2）安装和更新npm
   打开终端 输入‘npm -v’如果能看到输出一个版本号，说明有npm 安装了node 就安装了Npm 
更新  $ npm install -g npm

(3)基本使用

        npm  init 使用npm init 命令初始化一个package.json文件

        npm  install [--save] 包名 npm会自动去联网npmjs.com网站下载对应的包下载下来之后将这个包放到当前目录下的 `node_modules` 目录。
同时 `--save` 参数，会自动将下载的项以依赖名称的形式添加到 `package.json` 文件中的 `dependencies` 字段中。

        npm install

`npm install` 会自动找当前目录下的 `package.json` 文件，如果找不到，直接报错。
如果找到，找 `dependencies` 字段，然后拿到里面的依赖项，依次下载到当前目录下的 `node_moudles` 目录中。

## 十六 bower 和npm差不多的步骤
## 十七 angular
  + 当浏览器在解析DOm结构文档的时候：
     -  遇到自己不认识自己的属性或者字符串，浏览器会选择忽略或者直接渲染
     -  当浏览器解析到 script 标签的时候，会自动去发起请求下载该资源
     - 当下载 angular.js 文件资源成功的时候，ng 开始执行
     - ng 开始执行就会自动去 DOM 文档结构中找到 ng-app 属性，然后开始解析这个节点中被包裹的所有自己能识别的元素
     - 1. ng-app 在 AngularJS 中被称作是指令，用来作为 ng 启动和管理应用程序的一个入口标识
           -  同时还起到一个边界的作用，作用了 ng-app 节点内部的元素都可以直接使用 ng 提供的一系列的

+ 指令、表达式等相关功能。
    - 2. 当 ng 找到 ng-app 属性的时候，启动一个应用程序，ng 应用程序开始运行
       -  ng 自动在自己的应用程序内部创建一个数据容器（可以想象成一个对象）

       -  $scope 就是那个圆柱体对象

      - 需求：根据视图抽象数据模型成员

     - 1. 在全局定义一个函数，必须是全局

     - 2. 函数接收一个参数：$scope 必须的

     - 3. 在 html 中通过 ng-controller 让你的 HTML 视图和 f() 函数建立一个关系

     -     ng 解析执行到 ng-controller 的时候会自动去全局找对应的 f 函数，然后执行

     - 4. 这样的话被作用了 ng-controller 属性的元素中所有的子节点都可以直接访问函数 f 中的 $scope 数据成员

    -  总结：
    -    1. 写 ng 代码肯定是把代码都写到 js 中

    -   2. 通过一个函数让你的视图和数据模型之间产生一个关联

    -   3. 该函数具有特殊意义，是 ng 根据 ng-controller 指令自动去调用的
    
    -   4. 该函数必须定义在全局，而且为了有别于普通函数，所以在起名字的时候，用一个大写业务名称加上一个 Controller 作为一个语义性
    -    这个函数的学名叫控制器：用来控制视图和数据模型的交互
    -        控制器主要职责：
    -         1. 根据视图初始化数据模型成员
    -            普通成员
    -             行为函数
## 十八控制器的作用：
     -  将视图模型对象（根据视图抽象出来的数据）和视图连接起来进行交互，主要就是起到了一个桥梁的作用
     - $scope 的作用：
     -   第一它是数据模型对象
    - 这里为什么叫 scope
     -   这里实际上应该叫做：视图模型（根据视图抽象数据模型）
    -  主要职责就是和视图交互
     -       页面中某个元素的值变了，模型中的成员也跟着变
     -      模型中的成员变了，页面中使用或者绑定了该成员的地方都会跟着变（视图模型帮你自动同步过去呀）
     - $scope 还起到另一个作用：作用域
     - 在1.3版本之前，可以在全局定义一个全局函数充当控制器的作用，然后通过`ng-controller`指令将控制器（即视图模型）和视图绑定在一起，这样视图就可以访问该控制器nebulizer的所有元素
     - 在1.3版本之后，控制器函数已经不能定义到全局了，否则直接报错
     - 根据不同的业务划分不同的控制器

## 十九 模块
    - 在 1.3 之后，不能全局定义控制器了，必须先定义一个模块再再模块下定义控制器。
    - 模块主要的职责并不是为了解决命名冲突的：

    - 模块主要用来将相同业务的控制器组织到一起。
## 二十 Angular 的调试方式
- 通过Chrome应用商店下载AngularJs Batarage
- 以http服务器的形式打开你要调试的页面应用程序
- 打开控制台，找到AngularJS选项卡
- 选择Enable启用调试
- 切换到scopes选项，查看各个控制器作用域中的模型数据
- 对于事件行为的代码调试，和以前一样，直接找到对应的代码打断点调试即可
##  二十一 npm 被墙问题

   - 每次安装包的时候加上该参数：`--registry=https://registry.npm.taobao.org`，
   - 例如我要下载 `bower`, 命令如下：

   ```bash
   $ npm install -g bower --registry=https://registry.npm.taobao.org
   ```

   - 如果每次这样太麻烦，可以修改 `.npmrc` 文件配置 npm 下载所使用的下载地址：

   ```bash
   $ npm config set registry=https://registry.npm.taobao.org
   ```

   - 只要执行了上面的操作之后，以后使用 npm 下载任何包都会走上面配置的请求路径。
## 二十二 查看离线文档

   - 第一：安装一个工具：`http-server`，这是一个基于 Node 开发的一个命令台工具，
   - 通过 `npm install -g http-server` 安装。
   - 通过`http-server --version`去查看端口号
## 二十三 Browser-Sync

        https://www.browsersync.io/

        安装：`npm install -g browser-sync`

        启动：`browser-sync start --server --files "css/*.css, js/*.js, *.html"`

          该命令表示启动一个服务器同时监视指定文件的变化，当文件发生变化，自动同步浏览器刷新。
## 二十五 # JSON

 - 序列化（将一个对象转为字符串就叫 JSON 序列化）

 JSON.stringify

 ```json
 {
   foo: 'bar'
 }
 ```

 - 反序列化（将标准的 JSON 格式的字符串转为对象）

 JSON.parse

 ```json
 {
   "foo": "bar"
 }
 ```

## 二十六   本地存储

 - 持久存储（只要你不删，永久存在你的本地）
   + window.localStorage
     * setItem(String, String)
     * getItem(String)
     * removeItem(String)
     * 存储普通的字符串可以直接存储
     * 如果要存储一个对象，则必须将对象序列化成字符串才可以
     * 该存储只针对于当前
 - 会话存储（只要浏览器关了，数据就没了）


   



