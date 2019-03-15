# spring-cloud
为了搭建BUPT-Iot 的场景，采用spring cloud的组件，完成快速的开发，用户数据存储在mysql，调取gantch设备的cassandra数据库

# 使用的docker
```docker run -d --hostname my-rabbitmq -p 5672:5672 -p 15672:15672 rabbitmq:3.7.9-management```

```docker run -d -p 9411:9411 openzipkin/zipkin```

# 服务名称
## eurekaserver
  - 注册中心，提供服务注册

## config 
- 配置中心，为各种服务提供服务配置

## api-gateway
- 网关，限流和流控等安全机制，对外用户访问入口，暴露在外

## ribbon
- 负载均衡节点， 提供服务在集群中，选择服务几点地址的方案

# 数据库
- Mysql
   - 用户模块，两个角色，租户和用户
- Cassandra(Nosql)
   - 设备模块，对实际设备入网
   
# F&Q
- 由于config用到Rabbitmq，config下本地要docker配置一下 ```docker run -d --hostname my-rabbitmq -p 5672:5672 -p 15672:15672 rabbitmq:3.7.9-management```
- 装docker ce的博客 ```https://www.cnblogs.com/jmaly/p/7722863.html```
- 后台运行 ```nohup java -jar devices_access.jar >devices_access_log.out 2>&1 &```
- 本地scp文件夹copy到远端的home路径下 ```scp -r scp root@114.115.130.42:/home```
- 查看jar有关进程 ```ps -ef|grep jar```

