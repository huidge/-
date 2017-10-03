# Internship record(实习记录)   
记录每天实习学习到的新知识和新技能
<h2>2017-9-25</h2>

<h2>2017-9-26</h2>

<h2>2017-9-27</h2>

<h2>2017-9-28</h2>

<h2>2017-9-29</h2>
Redis通常被称为数据结构服务器，因为值（value）可以是 字符串(String), 哈希(Map), 列表(list), 集合(sets) 和 有序集合(sorted sets)等类型。

<h3>Redis与其他key-value缓存产品有以下三个特点：</h3>
<ol>
<li>Redis支持数据的持久化，可以将内存中的数据保存在磁盘中，重启的时候可以再次加载进行使用。</li>
<li>Redis不仅仅支持简单的key-value类型的数据，同时还提供list，set，zset，hash等数据结构的存储。</li>
<li>Redis支持数据的备份，即master-slave模式的数据备份。</li>
</ol>

<h3>Redis优势</h3>
<ul>
<li>性能极高</li>
<li>丰富的数据类型</li> 
<li>原子</li>
<li>丰富的特性</li>
</ul>

<h3>Redis安装配置</h3>  
<p>语法:</p>

>redis 127.0.0.1:6379> CONFIG GET CONFIG_SETTING_NAME   
>redis 127.0.0.1:6379> CONFIG SET CONFIG_SETTING_NAME NEW_CONFIG_VALUE   
>$redis-cli   
>redis 127.0.0.1:6379> PING   
>$redis-cli -h host -p port -a password

<h3>Redis常用命令</h3>

>redis 127.0.0.1:6379> COMMAND KEY_NAME

<h3>Redis 字符串命令</h3>

>redis 127.0.0.1:6379> SET runoobkey redis   
>redis 127.0.0.1:6379> GET runoobkey   
>redis 127.0.0.1:6379> DEL runoobkey   

<h3>Redis hash 命令</h3>

>redis 127.0.0.1:6379>  HMSET runoobkey name "redis tutorial"    description "redis basic commands for caching" likes 20 visitors    23000   
>redis 127.0.0.1:6379>  HGETALL runoobkey   

<h3>Redis 列表命令</h3>

>redis 127.0.0.1:6379>LPUSH runoobkey redis   
>redis 127.0.0.1:6379>LPUSH runoobkey mongodb   
>redis 127.0.0.1:6379> LPUSH runoobkey mysql   
>redis 127.0.0.1:6379> LRANGE runoobkey 0 10   

<h3>Redis 集合命令</h3>

>redis 127.0.0.1:6379> SADD runoobkey redis   
>redis 127.0.0.1:6379> SADD runoobkey mongodb   
>redis 127.0.0.1:6379> SADD runoobkey mysql   
>redis 127.0.0.1:6379> SMEMBERS runoobkey   

<h3>Redis 有序集合命令</h3>

>redis 127.0.0.1:6379> ZADD runoobkey 1 redis   
>redis 127.0.0.1:6379> ZADD runoobkey 2 mongodb   
>redis 127.0.0.1:6379> ZADD runoobkey 3 mysql   
>redis 127.0.0.1:6379> ZADD runoobkey 4 mysql   
>redis 127.0.0.1:6379> ZRANGE runoobkey 0 10 WITHSCORES   

<h3>Redis 发布订阅命令</h3>

>redis 127.0.0.1:6379> SUBSCRIBE redisChat   
>redis 127.0.0.1:6379> PUBLISH redisChat "Redis is a great caching technique"   
>redis 127.0.0.1:6379> PUBLISH redisChat "Learn redis by runoob.com"   

<h3>Redis 事务命令</h3>

>redis 127.0.0.1:6379> MULTI   
>redis 127.0.0.1:6379> SET book-name "Mastering C++ in 21 days"   
>redis 127.0.0.1:6379> GET book-name   
>redis 127.0.0.1:6379> SADD tag "C++" "Programming" "Mastering Series"   
>redis 127.0.0.1:6379> SMEMBERS tag   
>redis 127.0.0.1:6379> EXEC   
<h3>Redis 连接命令</h3>

>redis 127.0.0.1:6379> AUTH "password"   
>redis 127.0.0.1:6379> PING   

<h3>Redis 服务器命令</h3>

>redis 127.0.0.1:6379> INFO

<h3>Memcached安装配置</h3>

<h3>比较</h3>
<ul>
<li>Redis有着更为复杂的数据结构并且提供对他们的原子性操作，这是一个不同于其他数据库的进化路径。Redis的数据类型都是基于基本数据结构的同时对程序员透明，无需进行额外的抽象。</li>
<li>Redis运行在内存中但是可以持久化到磁盘，所以在对不同数据集进行高速读写时需要权衡内存，因为数据量不能大于硬件内存。在内存数据库方面的另一个优点是，相比在磁盘上相同的复杂的数据结构，在内存中操作起来非常简单，这样Redis可以做很多内部复杂性很强的事情。同时，在磁盘格式方面他们是紧凑的以追加的方式产生的，因为他们并不需要进行随机访问。</li>
</ul>
<br />

<h2>2017-9-30</h2>
<h3>Git与SVN的区别</h3>
<p>GIT不仅仅是个版本控制系统，它也是个内容管理系统(CMS),工作管理系统等。</p>
<p>如果你是一个具有使用SVN背景的人，你需要做一定的思想转换，来适应GIT提供的一些概念和特征。Git 与 SVN 区别点：</p>
<ol>
<li>GIT是分布式的，SVN不是：这是GIT和其它非分布式的版本控制系统，例如SVN，CVS等，最核心的区别。</li>
<li>GIT把内容按元数据方式存储，而SVN是按文件：所有的资源控制系统都是把文件的元信息隐藏在一个类似.svn,.cvs等的文件夹里。</li>
<li>GIT分支和SVN的分支不同：分支在SVN中一点不特别，就是版本库中的另外的一个目录。</li>
<li>GIT没有一个全局的版本号，而SVN有：目前为止这是跟SVN相比GIT缺少的最大的一个特征。</li>
<li>GIT的内容完整性要优于SVN：GIT的内容存储使用的是SHA-1哈希算法。这能确保代码内容的完整性，确保在遇到磁盘故障和网络问题时降低对版本库的破坏。</li>
</ol>

<h3>Git安装配置</h3>
<p>配置个人的用户名称和电子邮件地址：</p>

>$ git config --global user.name "huidge"  
>$ git config --global user.email huidge@outlook.com  
>//查看配置信息   
>$ git config --list

<h3>工作流程</h3>
<img src="http://www.runoob.com/wp-content/uploads/2015/02/git-process.png"></img>
<h3>工作区、暂存区和版本库</h3>
<ul>
<li><strong>工作区</strong>：就是你在电脑里能看到的目录。</li>
<li><strong>暂存区</strong>：英文叫stage, 或index。一般存放在 ".git目录下" 下的index文件（.git/index）中，所以我们把暂存区有时也叫作索引（index）。</li>
<li><strong>版本库</strong>：工作区有一个隐藏目录.git，这个不算工作区，而是Git的版本库。</li>
</ul>
<h3>创建仓库</h3>
<p>使用当前目录作为Git仓库，我们只需使它初始化。</p>

>git init   
>//指定目录作为Git仓库   
>git init newrepo   
>$ git add .   
>$ git add README   
>$ git commit -m '初始化项目版本'   
>//克隆仓库的命令格式为：   
>git clone (repo) (directory)

<h3>基本操作</h3>

>$ mkdir huidge   
>cd huidge   
> git clone [url]   
>ls -a   
>git add .    
>touch README   
>vim README   
>$ git add README hello.php    
>$ git status -s   
>$ vim README   
>$ git diff   
>git commit -a   
>$ git reset HEAD --hello.php    
>rm 'hello.php'   
>$ git mv README  README.md   

<h3>分支管理</h3>
<P>几乎每一种版本控制系统都以某种形式支持分支。使用分支意味着你可以从开发主线上分离开来，然后在不影响主线的同时继续工作。
有人把 Git 的分支模型称为"必杀技特性"，而正是因为它，将 Git 从版本控制系统家族里区分出来。
创建分支命令：</P>

>//创建分支命令   
>git branch (branchname)   
>//切换分支命令   
>git checkout (branchname)   
>//合并分支   
>git merge   
>//列出分支   
>git branch   
>//删除分支   
>git branch -d (branchname)   

<h3>Git查看提交历史</h3>

>$git log   
>$git log --online   
>$git log --online --graph   
>$ git log --reverse --oneline   

<h3>github相关</h3>

>//添加一个新的远程仓库   
>git remote add [shortname] [url]   
>//生成SSH Key   
>$ ssh-keygen -t rsa -C "huidge@outlook.com"   
>//验证是否成功   
>$ ssh -T git@github.com   
>git remote   
>git remote -v   
>git fetch   
>git merge   
>git push [alias] [branch]   
>git remote rm [别名]   

<h3>Git服务器搭建</h3>

<h2>2017-10-2</h2>
<h3>Web性能优化</h3>
<ol>
<li>减少请求次数（最大化利用有限的请求数）</li>
<p>浏览器针对资源的域名，限制并发连接数，静态资源放在单独域名下，减少携带不必要的cookie数据。合并同一域名下的资源，css合并，js合并，图片组合为css贴图（sprite image）,内嵌小型css,javascript，设置缓存，减少重定向等，省掉不必要的HTTP请求。</p>
<li>压缩资源体积</li>
<p>图片格式选择：对于比较大的文本资源，必须开启gzip压缩。</p>
<li>提高服务器的请求处理能力</li>
<ul>
<p多处理模块（MPM)</p>
<li>prefork模式:进程维持1个连接，内存高，稳定</li>
<li>worker模式:进程维持1个连接，内存低，不稳定</li>
<li>Apache:占用更少资源和内存，阻塞，高性能</li>
<li>Nginx:占用更少资源和内存，异步非阻塞，高性能</li>
</ul>
</ol>
<h3>缓存</h3>
<p>
<ul>
	<li>存储频繁访问的数据</li>
	<li>内存缓存减少磁盘I/O</li>
	<li>保存耗时的操作，以便下次使用</li>
</ul>
</p>
<li>服务器缓存（适用服务器性能为主要瓶颈的场合）</li>
<ol>
	<li>数据库查询缓存</li>
	<li>扩展数据库缓存memcached</li>
	<li>文件缓存</li>
	<li>静态化</li>
</ol>
<li>浏览器缓存（适用网络连接为主要瓶颈的场合）</li>
<ol>
	<li>主要作用</li>
	<p>对用户来说，减少请求可以更快地加载页面，节省流量；对网站来说，减少带宽压力和费用。</p>
	<li>服务器通过对每个资源的HTTP响应头设置属性和值，来发出自己的缓存指令。</li>
	<li>Expires 对静态资源设置Expires,用户需要这个资源时，浏览器直接从缓存中读取，不需要询问服务器端的意见，这种缓存是最快的。</li>
	<li>Last-Modified 对于一个有可能过期的资源，设置上次修改时间，如果用户要用就请求是否有更新，没有更新（回复304）直接使用，更新过重新获取（200）。</li>
	<li>Restful Web API</li>
	<p>是一种组织Web服务的架构，其目标是为了创建具有良好扩展性的分布式系统。
作为一种架构，其提出了一系列架构级约束。这些约束有：</p>
	<ol>
		<li>使用客户/服务器模型。客户和服务器之间通过一个统一的接口来互相通讯。</li>
		<li>层次化的系统。在一个REST系统中，客户端并不会固定地与一个服务器打交道。</li>
		<li>无状态。在一个REST系统中，服务端并不会保存有关客户的任何状态。也就是说，客户端自身负责用户状态的维持，并在每次发送请求时都需要提供足够的信息。</li>
		<li>可缓存。REST系统需要能够恰当地缓存请求，以尽量减少服务端和客户端之间的信息传输，以提高性能。</li>
		<li>统一的接口。一个REST系统需要使用一个统一的接口来完成子系统之间以及服务与用户之间的交互。这使得REST系统中的各个	子系统可以独自完成演化。</li>
	</ol>
<p>如果一个系统满足了上面所列出的五条约束，那么该系统就被称为是RESTful的。</p>
	<li>HTTP1.1加入的Cache-Control</li>
	<p>浏览器缓存设置最佳实践</p>
	<ol>
		<li>对于动态生成的HTML页面使用HTTPS头：Cache-Control:nocache</li>
		<li>对于静态HTML页面使用HTTPS头：Lats-Modified</li>
		<li>其它所有的文件类型都设置Expires头，并且在文件内容有所修改的时候修改Query String</li>
	</ol>
</ol>

<h2>2017-10-3</h2>
<h3>ES6语法</h3>
<h4>一、新的变量声明方式let、const</h4>
<p>与var不同，最重要的两个特性就是提供了块级作用域与不再具备变量提升。使用ES6，需要全面使用let/const替换var,let声明一个变量，const声明一个常量。</p>
<h4>二、箭头函数的使用</h4>
<p>箭头函数可以替换函数表达式，但是不能替换函数声明。（箭头函数中没有this!）</p>
<h4>三、模板字符串</h4>
<p>模板字符串是为了解决使用+号拼接字符串的不便利而出现的，使‘’将整个字符串包裹起来，而在其中使用${}来包裹一个变量或表达式。</p>
<h4>四、解析结构</h4>
<p>数组以序列号一一对应，有序的对应关系；对象根据属性名一一对应，无序的对应关系。</p>
<h4>五、默认的参数（函数）</h4>
<p></p>
<h4>六、展开运算符</h4>
<p>在ES6中用...来表示展开运算符，它可以将数组方法或对象进行展开。</p>
<h4>七、对象字面量与class</h4>
<p></p>
<h4>八、Promise</h4>
<p></p>
<h4>九、模块Modules</h4>
<p></p>


