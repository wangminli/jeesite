# 开发日志

---
##  将jeesite这个项目迁移到了IDEA这个平台  
这个比想象的要简单，虽然部署文档要求使用eclipse，当初见过同事在idea下运行过这个项目，这增加了我的信心。
很多在《介绍安装》中提到的细节，诸如redis的配置，运行bat程序，我暂时没有理睬他们，也成功启动了项目。

部署过程如下：
- 搭建环境：jdk8、tomcat 8、maven 3 
虽然要求使用jdk7，但8也是可以的
- 建立数据库   
将db/jeesite_mysql.sql这个文件复制到mac中的navicat的New Query(右键)中，然后点击执行即可创建所需的数据库
我在mac下的端口使用的是3307

- 部署和启动tomcat
    - 在部署项目的时候需要注意一下，在Project Structure中选在Web，然后选在本项目的web.xml，点击OK。
    - 在Edit Configrations 中选择Deployment,点击"+"，选择Arifact，然后选择war explored，这样就可以在IDE中看到tomcat的启动项了。
    - 点击启动即可。

-- 2017年10月15日23:32:17