# duibi_chuantong_biaoshi_shendu 模块代码规划

目标：系统比较传统机器学习、表示学习、深度学习在同一数据与同一评估协议下的差异。

## 建议新增文件与内容

| 文件名 | 应该写的代码内容 |
|---|---|
| `01_data_prepare.py` | 统一数据读取、清洗、标准化、训练/验证/测试划分。 |
| `02_traditional_ml_baselines.py` | 传统机器学习基线（如逻辑回归、SVM、随机森林）。 |
| `03_representation_learning_baselines.py` | 表示学习基线（如 PCA + 线性分类、AutoEncoder + 线性分类）。 |
| `04_deep_learning_baselines.py` | 深度学习基线（MLP/CNN，视数据类型选择）。 |
| `05_unified_train_eval.py` | 统一训练和评估入口，保证三类方法可公平比较。 |
| `06_metrics_and_report.py` | 输出 Accuracy/F1/AUC、训练时间、参数量、推理耗时。 |
| `07_visual_compare.py` | 画学习曲线、混淆矩阵、表示空间投影图。 |
| `08_case_study.md` | 记录“什么场景传统方法更优、什么场景深度学习更优”。 |

## 对比实验必须统一的约束

- 统一随机种子与数据划分。  
- 统一评估指标与统计口径。  
- 统一预处理流程（避免暗中偏向某类模型）。

## 完成标准

- 至少 1 组公开数据 + 1 组自定义数据完成三类方法对比。  
- 至少 1 张表格覆盖“精度、效率、参数量、鲁棒性”四维比较。  
- 能回答“为什么这个任务里表示学习/深度学习有效或无效”。
