## 星海后台测试平台
星海后台测试平台是涵盖API管理、接口测试、接口监控等功能的轻量级质量保障平台，通过docker一键部署，开箱即用，助力后台研发团队进行高效的接口测试

###产品功能
+ **接口测试**
支持Http/TARS/Dubbo等各通用及私有协议类型，平台可视化编辑接口测试用例，支持复杂的业务场景，支持API接口间的参数传递，实时在线调试以及获取单步执行日志
+ **接口监控**
支持秒级接口监控，整合邮件、钉钉、企业微信等多消息渠道提醒，第一时间接收告警，并获取执行结果与告警日志
+ **API管理**
提供方便快捷可视化的接口管理，支持Swagger，Postman等第三方工具数据导入，可通过接口一键生成用例

###产品特点
+ **用例编写普通模式，实现可视化用例编写**
+ **用例编写高级模式，满足复杂场景用例编写**
+ **支持数据驱动，一键完成批量数据测试+**


### 官方支持

官网：http://xinghai.21kunpeng.com

邮箱：xinghai@21kunpeng.com

QQ交流群：1046943423

dockerhub下载地址：https://hub.docker.com/r/xinghai/xinghai-community

### 星海后台测试平台企业版

申请使用企业版：http://xinghai.21kunpeng.com/applicaton.html


### 快速开始
+ **配置说明**
服务器最低配置建议 2核4G , 建议使用linux服务器部署，如需测试外网接口，请确保宿主机网络畅通

+ **容器启动**
docker run -d -v /data/xinghai:/data/xinghai/env/data --name xinghai-community -p 30000:8322 xinghai/xinghai-community:latest
--name 指定容器名为xinghai-community，可以随意指定。
-p 是指定端口映射(推荐使用)，容器内暴露端口为8322， -p 30000:8322 就是将宿主机的30000端口映射到容器内的8322端口
-v 挂载宿主机的目录到容器内的/data/xinghai/env/data目录(mysql和minio数据存储目录,请勿更改)，用以持久化容器数据，保证容器重启和升级数据不丢失

+ **进入星海平台**
浏览器打开访问地址：http://localhost:30000/service_test/index.html
访问地址：ip为宿主机地址，port为启动容器时-p指定的映射端口
登录，默认账号：admin 密码：admin 首次服务启动较慢，可刷新页面尝试

+ **工作目录**
交互式进入容器，工作目录在/data/xinghai

### 版本更新内容
#### v1.0.1   
 fix部分已知bug  
#### v1.1.0
--**v1.1.0 新增功能**
* postman，swagger接口导入
* TARS协议以及Dubbo协议的接口测试

--**v1.1.0 优化功能**
* 用例步骤支持拖拽
* 取消用例调试
* 用例编辑支持保存并关闭
* 提示框显示页面
* 必填项提示

--**v1.1.0 fix bug**
* 批量创建用例集，公共变量未获取到
* 资源池历史文件操作失败

#### v1.1.1
 fix未挂载页面提示bug 

