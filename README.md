### 修改内容

1. 修复Linux下部署报“用户凭证过期”问题（ [Issue #5](https://github.com/fangjc1986/wms/issues/5)）
2. 根据数据库情况修改 mysql 包版本
3. 去除原作者的 company.sql 文件，该SQL语句遗漏了`is_del`字段导致程序运行失败

### 部署简述

1. 把sql文件导入MySQL数据库（我服务器上用MariaDB代替MySQL）
2. 修改后端源码中数据库连接配置
3. 使用 maven 编译java后端可执行jar文件
4. 在服务器后台运行 jar
5. 修改前端源码中的后端连接配置
6. 使用 nodejs 的 npm 编译前端代码
7. 将编译好的 dist 文件夹放入服务器相应目录即可（经测试在 Nginx 或 Caddy 下前端均能正常解析）

（以下为原作者 readme）

---

## wms 通用仓储管理系统
### 使用框架核技术
* 后端采用 SpringBoot + MYSQL
* 前端采用 vue.js + ElementUI 
* 实现前后完全分离

### 文件目录：
* back 为后端代码
* app 为前端代码

演示地址：[http://wms.fangjc1986.com](http://wms.fangjc1986.com)
帐号：test
密码：123456