# spring-cloud
为了搭建BUPT-Iot 的场景，采用spring cloud的组件，完成快速的开发，用户数据存储在mysql，调取gantch设备的cassandra数据库

# 服务名称
## eurekaserver
注册中心，提供服务注册

## config 
配置中心，为各种服务提供服务配置

## api-gateway
网关，限流和流控等安全机制，对外用户访问入口，暴露在外

## ribbon
负载均衡节点， 提供服务在集群中，选择服务几点地址的方案
