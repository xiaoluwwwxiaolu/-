<系统虚拟化-原理与实现>

第1章　开篇

1.1　形形色色的虚拟化

1.2　系统虚拟化

1.3　系统虚拟化简史

1.4　系统虚拟化的好处

第2章　x86架构及操作系统概述

2.1　x86的历史和操作系统概要

2.1.1　x86的历史

2.1.2　操作系统概述

2.2　x86内存架构

2.2.1　地址空间

2.2.2　地址

2.2.3　x86内存管理机制

2.3　x86架构的基本运行环境

2.3.1　三种基本模式

2.3.2　基本寄存器组

2.3.3　权限控制

2.4　中断与异常

2.4.1　中断架构

2.4.2　异常架构

2.4.3　操作系统对中断/异常的处理流程

2.5　进程

2.5.1　上下文

2.5.2　上下文切换

2.6　I/O架构

2.6.1　x86的I/O架构

2.6.2　DMA

2.6.3　PCI设备

2.6.4　PCI　Express

2.7　时钟

2.7.1　x86平台的常用时钟

2.7.2　操作系统的时钟观

第3章　虚拟化概述

3.1　可虚拟化架构与不可虚拟化架构

3.2　处理器虚拟化

3.2.1　指令的模拟

3.2.2　中断和异常的模拟及注入

3.2.3　对称多处理器技术的模拟

3.3　内存虚拟化

3.4　I/O虚拟化

3.4.1　概述

3.4.2　设备发现

3.4.3　访问截获

3.4.4　设备模拟

3.4.5　设备共享

3.5　VMM的功能和组成

3.5.1　虚拟环境的管理

3.5.2　物理资源的管理

3.5.3　其他模块

3.6　VMM的分类

3.6.1　按虚拟平台分类

3.6.2　按VMM实现结构分类

3.7　典型虚拟化产品及其特点

3.7.1　VMware

3.7.2　Microsoft

3.7.3　Xen

3.7.4　KVM

3.8　思考题

第4章　基于软件的完全虚拟化

4.1　概述

4.2　CPU虚拟化

4.2.1　解释执行

4.2.2　扫描与修补

4.2.3　二进制代码翻译

4.3　内存虚拟化

4.3.1　概述

4.3.2　影子页表

4.3.3　内存虚拟化的优化

4.4　I/O虚拟化

4.4.1　设备模型

4.4.2　设备模型的软件接口

4.4.3　接口拦截和模拟

4.4.4　功能实现

4.4.5　案例分析：　IDE的DMA操作

4.5　思考题

第5章　硬件辅助虚拟化

5.1　概述

5.2　CPU虚拟化的硬件支持

5.2.1　概述

5.2.2　VMCS

5.2.3　VMX操作模式

5.2.4　VM?Entry/VM?Exit

5.2.5　VM?Exit

5.3　CPU虚拟化的实现

5.3.1　概述

5.3.2　VCPU的创建

5.3.3　VCPU的运行

5.3.4　VCPU的退出

5.3.5　VCPU的再运行

5.3.6　进阶

5.4　中断虚拟化

5.4.1　概述

5.4.2　虚拟PIC

5.4.3　虚拟I/O　APIC

5.4.4　虚拟Local　APIC

5.4.5　中断采集

5.4.6　中断注入

5.4.7　案例分析

5.5　内存虚拟化

5.5.1　概述

5.5.2　EPT

5.5.3　VPID

5.6　I/O虚拟化的硬件支持

5.6.1　概述

5.6.2　VT?d技术

5.7　I/O虚拟化的实现

5.7.1　概述

5.7.2　设备直接分配

5.7.3　设备I/O地址空间的访问

5.7.4　设备发现

5.7.5　配置DMA重映射数据结构

5.7.6　设备中断虚拟化

5.7.7　案例分析：　网卡的直接分配在Xen里面的实现

5.7.8　进阶

5.8　时间虚拟化

5.8.1　操作系统的时间概念

5.8.2　客户机的时间概念

5.8.3　时钟设备仿真

5.8.4　实现客户机时间概念的一种方法

5.8.5　实现客户机时间概念的另一种方法

5.8.6　如何满足客户机时间不等于实际时间的需求

5.9　思考题

第6章　类虚拟化技术

6.1　概述

6.1.1　类虚拟化的由来

6.1.2　类虚拟化的系统实现

6.1.3　类虚拟化接口的标准化

6.2　类虚拟化体系结构

6.2.1　指令集

6.2.2　外部中断

6.2.3　物理内存空间

6.2.4　虚拟内存空间

6.2.5　内存管理

6.2.6　I/O子系统

6.2.7　时间与时钟服务

6.3　Xen的原理与实现

6.3.1　超调用

6.3.2　虚拟机与Xen的信息共享

6.3.3　内存管理

6.3.4　页表虚拟化

6.3.5　事件通道

6.3.6　授权表

6.3.7　I/O系统

6.3.8　实例分析：　块设备虚拟化

6.4　XenLinux的运行

6.5　思考题

第7章　虚拟环境性能和优化

7.1　性能评测指标

7.2　性能评测工具

7.2.1　重用操作系统的性能评测工具

7.2.2　面向虚拟环境的性能评测工具

7.3　性能分析工具

7.3.1　Xenoprof

7.3.2　Xentrace

7.3.3　Xentop

7.4　性能优化方法

7.4.1　降低客户机退出事件发生频率

7.4.2　降低客户机退出事件处理时间

7.4.3　降低处理器利用率

7.5　性能分析案例

7.5.1　案例分析：　Xenoprof

7.5.2　案例分析：　Xentrace

7.6　可扩展性

7.6.1　宿主机的可扩展性

7.6.2　客户机的可扩展性

7.7　思考题

第8章　虚拟化技术的应用模式

8.1　常用技术介绍

8.1.1　虚拟机的动态迁移

8.1.2　虚拟机快照

8.1.3　虚拟机的克隆

8.1.4　案例分析：　VMware　VMotion　和VMware　快照

8.2　服务器整合

8.2.1　服务器整合技术

8.2.2　案例分析：　VMware　Infrastructure　3

8.3　灾难恢复

8.3.1　灾难恢复与虚拟化技术

8.3.2　案例分析：　VMware　Infrastructure　3

8.4　改善系统可用性

8.4.1　可用性的含义

8.4.2　虚拟化技术如何提高可用性

8.4.3　虚拟化技术带来的新契机

8.4.4　案例分析：　VMware　HA和　LUCOS

8.5　动态负载均衡

8.5.1　动态负载均衡的含义

8.5.2　案例分析：　VMware　DRS

8.6　增强系统可维护性

8.6.1　可维护性的含义

8.6.2　案例分析：　VMware　VirtualCenter

8.7　增强系统安全与可信任性

8.7.1　安全与可信任性的含义

8.7.2　虚拟化技术如何提高系统安全

8.7.3　虚拟化技术如何提高可信任性

8.7.4　案例分析：　sHyper、VMware　Infrastructure　3和CoVirt

8.8　Virtual　Appliance

第9章　前沿虚拟化技术

9.1　基于容器的虚拟化技术

9.1.1　容器技术的基本概念和发展背景

9.1.2　基于容器的虚拟化技术

9.2　系统安全

9.2.1　基于虚拟化技术的恶意软件

9.2.2　虚拟机监控器的安全性

9.3　系统标准化

9.3.1　开放虚拟机格式

9.3.2　虚拟化的可管理性

9.3.3　虚拟机互操作性标准

9.4　电源管理

9.5　智能设备

9.5.1　多队列网卡

9.5.2　SR?IOV

9.5.3　其他

索引

参考文献
