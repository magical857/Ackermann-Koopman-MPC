# Ackermann-Koopman-MPC

基于Koopman算子理论和LSTM自编码器的Ackermann车辆模型预测控制项目

## 项目目标
- 实现基于Koopman算子理论的Ackermann车辆模型预测控制。
- 使用LSTM自编码器进行数据压缩和特征提取。

## 技术栈
- MATLAB
- Python
- LSTM
- Koopman算子

## 安装说明
### MATLAB
1. 确保安装了MATLAB R2018b或更高版本。
2. 下载并安装所需的工具箱。

### Python
1. 安装Python 3.7或更高版本。
2. 使用以下命令安装依赖：
   ```bash
   pip install -r requirements.txt
   ```

## 快速入门指南
1. **数据收集（MATLAB）**  
   在MATLAB中运行数据收集脚本以获取训练数据。
2. **训练Koopman模型（Python）**  
   运行训练脚本以训练Koopman模型。
3. **模型评估**  
   使用评估脚本评估模型性能。

## 项目结构概述
```
Ackermann-Koopman-MPC/
├── data/             # 存放数据
├── docs/             # 文档
├── notebooks/        # Jupyter笔记本
├── src/             # 源代码
├── requirements.txt  # Python依赖
└── README.md        # 项目说明
```

## 理论背景
### Ackermann转向模型方程
- 车辆动力学模型，描述了车辆的运动行为。

### Koopman算子理论
- 提供了一种分析非线性动力系统的方式，使用线性算子来描述其演化。

## LSTM自编码器架构
- 包含编码器和解码器，用于特征提取和数据重建。

## 训练配置
- **超参数**：
  - 学习率：0.001
  - 批大小：32
  - 训练周期：100

## 可视化结果描述
- 结果图表展示了模型预测与实际数据的对比。

## 文档链接
- [项目文档](docs/index.md)

## Jupyter笔记本描述
- 提供了用于数据分析和模型评估的Jupyter笔记本。

## 贡献指南
- 欢迎贡献者提交问题和拉取请求。

## MIT许可证
本项目采用MIT许可证，详见LICENSE文件。

## 作者
- magical857

## 感谢
- 感谢所有参与和支持本项目的人。