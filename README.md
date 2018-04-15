# Docker Compose编排工具简介

Compose是一个用于定义和运行多容器Docker应用程序的工具，前身是Fig，它非常适合用在开发、测试、构建CI（持续集成）工作流等场景中。

Docker Compose是一个用来定义和运行复杂应用的Docker工具。一个使用Docker容器的应用，通常由多个容器组成。使用Docker Compose不再需要使用shell脚本来启动容器。 

Compose 通过一个配置文件来管理多个Docker容器，在配置文件中，所有的容器通过services来定义，然后使用docker-compose脚本来启动，停止和重启应用，和应用中的服务以及所有依赖服务的容器，非常适合组合使用多个容器进行开发的场景。

![](http://www.ruanyifeng.com/blogimg/asset/2018/bg2018021311.jpg)

[Compose](https://docs.docker.com/compose/) 是 Docker 公司推出的一个工具软件，可以管理多个 Docker 容器组成一个应用。你需要定义一个 [YAML](http://www.ruanyifeng.com/blog/2016/07/yaml.html) 格式的配置文件`docker-compose.yml`，写好多个容器之间的调用关系。然后，只要一个命令，就能同时启动/关闭这些容器。

```
# 启动所有服务
$ docker-compose up
# 关闭所有服务
$ docker-compose stop
```

# 学习目标

在[**Micro-service-learning**](https://github.com/TaciturnK/Micro-service-learning) 工程的学习基础之上，使用docker工具进行服务的发布，主要利用其中的6个子工程来进行学习，工程列表如下：

- microservice-consume-movie-feign-hystrix：服务消费者(整合ribbon.feign,hystrix)
- microservice-discovery-eureka：服务注册中心(Eureak)
- microservice-getway-zuul：路由网关(Zuul)
- microservice-hystrix-dashboard：hystrix可视化监控工具(独立项目，不依赖服务注册中心)
- microservice-hystrix-turbine：turbine聚合监控数据(供microservice-hystrix-dashboard调用)
- microservice-provider-user：服务提供者

**环境：**

- 虚拟机上已经搭建了docker服务，并可以进行正常的镜像拉取，上传阿里云镜像仓库操作，相关功能已经经过测试，达到了实验的条件。
- idea开发工具上面已经安装了docker开发插件，并且虚拟机的docker开启了api2375端口，远程传输的功能，并且已经单独进行了测试，达到了在idea上发布镜像到虚拟中的条件。

**学习目的：**

> 在Idea工具上编排微服务的各个服务，并使用docker插件发布到虚拟机中的docker服务中，然后进入虚拟机，在虚拟机中将镜像发布到远程阿里云docker镜像仓库，供其他主机使用时拉取。

**学习计划：**

1. docker compose快速入门：使用microservice-discovery-eureka作为学习目标，使用compose工具进行编排发布，并可进行访问；
2. 编排这6个微服务，并最终可进行访问；



# Docker Compose 的安装



# 安装Compose命令补全工具



# Docker Compose基本使用

