# AI-Fere
作用于B端的提供伴侣回复的AI架构，当前调用为GPT的接口实现。


# 项目结构
/myapp
├── /cmd              # 启动程序
│   └── /server.go    # 启动文件
├── /config           # 配置文件
├── /internal         # 内部业务代码
│   ├── /handler      # 路由处理层
│   ├── /service      # 业务逻辑层
│   ├── /repository   # 数据库访问层
│   ├── /model        # 数据模型层
│   └── /middleware   # 中间件
├── /pkg              # 公共库
├── /scripts          # 脚本（如数据库迁移）
├── /deploy           # 部署相关文件
└── go.mod            # Go Module 配置

1. 安装go及其相关依赖依赖
   1. go安装网上有
   2. go依赖
      go get 
      依赖：
2. 关键设计原则
   1. 使用 Goroutines 和 Channels
   2. 连接池（Connection Pool）
   3. 负载均衡
   4. 限流
   5. 异步处理
3. 架构设计
   1. Web 框架：Gin
   2. 消息队列：Kafka
   3. 数据库：MySQL配合连接池管理
   4. 缓存：Redis
   5. 负载均衡器：Traefik
   6. 服务发现和调度：Zookeeper
   7. 服务容器化：docker
4. 业务设计
   1. 当前仅仅使用gpt api 实现封装。
   2. prompt实验设置效果
   3. prompt模板设计
   4. 用户输入特征归纳提取。（后续项目）
   5. prompt标签加入(后续项目)