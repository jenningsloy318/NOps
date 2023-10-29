---
marp: true
theme: am_blue
size: 16:9
paginate: true
headingDivider: 2
footer: Jennings Liu
_class: lead
---


# 运维

###### Jennings Liu
<!-- _class: cover_b fixedtitleA
<!-- _header: "" -->
<!-- _footer: "" -->
<!-- _paginate: "" -->

##
<!-- _header: 目录<br>CONTENTS<br> -->
<!-- _class: toc_b -->

- [监控](#2)
- [备份](#6)
- [自动化](#10)

## 监控
<!-- _header: \ ***云运维*** **监控** *备份* *自动化* -->
<!-- _class:  navbar bq-green fixedtitleA  -->

构建一套完整的冲底层服务器的硬件信息，主机操作系统，云系统和运上虚拟机的监控系统，实时了解系统中所发生的各种信息
> 工具选择：

- promethues： 监控服务，获取各个监控对象的各种信息并存储
- altermanager：根据预定义的规则，发送告警信息
- grafana：图形化展示监控图标

## 监控
<!-- _header: \ ***云运维*** **监控** *备份* *自动化*  -->
<!-- _class:  navbar bq-green fixedtitleA  -->
> 监控内容：

- 主机硬件监控： 通过Redfish API 获取主机硬件健康信息
- 主机系统监控：通过监控客户端获取主机操作系统的信息，包括(CPU,内存，磁盘，IO，网络等)
- 云服务监控：通过OpenStack和Ceph监控客户端访问相应的API获取其各种信息
- 云上虚拟机监控：通过集成监控客户端获取虚拟机列表并通过内部安装监控客户端进行操作系统的监控

## 监控
<!-- _header: \ ***云运维*** **监控** *备份* *自动化* -->
<!-- _class:  navbar bq-green fixedtitleA  -->
> 监控报告

- 自动化生成监控图片
- 根据模版自动生成监控报告

## 备份
<!-- _header: \ ***云运维*** *监控* **备份** *自动化*  -->
<!-- _class:  navbar bq-green fixedtitleA  -->
> 备份策略
>
- 每日自动备份
- 多重备份
- 异地保存备份

## 备份
<!-- _header: \ ***云运维*** *监控* **备份** *自动化* -->
<!-- _class:  navbar bq-green fixedtitleA  -->
> 备份工具
>
- rsync/lsync
- Bacula
- storware
- Bareos

## 备份
<!-- _header: \ ***云运维*** *监控* **备份** *自动化* -->
<!-- _class:  navbar bq-green fixedtitleA  -->
> Ceph
>
- Ceph Configuration(/etc/ceph)
- Ceph Monitor State
- Ceph OSD Metadata
- Ceph RBD Images
- Ceph CephFS
- Ceph Database Backups
- Log Files

## 备份
<!-- _header: \ ***云运维*** *监控* **备份** *自动化* -->
<!-- _class:  navbar bq-green fixedtitleA  -->
> OpenStack
>
- OpenStack Configuration(/etc/openstack)
- Network Configuration(/etc/neutron)
- OpenStack Database
- Instance Images(glance backup)
- Volume Backup(cinder backup)
- Network Backup(neutron backup)
- instance(nava backup)
- Log Files

## 自动化
<!-- _header: \ ***云运维*** *监控* *备份* **自动化**  -->
<!-- _class:  navbar bq-green fixedtitleA  -->
- OpenStack IaC(infrastructure as code)
  - ansible
  - terraform
- 镜像定制
- cloud-init集成
