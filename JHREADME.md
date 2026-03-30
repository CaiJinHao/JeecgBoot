# 介绍

启动前需要修改本地 hosts，使用管理员启动修改：notepad C:\Windows\System32\drivers\etc\hosts
将以下内容添加到 hosts 中：
``` text
192.168.2.88 jeecg-boot-redis
192.168.2.88 jeecg-boot-rabbitmq
10.0.10.165 jeecg-boot-mysql
192.168.2.89 jeecg-boot-nacos
192.168.2.89 jeecg-boot-gateway
192.168.2.89 jeecg-boot-system
```

## 修改配置

### 修改密码

批量搜索jeecg-boot-mysql，修改root密码为 ${MYSQL-PWD:密码}
${MYSQL-PWD:root} 替换${MYSQL-PWD:密码}
password: root  替换${MYSQL-PWD:cngrain}
mysql://127.0.0.1:3306 替换 mysql://jeecg-boot-mysql:3306

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