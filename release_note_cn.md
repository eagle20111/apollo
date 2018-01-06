
[原版地址][original_url]

#2.0发布

这版本支持在简单的市郊路段自动驾驶。车辆能巡航并且躲避障碍物，在交通信号灯前停下，如果有必要会换道以到达目的地。  

##主要新功能和改进
* 新增交通信号灯检测
* 新增障碍物分类，支持障碍物类别：车辆，行人，骑自行车的人，未知物体
* 提升规划能力，能通过换道以抵达目的地
* 新增点云定位算法，结合了RTK(real time kinematic,实时动态)
* 新增MPC控制算法
* 为路况预测新增RNN模型
* 将HMI和DreamView整合
* 重新设计并升级了DreamView，新增了可视化调试工具
* 新增调试工具(modules/tools)
* 通过安全的OTA升级正式环境docker镜像
* 新增USB摄像头和雷达驱动支持

##自动驾驶能力
这个版本的车辆能够在有信号灯的，中等交通流量的简单市郊路段自动行驶，速度从慢速到中速。

##1.5发布
这版本支持车辆在固定道路上自动巡航。

##主要新功能和改进
* 新增路由，感知，预测，规划和端到端
 * 感知：GPU支持的3D点云的障碍物检测和跟踪
 * 预测：深度神经网络MLP预测模型和多预测器，处理不同的障碍物类别
 * 规划：交规模块，路径和速度的多迭代DP和QP优化
 * 端到端：混合深度神经网络模型,纵向控制有卷积LSTM，横向有FCNN
* 新增HD地图引擎API
* 新增Velodyne 64 LiDAR驱动支持
* 新增调试工具（modules/tools）
* 提升HMI和DreamView功能，允许实时交通显示和场景回放
##自动驾驶能力
本版本车辆**不能**检测到交通信号灯。车辆**不会**在红灯前停下。他们也不会在路上换道。

#1.0发布
初始版本，无人自动GPS路径跟随的阿波罗项目
##主要新功能和改进
* 包括定位，控制
 * 定位：RTK
 * 控制：纵向用矫正表，横向用LQR
* 新增GPS/IMU gnss驱动支持
* 用HMI记录和回放轨迹，DreamView可视化车辆轨迹
* 包含调试工具（modules/tools）
##自动驾驶能力
这个版本的车辆**不能**感知近距离障碍物。也不能驾驶在公共道路或者没有GPS信号的区域。

[original_url]: https://github.com/ApolloAuto/apollo/blob/master/RELEASE.md "Release Note"