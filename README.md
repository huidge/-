# Internship record(实习记录)   
记录每天实习学习到的新知识和新技能

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
<p>语法:</p><br />

>redis 127.0.0.1:6379> CONFIG GET CONFIG_SETTING_NAME   
>redis 127.0.0.1:6379> CONFIG SET CONFIG_SETTING_NAME NEW_CONFIG_VALUE   
>$redis-cli   
>redis 127.0.0.1:6379> PING   
>$redis-cli -h host -p port -a password

<h3>Redis常用命令</h3>

>redis 127.0.0.1:6379> COMMAND KEY_NAME

<p>Redis 字符串命令</p>

>redis 127.0.0.1:6379> SET runoobkey redis   
>redis 127.0.0.1:6379> GET runoobkey   
>redis 127.0.0.1:6379> DEL runoobkey   

<p>Redis hash 命令</p>

>redis 127.0.0.1:6379>  HMSET runoobkey name "redis tutorial"    description "redis basic commands for caching" likes 20 visitors    23000
>redis 127.0.0.1:6379>  HGETALL runoobkey   

<p>Redis 列表命令</p>

>redis 127.0.0.1:6379>LPUSH runoobkey redis   
>redis 127.0.0.1:6379>LPUSH runoobkey mongodb   
>redis 127.0.0.1:6379> LPUSH runoobkey mysql   
>redis 127.0.0.1:6379> LRANGE runoobkey 0 10   

<p>Redis 集合命令</p>

>redis 127.0.0.1:6379> SADD runoobkey redis   
>redis 127.0.0.1:6379> SADD runoobkey mongodb   
>redis 127.0.0.1:6379> SADD runoobkey mysql   
>redis 127.0.0.1:6379> SMEMBERS runoobkey   

<p>Redis 有序集合命令</p>

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

<br />

<h2>2017-9-30</h2>
<h3>Git安装配置</h3>

<h3>工作流程</h3>

<h3>工作区、暂存区和版本库</h3>

<h3>创建仓库</h3>

<h3>基本操作</h3>

<h3>分支管理</h3>

<h3>github相关</h3>

<h3>Git服务器搭建</h3>

 
