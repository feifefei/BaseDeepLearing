# jiqi_xuexi_jichu 模块代码规划

目标：把机器学习基础问题（泛化、过拟合、正则化、评估）做成标准实验脚手架。

## 建议新增文件与内容

| 文件名 | 应该写的代码内容 |
|---|---|
| `01_data_split_and_leakage_check.py` | 训练/验证/测试划分与数据泄漏自动检查。 |
| `02_empirical_risk_minimization.py` | 经验风险最小化流程，支持多损失函数。 |
| `03_underfit_overfit_demo.py` | 用模型容量和训练轮数演示欠拟合/过拟合。 |
| `04_bias_variance_tradeoff.py` | 通过采样实验分解偏差与方差。 |
| `05_loss_by_distribution.py` | 将回归/分类损失映射到概率假设（MSE, BCE, CE）。 |
| `06_regularization_suite.py` | L1/L2、Early Stopping、Dropout 的统一实验入口。 |
| `07_hyperparameter_search.py` | 网格搜索/随机搜索模板（可扩展 Optuna）。 |
| `08_metrics_classification.py` | Accuracy/Precision/Recall/F1/AUC 统一计算与可视化。 |
| `09_metrics_regression.py` | MSE/RMSE/MAE/R2 统一计算与残差图分析。 |

## 完成标准

- 每个训练实验都要同时输出训练集和验证集指标。  
- 至少 1 个脚本能自动检测并提示过拟合。  
- 形成统一评估接口，供后续模型复用。
