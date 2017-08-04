这是一个单机版的fastdfs  
tracker和storage都在一台机器上  
实现了与nginx的集成以便于通过http的方式进行访问

使用方法见最后的已知缺陷

fastdfs在部署的时候需要终端的ip地址，且不能使用127.0.0.1，  
在测试时的ip地址是172.17.0.2，所以配置文件中使用的ip地址就是172.17.0.2  
如果ip地址有变化，则需要修改相应的配置文件，包括：

* client.conf
* storage.conf
* mod_fastdfs.conf

#### 目前已知的缺陷是：

需要根据此镜像创建容器后，在容器内部执行

	'/usr/local/src/start.sh'

才可以启动所需要的服务
