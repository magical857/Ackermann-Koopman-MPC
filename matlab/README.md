# MATLAB仿真部分

本部分使用MATLAB/Simulink实现Ackermann车辆模型的MPC控制和数据采集。

## 环境要求

- MATLAB R2020b或更高版本
- **必需工具箱**:
  - Robotics System Toolbox
  - Control System Toolbox
- **可选工具箱**:
  - Model Predictive Control Toolbox (用于高级MPC)
  - Automated Driving Toolbox (用于高级可视化)

## 使用MATLAB官方Ackermann模型

本项目使用MATLAB官方提供的Ackermann驱动车辆模型：
- 参考: https://www.mathworks.com/help/robotics/ug/plot-ackermann-drive-vehicle-in-simulink.html

## 快速开始

### 方式1: 使用Simulink模型（推荐）

```matlab
% 打开Simulink模型
open_system('ackermann_mpc_tracking.slx')

% 运行仿真
sim('ackermann_mpc_tracking.slx')
```

### 方式2: 使用纯MATLAB脚本

```matlab
% 运行数据采集脚本
run main_collect_data.m
```

## 文件说明

- `main_collect_data.m` - 主数据采集脚本
- `main_with_robotics_toolbox.m` - 使用Robotics Toolbox的版本
- `ackermann_mpc_tracking.slx` - Simulink模型（推荐）
- `models/` - 车辆模型定义
- `controllers/` - 控制器实现
- `trajectories/` - 轨迹生成
- `utils/` - 工具函数

## 输出数据

仿真完成后，数据保存在 `../data/raw/`:
- `trajectory_data.mat` - MATLAB格式
- `trajectory_data.csv` - CSV格式（用于Python）

数据包含:
- `time` - 时间向量
- `states` - 状态 [x, y, theta, v]
- `controls` - 控制 [a, delta]
- `reference` - 参考轨迹
