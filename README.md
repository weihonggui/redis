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
