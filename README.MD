# QuartzUtils [![Travis](https://img.shields.io/badge/QuartzUtils-v1.0.0-green.svg)](https://github.com/huangyueranbbc/QuartzUtils/)  [![Travis](https://img.shields.io/badge/API-Quartz-orange.svg)](http://www.quartz-scheduler.org/)      

学习整理quartz一些常用配置和组件。 Quartz工具类。

Job、Trigger、JobDetail、Listener、JobExecutionException、misfire、Priority、Durably、Recovery、DisallowConcurrentExecution、PersistJobDataAfterExecution、ThreadPool、usingJobData、Quartz Plugin、ShutdownHook、JobMxBean。

1.增加QuartzUtils工具类

2.采用优先级的ShutDownHook进行Scheduler和Job的关闭。

3.加入Quartz插件Plugin支持。LogPlugin和ShutdownHookPlugin.

4.新增MxBean坚持Java程序和任务状态。例如内存监控，死锁监控。

5.已打包依赖到github仓库。
    仓库地址:https://github.com/huangyueranbbc/QuartzUtils-1.0.0-RELEASE

    pom增加配置:
    <repositories>
            <repository>
                <id>QuartzUtils</id>
                <name>QuartzUtils</name>
                <url>https://raw.github.com/huangyueranbbc/QuartzUtils-1.0.0-RELEASE/master/</url>
                <releases>
                    <enabled>true</enabled>
                </releases>
                <snapshots>
                    <enabled>true</enabled>
                </snapshots>
            </repository>
    </repositories>

    <dependency>
       <groupId>com.hyr.quartz.utils</groupId>
       <artifactId>QuartzUtils</artifactId>
       <version>1.0-SNAPSHOT</version>
    </dependency>


# Release
# 2020-2-16 V2.0.0
    1、支持延迟定时任务。
    2、简化调用Quartz过程。一行代码搞定。
    QuartzUtils.scheduleWithFixedDelay(scheduler, MyJob.class, 0, 1, TimeUnit.SECONDS, -1, "ProducerJob", "QUARTZ-JOB-GROUP");
    3、新增具有优先级的ShutdownHook进行Quartz组件的顺序安全关闭。
    4、新增MXBean进行任务过程监测。
    5、优化Quartz Plugin插件。提供Job/Trigger日志、ShutDownHook插件。
    6、提供优化的Listener监听器。 可以定制修改。
    7、支持日志级别设置。
    8、提供测试入口。
    9、新增Job持久化策略。  
    10、增加集群模式。 
    11、使用Druid连接池替换默认的c3p0连接池。  
    12、支持导入外部配置。  

更新中......










