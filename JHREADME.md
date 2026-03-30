# 介绍

启动前需要修改本地 hosts，使用管理员启动修改：notepad C:\Windows\System32\drivers\etc\hosts
将以下内容添加到 hosts 中：
``` text
10.0.10.162 safestore-redis
10.0.10.165 safestore-mysql
10.0.10.166 safestore-nacos
10.0.10.166 safestore-gateway
10.0.10.166 safestore-system
```
``` text
10.0.10.162 jeecg-boot-redis
192.168.2.88 jeecg-boot-rabbitmq
10.0.10.165 jeecg-boot-mysql
127.0.0.1 jeecg-boot-nacos
127.0.0.1 jeecg-boot-gateway
127.0.0.1 jeecg-boot-system
```

## 创建模块

mvn archetype:generate ^
-DgroupId=org.jeecgframework.boot3 ^
-Dmodule=erp^
-Dmodule-up-first=Erp^
-DartifactId=jeecg-module-erp ^
-Dversion=3.9.1^
-DarchetypeGroupId=org.jeecgframework.archetype ^
-DarchetypeArtifactId=jeecg-cloud-archetype ^
-DarchetypeVersion=3.0