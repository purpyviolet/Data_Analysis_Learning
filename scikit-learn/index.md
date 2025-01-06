除了Scikit-learn 中模型部分，Scikit-learn 还有其他丰富的功能模块，可以进一步学习和实践：

------

### **1. 数据预处理与特征工程**

- **数据预处理工具**:
  - `StandardScaler`, `MinMaxScaler`, `RobustScaler`: 数据归一化和标准化。
  - `PolynomialFeatures`: 多项式特征扩展。
  - `Normalizer`: 数据规范化。
  - `Binarizer`: 二值化。
  - `Imputer` (新版用 `SimpleImputer`): 处理缺失值。
- **特征选择**:
  - `SelectKBest`, `RFE`, `SelectFromModel`: 选择最重要的特征。
  - `VarianceThreshold`: 基于方差的特征过滤。
- **编码与处理分类变量**:
  - `OneHotEncoder`: 独热编码。
  - `LabelEncoder`: 标签编码。
  - `OrdinalEncoder`: 序数编码。
- **处理不平衡数据**:
  - `SMOTE`, `ADASYN`: 增加少数类样本。

------

### **2. 模型评估与优化**

- **交叉验证**:
  - `cross_val_score`: 交叉验证评分。
  - `KFold`, `StratifiedKFold`, `TimeSeriesSplit`: 数据分割策略。
- **超参数调优**:
  - `GridSearchCV`: 网格搜索。
  - `RandomizedSearchCV`: 随机搜索。
  - `HalvingGridSearchCV`, `HalvingRandomSearchCV`: 半精度搜索。
- **模型评估指标**:
  - 分类: `accuracy_score`, `precision_score`, `recall_score`, `f1_score`, `roc_auc_score`。
  - 回归: `mean_squared_error`, `mean_absolute_error`, `r2_score`。
  - 聚类: `silhouette_score`, `adjusted_rand_score`。

------

### **3. 流水线 (Pipelines)**

- **Pipeline**:
  - 将数据预处理和模型训练结合，形成可复用的流程。
  - 如 `Pipeline(steps=[('scaler', StandardScaler()), ('model', LogisticRegression())])`。
- **FeatureUnion**:
  - 并行处理特征工程步骤。

------

### **4. 数据生成与采样**

- **数据集生成**:
  - 分类: `make_classification`, `make_moons`, `make_circles`。
  - 回归: `make_regression`, `make_friedman1`。
  - 聚类: `make_blobs`。
- **真实数据集加载**:
  - 内置数据集: `load_iris`, `load_digits`, `load_boston`（已弃用）等。
  - 外部数据集: `fetch_openml`, `fetch_california_housing`。

------

### **5. 非监督学习**

除了你已经了解的聚类与降维，还有：

- 孤立森林 (Isolation Forest):
  - 用于异常检测。
- 矩阵分解:
  - PCA 的扩展，如 `KernelPCA`, `SparsePCA`, `FactorAnalysis`。

------

### **6. 特殊任务模块**

- **序列预测**:
  - 时间序列交叉验证（`TimeSeriesSplit`）。
  - 通过手动扩展支持简单时间序列建模。
- **模型持久化**:
  - 使用 `joblib` 或 `pickle` 保存和加载模型。

------

### **7. 可解释性 (Interpretability)**

- 使用 

  ```
  sklearn.inspection
  ```

   模块进行模型解释：

  - `partial_dependence`: 部分依赖图。
  - `permutation_importance`: 特征重要性。

------

### **8. 自定义扩展**

- 自定义模型:
  - 实现自定义的 `BaseEstimator` 和 `TransformerMixin`。
- 自定义评分函数:
  - 使用 `make_scorer` 创建自定义评估指标。

------

### **建议学习路径**

1. 先学习 **数据预处理与特征工程**，掌握数据清洗与特征处理的流程。
2. 深入 **模型评估与优化**，提升模型性能。
3. 使用 **流水线** 整合完整的机器学习工作流。
4. 探索 **非监督学习** 和 **特殊任务模块**。