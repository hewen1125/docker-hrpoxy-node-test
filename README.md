使用 docker-compose 编排一个 node 应用

功能

- 显示一张静态图片
- 使用 redis 保存网站访问计数器
- 显示计数器和主机名

技术要点

- node app 使用 supervisor 管理进程 (nginx, node)
- 使用 docker-compose 的 v2 配置

配置官方 repo 源
   
- http://mirrors.163.com/.help/CentOS7-Base-163.repo

运行方式:
    
根据 docker-compose.yml 文件构建镜像并后台运行

    docker-compose up -d  

拓展 nodeapp 结点个数, haproxy 来进行负载均衡 
    
    docker-compose scale nodeapp=3
