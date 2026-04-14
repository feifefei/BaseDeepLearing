# gailv_yu_xinxi_lun 模块代码规划

目标：把概率与信息论从“会背公式”变成“会写实验验证”。

## 建议新增文件与内容

| 文件名 | 应该写的代码内容 |
|---|---|
| `01_probability_basics.py` | 用模拟实验验证期望、方差、大数定律。 |
| `02_bayes_update_demo.py` | 从先验到后验的贝叶斯更新流程（可用 Beta-Bernoulli）。 |
| `03_covariance_vs_independence.py` | 演示“协方差为 0 但不独立”的反例。 |
| `04_multivariate_gaussian_demo.py` | 可视化多元高斯等密度椭球与协方差矩阵关系。 |
| `05_clt_simulation.py` | 中心极限定理数值实验（不同分布收敛到正态）。 |
| `06_entropy_crossentropy_kl.py` | 实现并比较熵、交叉熵、KL（含离散与连续版本）。 |
| `07_mle_map_compare.py` | 最大似然 MLE 与最大后验 MAP 的代码对比。 |
| `08_observation_vs_intervention.py` | 区分 `P(Y|X)` 与 `P(Y|do(X))` 的简化因果实验。 |

## 完成标准

- 每个理论点至少有 1 个“可重复随机实验”。  
- 至少 2 张图展示概率概念（分布、收敛、散度）。  
- 输出统一格式的实验结论，方便后续写报告或笔记。
