# Go基础组件库

### 需求阐述

在后台开发中，有很多共性可寻，比如:

* 都会用db，逃不了sql(mysql,postgres),redis,mongo 这三个
* 都会用日志
* 模块较多的场景会使用服务发现，老牌的zk或者etcd
* 每个服务模块都有自己的配置，json,yaml,toml等
* 对于配置更新频繁的场景，会选择将配置放在配置管理服务里，比如etcd, zk都可以做到这点
* profiling

db，服务发现，配置管理等组件都需要一个client去连接它，开源的client有很多，需要选型，client的使用不难，大部分时候开箱即用不会有大问题，但当并发量上去之后，默认配置多多少少会有些问题，这就需要一个最佳实践。结合这几点，我们可以在开源组件client的基础上再封装一层，让它在不同的场景下都变得易用。这方面本人(songtianyi)在以前开发Golang项目的时候总结了一部分，askuy也在自己的开发过程中总结了一部分，现在可以将这两个项目合并，并加以优化，达到前面说的目标。

### 项目成员

- [songtianyi](https://github.com/songtianyi) 
- [askuy](https://github.com/askuy) 
- [WuKong](https://github.com/qi19901212) 
- [qcrao](https://github.com/qcrao)
- [Jason](https://github.com/XiaoZhangJian)
- [7Ethan](https://github.com/7Ethan)
- [Le](https://github.com/angeletlsf)

### 组内守则

* 需表决的内容，看到后请尽快参与表决，暂时没有时间的可以写明自己的表决时间，给大家一个预期，如果手上没有合适的工具，建议大家下载手机版的应用，比如ios版的codehub。

### 路线图

1. 合并rrframework和invoker并重新命名
2. 组件选型，收集需求，调研网络上已经出现的优化点
3. 提供封装后的接口 
4. 发布第一个版本
5. 投产到本组织的其他项目中(这是一个连续过程，并已定在第一个版本发布以后)
6. 投产到本人或其他人所在公司的Go项目中
7. 公开宣传



