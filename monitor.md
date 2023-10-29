---
marp: true
theme: am_blue
size: 16:9
paginate: true
headingDivider: 2
footer: Jennings Liu
_class: lead
---


# 监控

###### 京东云
<!-- _class: cover_b fixedtitleA
<!-- _header: "" -->
<!-- _footer: "" -->
<!-- _paginate: "" -->
##
<!-- _header: 目录<br>CONTENTS<br> -->
<!-- _class: toc_b -->

- [监控设计](#3)
- [监控内容](#4)
- [监控报告](#6)

## 监控设计
<!-- _header: \ ***云运维*** **监控设计** *监控内容* *监控报告* -->
<!-- _class:  navbar bq-green fixedtitleA  -->

  ![设计](./images/monitoring01.png)

## 监控内容
<!-- _header: \ ***云运维*** *监控设计* **监控内容** *监控报告*-->
<!-- _class:  navbar bq-green fixedtitleA  -->
> 主机硬件监控：

- 硬件启用状态
- 硬件健康状态
- 温度

> 操作系统：

- CPU
- 内存
- 硬盘/IO
- 网络
- 进程
- ....

## 监控内容
<!-- _header: \ ***云运维*** *监控设计* **监控内容** *监控报告* -->
<!-- _class:  navbar bq-green fixedtitleA  -->

- 云平台监控：
  - 各个组件状态
  - 使用状态
  - 云上虚拟机
  - Ceph存储系统

> 系统服务监控：

- RocketMQ队列
- Pacemaker集群
- MySQL数据库
- ...

## 监控报告
<!-- _header: \ ***云运维*** *监控设计* *监控内容* **监控报告**-->
<!-- _class:  navbar bq-green fixedtitleA  -->

> 图形展示

- grafana 仪表板

> 月报

- 可以采用固定PPT模版，使用自动化的脚本每月生成报告
