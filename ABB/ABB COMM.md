# ***ABB通讯配置***

[TOC]

# Industrial Network（工业网络 ）

## 1．DeviceNet

- ##### 系统选项：709-1 DeviceNet Master/slave 

- ##### 硬		件：DSQC1006（DeviceNet 是早期 ABB 机器人标配的选项，在新版本的机器人都改掉了。）

**DeviceNet 主 / 从站特点介绍**
		在一个 DeviceNet 网络中，主站是负责集中管理 I/O 数据的设备，并具备未连接报文管理 UCMM（Unconnected MessageManager）功能。从站节点则是执行特定功能并将自己的 I/O 数据传送给主站的设备，可以无 UCMM 功能，但必须支持预定义主从显式报文连接 。
**（1）DeviceNet 从站特性**
		DeviceNet 从站在网络中拥有唯一的节点地址，并且能独立完成特定的功能，例如 I/O 设备、传感器、数据采集、电机控制等。对实时性要求高的数据通过I/O连接进行传输，因此DeviceNet从站应当支持至少一种I/O连接，且每个 DeviceNet 从站都有一个特定功能的应用对象类，该对象类描述了从站所具有的应用参数和功能 。
**（2）DeviceNet 主站特性**
		DeviceNet 主站在网络中所起的作用有别于 DeviceNet 从站， 它负责网络管理、从站配置以及数据处理，其并不一定具有特定的功能，但也有自己的的对象类和的节点地址。市场上主要有两种形式的主站，一种是可编程控制器（PLC）中的一个单元，它的内部集成了DeviceNet的主站功能；另一种是PC使用的一个集成DeviceNet主站功能的PCI或USB接口卡，通过 PCI / USB 总线与 PC 交换数据 。**DeviceNet 网络组建**
		由于 DeviceNet 是基于 CAN 总线的一种应用层协议，因此其网络组建与 CAN 总线一致，采用主干-分支结构。从站和主站都挂接在该总线上，通常一个 DeviceNet 网络中只有一个主站设备和若干个从站设备同时工作。在进行 DeviceNet 网络布线时，建议选用专用的 DeviceNet 电缆，这样可以提高总线抗干扰能力 。

## 2．EtherNet / IP 

- ##### 系统选项：841-1 EtherNet/IP Scanner/Adapter 

- ##### 硬		件：EtherNet / IP 使用的是主机自带的网口 WAN、Lan2 或是 Lan3，无需增加硬件 。

## 3．ModBus  TCP

​		ModBus  TCP 是简单的、中立厂商的用于管理和控制自动化设备的 ModBus 系列通讯协议的派生产品。显而易见，它覆盖了使用 TCP/IP 协议的 “ Intranet ” 和 “ Internet ” 环境中 ModBus 报文的用途。协议的通用用途是为诸如 PLC'S，I/O 模块，以及连接其它简单域总线或 I/O 模块的网关服务的 。
​		ModBus TCP 协议是作为一种（实际的）自动化标准发行的。既然 ModBus 已经广为人知，该规范只将别处没有收录的少量信息列入其中。然而，本规范力图阐明 ModBus 中哪种功能对于普通自动化设备的互用性有价值，哪些部分是 ModBus 作为可编程的协议交替用于 PLC'S 的“多余部分”。

## 4．PROFIBUS（DP）

- ##### 系统选项：969-1 PROFIBUS Controller 

- ##### 硬		件：DSQC1005 

目前的 PROFIBUS 可分为二种，分别是大多数人使用的 PROFIBUS DP 和用在过程控制的 PROFIBUS PA 。
		**PROFIBUS DP（分布式周边，Decentralized Peripherals）**用在工厂自动化的应用中，可以由中央控制器控制许多的传感器及执行器，也可以利用标准或选用的诊断机能得知各模块的状态 。
		**PROFIBUS PA（过程自动化，Process Automation）**应用在过程自动化系统中，由过程控制系统监控量测设备控制，是本质安全的通信协议，可适用于防爆区域（工业防爆危险区分类中的 Ex-zone 0 及 Ex-zone 1 ）。其物理层（缆线）匹配 IEC61158-2，允许由通信缆线提供电源给现场设备，即使在有故障时也可限制电流量，避免制造可能导致爆炸的情形。因为使用网络供电，一个PROFIBUS PA网络所能连接的设备数量也就受到限制。PROFIBUS PA 的通信速率为 31.25 kbit/s 。
		PROFIBUS PA 使用的通信协议和 PROFIBUS DP 相同，只要有转换设备就可以和 PROFIBUS DP 网络连接，由速率较快的PROFIBUS DP 作为网络主干，将信号传递给控制器。在一些需要同时处理自动化及过程控制的应用中就可以同时使用 PROFIBUS DP 及 PROFIBUS PA 。

## 4．PROFINET 

- ##### 系统选项：888-2 PROFINET Controller/Device

  ##### 				  	  888-3 PROFINET Device

- ##### 硬		件：使用的是主机自带的网口 WAN、Lan2 或是 Lan3，无需增加硬件 。

区别是 888-2 既可以做主站也可以做从站，而 888-3 只能做从站，二者只能选择其一 。

​		PROFINET CBA 的基本概念是很多时候自动化系统都可以分为几个小的子系统，彼此有清楚的区分。PROFINET 元件一般只由少数几个输入信号控制，借由这些元件，用户写的程式启动了元件中的特定机能，将输出信号传递给另一个元件。其中用到的技术是制作商中立的。以元件为基础的通讯只需要进行规划，不需要进行编程。PROFINET CBA 的通讯（非实时通讯）适用于总线周期时间在 50...100微秒的系统 。

# Anybus Adapter（AnyBus 适配器）

Anybus Adapter 有且只能选择一种添加，毕竟主板上只能增加一个适配器 。

## 1．EtherNet/IP

- ##### 系统选项：840-1 EtherNet/IP Anybus 

- ##### 硬		件：DSQC669 

**注：**只能做从站 。

## 2．PROFIBUS（DP）

- ##### 系统选项：840-2 PROFIBUS Anybus Device 

- ##### 硬		件：DSQC667 

**注：**只能做从站 。

## 3．PROFINET

- ##### 系统选项：840-3 PROFINET Anybus Device 

- ##### 硬		件：DSQC688 

**注：**只能做从站 。

## 4．PROFINET 

- ##### 系统选项：840-4 DeviceNet Anybus slave 

- ##### 硬		件：DSQC1004 

# Communication（通讯） 

## 1．FTP 

- ##### 系统选项：614-1 FTP SFTP and NFS client 

用于机器人访问远程挂载的磁盘 。

## 2．PC Interface 

- ##### 系统选项：616-1 PC Interface 

用于电脑与机器人的通讯 。

<img src="https://cdn.jsdelivr.net/gh/lbwds/cloud-img/Cloud img/2022.04.07/004516-09-43-53-45-27184.png" alt="ABB机器人通讯协议（干货）" style="zoom: 80%;" />