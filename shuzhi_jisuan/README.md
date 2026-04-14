# shuzhi_jisuan 模块代码规划

目标：解决训练中常见的数值问题，形成稳定实现模板。

## 建议新增文件与内容

| 文件名 | 应该写的代码内容 |
|---|---|
| `01_floating_point_limits.py` | 展示 float32/float64 的范围、精度、上溢下溢示例。 |
| `02_stable_softmax.py` | 对比 naive softmax 与减最大值 softmax 的稳定性。 |
| `03_logsumexp_demo.py` | 实现稳定 `logsumexp`，并验证与 `log_softmax` 一致性。 |
| `04_gradient_check.py` | 数值梯度 vs 反向传播梯度一致性检查。 |
| `05_jacobian_hessian_demo.py` | Jacobian/Hessian 的数值构造与几何解释。 |
| `06_optimization_landscape.py` | 可视化局部最小、鞍点，分析优化难点。 |
| `07_sgd_momentum_adam_compare.py` | 比较不同优化器收敛速度与稳定性。 |
| `08_condition_number_effect.py` | 展示病态矩阵对优化/求解稳定性的影响。 |

## 完成标准

- 至少建立 1 套“稳定实现函数库”（softmax/logsumexp/loss）。  
- 至少建立 1 个自动梯度检查脚本。  
- 至少 1 份对比报告解释数值技巧带来的收益。
