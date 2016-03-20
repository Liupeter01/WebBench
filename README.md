# 项目说明
Webbench是C语言开发的网站压测工具，性能良好, 推荐作为经典项目进行源码阅读。
该项目通过对Webbench项目的源码分析，理解其多进程模拟请求的模型及编码规范与技巧。
主要通过以下方式阅读源码：
* 通读代码，增加部分注释信息
* 绘制程序流程图、函数调用关系图
* 总结多进程模型等程序设计思想的优劣


# WebBench
Webbench是一个在linux下使用的非常简单的网站压测工具。它使用fork()模拟多个客户端同时访问我们设定的URL，测试网站在压力下工作的性能，最多可以模拟3万个并发连接去测试网站的负载能力。Webbench使用C语言编写, 代码实在太简洁，源码加起来不到600行。

使用：
	sudo make clean
	
	sudo make && make install
  
命令行选项：

     -f|--force               不需要等待服务器响应
	   -r|--reload              发送重新加载请求
	   -t|--time <sec>          运行多长时间，单位：秒"
    -p|--proxy <server:port> 使用代理服务器来发送请求
	   -c|--clients <n>         创建多少个客户端，默认1个"
     -9|--http09              使用 HTTP/0.9 
	   -1|--http10              使用 HTTP/1.0 协议
     -2|--http11              使用 HTTP/1.1 协议
	   --get                    使用 GET请求方法
	   --head                   使用 HEAD请求方
	   --options                使用 OPTIONS请求方法
	   --trace                  使用 TRACE请求方法
	   -?|-h|--help             打印帮助信息
	   -V|--version             显示版本号
