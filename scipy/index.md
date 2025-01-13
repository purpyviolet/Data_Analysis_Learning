### **Scipy 学习大纲**

Scipy 是一个强大的科学计算库，包含多种工具箱，广泛应用于科学计算和数据分析。以下是详细的学习大纲，分为各类别和重点内容：

------

### **1. 基础知识**

#### **1.1 Scipy 概述**

- Scipy 与 Numpy 的关系。
- Scipy 的核心模块简介。

#### **1.2 Scipy 安装与配置**

- Scipy 的安装。
- 环境配置与基础使用。

------

### **2. 线性代数模块 (`scipy.linalg`)**

- 矩阵和向量运算：
  - 矩阵求逆：`inv`
  - 矩阵行列式：`det`
  - 矩阵特征值和特征向量：`eig`
- 奇异值分解 (SVD)：`svd`
- 求解线性方程组：`solve`
- 分块矩阵：`block_diag`

------

### **==3. 优化模块 (`scipy.optimize`)==**

- 单变量函数优化：
  - `minimize_scalar`，`brent`
- 多变量函数优化：
  - `minimize`，支持算法如 Nelder-Mead、BFGS。
- 非线性方程组求解：
  - `root`，`fsolve`
- 曲线拟合：
  - `curve_fit`
- 全局优化：
  - `basinhopping`，`differential_evolution`

------

### **4. 插值模块 (`scipy.interpolate`)**

- 一维插值：
  - `interp1d`
- 多维插值：
  - `griddata`，`Rbf`
- 样条插值：
  - `splrep` 和 `splev`
  - `UnivariateSpline`

------

### **5. 数值积分和微分模块 (`scipy.integrate`)**

- 一维积分：
  - `quad`，`dblquad`，`tplquad`
- 多维积分：
  - `nquad`
- 常微分方程 (ODE) 求解：
  - `solve_ivp`
- 数值微分：
  - `derivative`，`quad_explain`

------

### **6. 信号处理模块 (`scipy.signal`)**

- 滤波器设计：
  - FIR 和 IIR 滤波器。
- 信号卷积和去卷积：
  - `convolve`，`deconvolve`
- 窗函数：
  - `get_window`
- 傅里叶变换：
  - `spectrogram`，`hilbert`

------

### **7. 稀疏矩阵模块 (`scipy.sparse`)**

- 创建稀疏矩阵：
  - `csr_matrix`，`csc_matrix`
- 稀疏矩阵运算：
  - 稀疏矩阵加减乘除。
- 稀疏矩阵存储和加载：
  - `save_npz`，`load_npz`

------

### **8. 图论算法 (`scipy.sparse.csgraph`)**

- 图的表示：
  - 邻接矩阵表示图。
- 最短路径算法：
  - `shortest_path`，`dijkstra`
- 最小生成树：
  - `minimum_spanning_tree`
- 连通分量分析：
  - `connected_components`

------

### ==**9. 统计模块 (`scipy.stats`)**==

- 概率分布：
  - 连续分布和离散分布：`norm`，`binom`，`poisson`
- 假设检验：
  - `ttest_1samp`，`ttest_ind`，`chi2_contingency`
- 描述统计：
  - 均值、中位数、方差、偏度、峰度。
- 相关性分析：
  - `pearsonr`，`spearmanr`

------

### **10. 图像处理模块 (`scipy.ndimage`)**

- 图像变换：
  - 平移、旋转、缩放。
- 图像过滤：
  - 高斯滤波：`gaussian_filter`
- 形态学操作：
  - 腐蚀、膨胀、开闭运算。

------

### **11. 文件输入输出 (`scipy.io`)**

- 读取和保存 MATLAB 文件：
  - `loadmat`，`savemat`
- 读取和保存其他格式文件。

------

### **12. 空间计算模块 (`scipy.spatial`)**

- 距离计算：
  - `distance_matrix`，`pdist`，`cdist`
- 最近邻搜索：
  - KD 树 (`KDTree`) 和球树 (`BallTree`)。
- 凸包和 Delaunay 三角剖分：
  - `ConvexHull`，`Delaunay`

------

### **13. 随机数生成 (`scipy.stats` 和 `scipy.special`)**

- 随机数生成：
  - 各种分布的随机数：`norm.rvs`，`binom.rvs`
- 特殊函数：
  - 伽马函数、贝塞尔函数、阶乘函数。

