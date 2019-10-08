# wechat-client-go
- 该代码为微信ipad协议的golang客户端实现版本，其中实现了除支付外的大部分常用接口。
- 已实现多个微信号登录，实测可以运行1000+个微信，内存消耗为400M不到，但是会比较吃cpu
- 该项目已通过实际项目运行，压力各方面都还算稳定
- 强调一点，该项目需要grpc服务端的组包解包的接口服务，不然无法正常使用
- 强调一点，该项目需要grpc服务端的组包解包的接口服务，不然无法正常使用
- 强调一点，该项目需要grpc服务端的组包解包的接口服务，不然无法正常使用

### 清粉应用
- clearUser.go为清粉的应用代码，本质上是使用的协议的方法调用实现
- 通过make clear-server命令可以生成二进制运行文件，可以实现跨平台。
- 运行 clear-server，通过http接口访问清粉的二维码，如：http://127.0.0.1:9101/clear/start

### 项目结构
- Makefile 为生成运行程序的脚本文件，通过make linux这种命令可以直接生成指定平台的运行文件，不需要依赖任何环境
- main.go 入口文件，其中有二维码的运行方式和账号密码的运行方式
- runtime/ 运行程序资源文件夹：下载图片语音、登录二维码、运行日志、测试的图片语音
- client/ 微信各个功能模块的实现策略
- client/system/ 主要是系统服务的基础模块：grpc客户端通讯、pack的长连接组包、请求操作、缓存策略等等

### 作者微信
 <img src="https://user-images.githubusercontent.com/15431129/60790819-f0e0b200-a194-11e9-9565-5f6f42dec26c.jpg" width = "150" height = "150" alt="周先生" align=center />
 
### Mac协议交流作者
 <img src="https://wkgjtest.oss-cn-beijing.aliyuncs.com/images/20191008/7c68ad4ddecb3c8b63d37dcad17f2aa3.png" width = "150" height = "150" alt="atdown" align=center />

### 赞助微信
<img src="https://user-images.githubusercontent.com/15431129/60791074-79f7e900-a195-11e9-85ff-f6647482b0a4.jpg" width = "151" height = "217" alt="微信" align=center />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<img src="https://user-images.githubusercontent.com/15431129/60791166-a6136a00-a195-11e9-92c7-f64fa9c28d79.jpg" width = "141" height = "234" alt="支付宝" align=center />


### 赞助列表

| 姓名 | 方式 | 金额 | 日期 |
| --- | --- | --- | --- |
| 李浩🦶 | 微信 | 666.0 | 2019-07-08 15:20:38 |
| \*萌 | 支付宝 | 31 | 2019-07-08 15:48:36 |
| Amb | 微信 | 66.66 | 2019-07-30 11:47:52 |
| Amb | 微信 | 666.66 | 2019-07-30 15:13:52 |
| \*皮 | 微信 | 10.0 | 2019-08-01 10:02:32 |
