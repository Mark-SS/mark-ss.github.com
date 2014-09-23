---
layout: post
title: "chnroutes和代码统计"
date: 2014-09-23 12:50:54 +0800
comments: true
categories: 
---
### 使用VPN时候用chnroutes访问国内外  
1. 首先下载 [chnroutes.py](https://github.com/fivesheep/chnroutes) 。
2. 打开终端进入下载文件目录，执行： `python chnroutes.py -p mac`, 该目录下会生成两个文件 [ip-up] 和 [ip-down]。
3. 把这两个文件复制到 /etc/ppp 下，然后进入该目录执行: `sudo chmod a+x ip-up ip-down`
4. 测试一下，是否生效，终端执行: `netstat -nr`, 检查路由表的输出信息。连接VPN， 然后再次执行：netstat -nr， 你会发现路由表已经发生了变化。
5. 到此，访问国内外的网站，同时都是嘻唰唰了。 

	ps: 停用chnroutes, 把 /etc/ppp 目录下的 ip-up 和 ip-down 删除就行了，删除之前，执行一次 ip-down，删除之后保险起见执行 `sudo route -n flush`。
	
		
### 统计代码行数

1. 打开终端。
2. cd到你项目的目录。
3. 输入如下命令：  

	(1) 统计整个工程的所有文件的代码量已经总量  
	`find . "(" -name "*.m" -or -name "*.mm" -or -name "*.cpp" -or -name "*.h" -or -name "*.rss" ")" -print | xargs wc -l`  
	(2) 统计总数  
	`find . -name '*.m' -exec cat {} \; | wc -l`  
	`find . -name '*.h' -exec cat {} \; | wc -l`  
	(3) 统计加排序  
	`find . -name  ‘*.swift’ -print | xargs wc -l | sort`
	
	

