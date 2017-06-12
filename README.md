# redis
# 什么是redis
redis 是用C语言开发的一个高性能键值对（key-value）数据库。它通过提供多种键值数据类型类来适应不同场景下的存储需求，
目前redis支持的键值数据类型如下：
  字符串类型
  散列类型
  列表类型
  集合类型
  有序集合类型
 
 # redis的应用场景
 缓存(数据查、短连接、新闻内容、商品内容)
 （最多使用）-->
 分布式集群架构中的session分离
 聊天室的在线好友列表
 任务队列。（秒杀、抢购、12306等）
 应用排行榜
 网站访问统计
 数据过期处理（可以精确到毫秒）

# redis的安装
  redis是C语言开发，建议在linux上运行，本教程使用Centos6.4作为安装环境。
	安装redis需要先将官网下载的源码进行编译，编译依赖gcc环境，如果没有gcc环境，需要安装gcc：yum install gcc-c++
  
  版本说明
	本教程使用redis3.0版本。3.0版本主要增加了redis集群功能。
	
 源码下载
	从官网下载 
	http://download.redis.io/releases/redis-3.0.0.tar.gz
	将redis-3.0.0.tar.gz拷贝到/usr/local下
解压源码
   tar -zxvf redis-3.0.0.tar.gz  
进入解压后的目录进行编译
	cd /usr/local/redis-3.0.0
	make
安装到指定目录,如 /usr/local/redis
	cd /usr/local/redis-3.0.0 
	make PREFIX=/usr/local/redis install
	
redis.conf
redis.conf是redis的配置文件，redis.conf在redis源码目录。
注意修改port作为redis进程的端口,port默认6379。


拷贝配置文件到安装目录下	
	进入源码目录，里面有一份配置文件 redis.conf，然后将其拷贝到安装路径下 
	cd /usr/local/redis
	mkdir conf
	cp /usr/local/redis-3.0.0/redis.conf  /usr/local/redis/bin

2.4.2.后端模式启动
修改redis.conf配置文件， daemonize yes 以后端模式启动。

执行如下命令启动redis：
cd /usr/local/redis
./bin/redis-server ./redis.conf

redis默认使用6379端口。

也可更改redis.conf文件，修改端口号：

