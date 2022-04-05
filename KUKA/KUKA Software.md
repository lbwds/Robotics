# KUKA备选软件包

对于不同行业的应用，为了方便编程操作及提高效率，KUKA机器人提供了不同的软件选项。

---

# 专用功能 - 工艺自动化

## 一．弧焊功能包

### 1．ArcTech Basic

KUKA.ArcTech Basic 是一个用于气体保护焊且可以后载入的备选软件包。用 KUKA.ArcTech Basic 可以配置各制造商的焊接电源。

```
• 配置焊接电源：
  ‒ 可以为每个电源配置多达 4 种焊接模式（运行方式）
  ‒ 为每种焊接模式定义与电源通讯的参数（信道）
  ‒ 定义电源参数的支点
  ‒ 将参数分配给流程（引弧、焊接、填满终端焊口）
  ‒ 根据标准数据组针对某些焊接任务定义焊接数据组
  ‒ 配置与电源和其他设备（例如 PLC）的通讯输入端/输出端
• 对简单焊接任务进行编程
• 配置引弧和焊接故障的故障策略
• 用于焊接大缝隙的机械摆动
• 在 smartHMI 上显示电源的故障信息（并非适用于所有电源）
• 简单示教
• 创建用户特有的摆动图形
```

### 2．ArcTech  Advanced

ArcTech Advanced 是一个可后载入的备选软件包，它对备选软件包 ArcTech Basic 的功能进行了如下扩展：

``` 
• 配置最多 10 个引燃和焊接故障的故障策略
• 摆动延迟
• 摆动振幅和 8 个可配置通道的轨迹逼近参数
• 迅速接通或关断电弧
• 通过上一级控制装置开通焊缝
• 将焊接速度传递给电源
• 用户特有的功能
• 配置多达 32 种焊接模式
• Advanced Error Recovery 策略
Ps：如果额外安装了 SeamTech Tracking 和/或 ArcSense 备选软件包，则不能使用 Advanced Error Recovery 策略
```

### 3．SeamTech Finding

SeamTech Finding 可以修正原先的轨迹，以便均衡工件的造型和位置偏差。

### 4．SeamTech Tracking

SeamTech Tracking 是一个用于接缝跟踪的程序。它可以配合光切传感器一起，用于大量的应用领域，例如气体保护焊接、激光焊接等。即便在摆动运动中也可以进行接缝跟踪和轨迹的修正,为此刀具的作业方向须为 Z 方向。
Ps：备选软件包 ArcTech Advanced 的“摆动延迟”选项受到 SeamTech Tracking 支持。

### 5．ArcSense

ArcSense 是一个可后载入的备选软件包，以 ArcTech Basic 为基础，用于传感器追踪的轨迹修正。
各个工件的焊缝位置及其走向并不总是完全相同。为了均衡工件的造型和位置偏差，常常须修正原有的轨迹。
用 ArcSense 可修正原有轨迹，使机器人找到实际的焊缝走向。ArcSense 可实现轨迹曲线至焊缝中心的侧面修正和焊嘴与工件之间的距离修正。

```
• 通过电流或电压曲线信号进行焊缝跟踪，包含侧向调整和高度调整
• 自动校准焊缝跟踪输入信号，无需事先调试
• 支持用于调节的模拟和数字输入信号
• 单独设置侧向和垂直的调节器增益
• 在无摆动运动的情况下进行高度调节
• 启动工艺流程时焊缝中心的查找功能
• 侧向偏移（偏量）功能
```

### 6．TouchSense

TouchSense 是一款在焊接应用中用于触觉或光学工件搜索的备选软件包。能够借助一个传感器识别工件的造型和小的位置偏差，校准焊缝的位置。

```
• 识别工件的外形和位置偏差：
  ‒ 动态测量工件的位置
  ‒ 静态测量工件的位置
  ‒ 扫描工件表面和检查焊缝形状
• 校准焊缝的位置
```

### 7．MultiLayer

MultiLayer 工艺程序包只用于对传统焊缝无法胜任的厚板材和工件进行气体保护焊。 由此能够使用多个焊缝和少量能量焊接耐高温材料。
通过该工艺程序包能够以根轨迹为基础通过编程的偏移量计算出新的轨迹。

```
• 以根焊缝为基础通过偏移值计算整个焊缝
• 除了轨迹偏移之外计算单点偏移
• 选择不同的传感器技术 （例如 ArcSense、SeamTechFinding、SeamTechTracking）
• 偏移轨迹以与根焊缝相同或相反的方向运动
```

### 8．LaserTech

LaserTech 是一个可后续载入的备选软件包，具有下列功能：

```
• 对激光器应用进行配置和编程 （LaserTech 标准软件包）
• 对用于激光切割的应用进行配置和编程 （LaserCut）
• 对用于带 / 不带填充焊丝激光焊接的应用进行配置和编程 （LaserWeld）
• 对最多 3 种自定义激光器应用进行配置和编程w
```

### 9．ServoGun Basic

ServoGun Basic 一个可后加载的备选软件包。它提供了用于运行电动点焊钳的基本功能。

```
• 控制多达 6 个电动焊钳
  ‒ 可以操作具有正传动比的焊钳以及具有负传动比的焊钳
• 补偿电极帽磨损、电极杆磨损和焊钳挠度
• 能够控制气动平衡系统
• 自动校准作用力
• 大量预配置的过程组件，如不同制造商的焊接控制系统和电机
• 对于固定式焊钳：进行铣削/焊接过程中，机器人轴可独立于焊钳执行搬运任务
• 调试助手
```

---

## 二．通讯配置类

### 1．PROFINET

PROFINET是一种基于以太网的现场总线。数据交换是在客户机-服务器基础上进行的，PROFINET 安装在机器人控制器上。

### 2．EtherNet/IP

EtherNet/IP也是一种基于以太网的现场总线。

### 3．Ethernet KRL

Ethernet KRL通讯数据通过TCP/IP 协议传输，机器人控制系统和外部系统作为客户端或服务器。

### 4．PLCmxAutomation

PLCmxAutomation 通过它可以通过外部PLC对机器人进行编程和控制。

### 5．RobotSensorlnterface

实现机器人控制系统和传感器系统之间的数据交换，通过传感器信号的处理对机器人运动或程序运行进行控制。

---

## 三．其他应用类

### 1．GlueTech

KUKA.GlueTech常用于涂胶应用中。

### 2．GripperSpotTech

GripperSpotTech 夹爪和点焊，常用在点焊、安装、机器上料、运输等应用领域。

### 3．ForceTorqueControl

力控软件，通过ForceTorqueControl和一个软件支持的力/力矩传感器系统，机器人得到了一种触觉。就能感觉录敏地对外力和外力矩作出反应，并在工件上施加编程的力和力矩。

### 4．ConveyorTech

ConvevorTech同步输送器，用于抓取．处理或放下任意结构输送器上的工件。

### 5．VectorMove

VectorMove矢量运动，主要用于压铸和注射成型技术，用于零件的拆卸。

### 6．Directory Loader

Directory Loader主要用于在机器人运行时载入KRL 模块，可配置待载入KRL模块所处的源目录以及机器人控制系统上的目标目录。

---

## 四．关于机器人系统的软件

### 1．LoadDataDetermination

LoadDataDetermination是KUKA负载测试软件，通过输入正确的载荷数据(质量．重心．惯性矩)，避免机器人的过载。

### 2．UserTech

UserTech是一个用户自定义的软件包，定义用户特定的联机表单．特定的工艺键和按键等。

### 3．RoboTeam

KUKA．RoboTeam可实现多个机器人或机器人与附加轴运动系统的协同作业。机器人协作时，轨迹运动在时间和几何上相互协调（时间和/或几何耦合）。

### 4．RemoteService

RemoteService是一个在线支持机器人控制器的软件包。

### 5．Robot LBS

KUKA.RobotLBs是KUKA新增的功能选项,用于连接机器人到库卡客户消费部门。用户可以在smartPAD 或微信应用程序上读取特定客户的文件。

### 6．DeviceConnector pre-installed

KUKA.DeviceConnectorpre-installed是一个出厂时安装的备选软件包。可实现连接到 KUKA云（例如 KUKA．Connect 或 KUKA smartProduction）。

### 7．DiagnosisSafety

DiagnosisSafety是一个安全诊断的软件包，用于确定安全控制系统妨碍机器人移动的原因。可以做出以下诊断:

```
• 安全输入端和输出端的诊断
• 安全组件的诊断
• 以太网安全接口信号的诊断
• 安全选项配置的诊断的诊断
```
