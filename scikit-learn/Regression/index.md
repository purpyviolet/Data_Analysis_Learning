在回归问题中，目标是预测一个连续值，而不是分类。回归模型的类型主要分为以下几大类，涵盖了 **Scikit-learn** 和常见的扩展库中的模型：

------

### **1. 线性回归模型 (Linear Regression Models)**

- **Linear Regression**: 线性回归
- **Ridge Regression**: 岭回归
- **Lasso Regression**: Lasso回归
- **ElasticNet Regression**: 弹性网络回归
- **Bayesian Ridge Regression**: 贝叶斯岭回归
- **Orthogonal Matching Pursuit (OMP)**: 正交匹配追踪
- **Least Angle Regression (LARS)**: 最小角回归
- **Huber Regression**: Huber回归（对异常值鲁棒）

------

### **2. 支持向量回归 (Support Vector Regression)**

- **Support Vector Regression (SVR)**: 支持向量回归
- **Nu-Support Vector Regression (NuSVR)**: Nu-支持向量回归

------

### **3. 树回归模型 (Tree-Based Regression Models)**

- **Decision Tree Regressor**: 决策树回归
- **Random Forest Regressor**: 随机森林回归
- **Extra Trees Regressor**: 极端随机树回归
- **Gradient Boosting Regressor**: 梯度提升回归
- **XGBoost Regressor**: XGBoost回归
- **LightGBM Regressor**: LightGBM回归
- **CatBoost Regressor**: CatBoost回归

------

### **4. 贝叶斯回归模型 (Bayesian Regression Models)**

- **Gaussian Process Regression**: 高斯过程回归
- **Bayesian Ridge Regression**: 贝叶斯岭回归
- **Automatic Relevance Determination (ARD) Regression**: 自动相关确定回归

------

### **5. 基于最近邻的回归模型 (Nearest Neighbor Regression Models)**

- **K-Neighbors Regressor**: K-最近邻回归
- **Radius Neighbors Regressor**: 半径最近邻回归

------

### **6. 基于核的回归模型 (Kernel-Based Regression Models)**

- **Kernel Ridge Regression**: 核岭回归
- **Gaussian Process Regression**: 高斯过程回归（也属于贝叶斯回归）

------

### **7. 基于神经网络的回归模型 (Neural Network Regression Models)**

- **MLPRegressor (Multi-layer Perceptron Regressor)**: 多层感知机回归

------

### **8. 鲁棒回归模型 (Robust Regression Models)**

- **Huber Regressor**: Huber回归
- **Theil-Sen Estimator**: Theil-Sen估计
- **RANSAC Regressor (Random Sample Consensus)**: 随机样本一致回归

------

### **9. 半监督回归模型 (Semi-Supervised Regression Models)**

- **Label Spreading**: 标签传播回归
- **Label Propagation**: 标签传递回归

------

### **10. 混合模型 (Ensemble Regression Models)**

- **Voting Regressor**: 投票回归
- **Stacking Regressor**: 堆叠回归
- **Bagging Regressor**: 装袋回归

------

### **11. 时间序列回归模型 (Time Series Regression Models)**

（需要扩展库如 `statsmodels` 或 `pmdarima`）

- **ARIMA (AutoRegressive Integrated Moving Average)**: 自回归积分滑动平均
- **SARIMA (Seasonal ARIMA)**: 季节性ARIMA
- **VAR (Vector AutoRegression)**: 向量自回归
- **LSTM (Long Short-Term Memory)**: 长短时记忆网络

------

### **总结对比表**

| **类型**             | **英文**                           | **常见模型**                       |
| -------------------- | ---------------------------------- | ---------------------------------- |
| **线性回归模型**     | Linear Regression Models           | Linear, Ridge, Lasso, ElasticNet   |
| **支持向量回归**     | Support Vector Regression          | SVR, NuSVR                         |
| **树回归模型**       | Tree-Based Regression Models       | Decision Tree, Random Forest       |
| **贝叶斯回归模型**   | Bayesian Regression Models         | Gaussian Process, Bayesian Ridge   |
| **最近邻回归模型**   | Nearest Neighbor Regression Models | K-Neighbors, Radius Neighbors      |
| **基于核的回归模型** | Kernel-Based Regression Models     | Kernel Ridge, Gaussian Process     |
| **神经网络回归模型** | Neural Network Regression Models   | MLPRegressor                       |
| **鲁棒回归模型**     | Robust Regression Models           | Huber, Theil-Sen, RANSAC           |
| **半监督回归模型**   | Semi-Supervised Regression Models  | Label Spreading, Label Propagation |
| **混合模型**         | Ensemble Regression Models         | Voting, Stacking, Bagging          |
| **时间序列回归模型** | Time Series Regression Models      | ARIMA, SARIMA, VAR, LSTM           |

------

### **扩展说明**

1. **Scikit-learn 原生支持**：
   - Scikit-learn 提供了大部分通用回归模型，如线性回归、树模型、支持向量机等。
2. **扩展库支持**：
   - 深度学习回归（如 `LSTM`）需使用框架如 TensorFlow 或 PyTorch。
   - 时间序列回归（如 `ARIMA`、`SARIMA`）通常使用 `statsmodels` 或 `pmdarima`。
