# xianxingdaishu 模块代码规划

目标：把线性代数中的关键概念（特征分解、SVD、范数、条件数、二次型）做成可验证的代码实验。

## 建议新增文件与内容

| 文件名 | 应该写的代码内容 |
|---|---|
| `01_matrix_basics.py` | 向量/矩阵乘法、维度检查、广播与常见 shape 错误示例。 |
| `02_rank_and_solve.py` | `rank(A)` 与 `rank([A|b])` 判定方程是否有解，展示唯一解/多解/无解。 |
| `03_inverse_and_geometry.py` | 2D 线性变换与逆变换可视化，解释可逆条件。 |
| `04_norms_compare.py` | 比较 `L1/L2/Linf/Frobenius`，特别说明为什么 `||x||_2^2` 不是范数。 |
| `05_eigendecomposition_demo.py` | 手动验证 `A=VΛV^{-1}` 条件，演示不可对角化情形。 |
| `06_symmetric_matrix_properties.py` | 实对称矩阵的实特征值与正交特征向量验证。 |
| `07_quadratic_form_visualization.py` | 可视化 `x^T A x` 等高线，并和特征值符号关联。 |
| `08_svd_low_rank_approx.py` | 基于 SVD 做低秩近似、重构误差曲线。 |
| `09_trace_tricks.py` | 用 trace 恒等式验证常见矩阵推导（如二次型期望）。 |
| `svd.ipynb` | 保留现有 notebook，建议升级为 SVD + PCA + 压缩效果总实验。 |

## 最小完成顺序

1. 先做 `01~04`（打基础）。  
2. 再做 `05~07`（连接到优化与曲率）。  
3. 最后做 `08~09`（对接深度学习工程场景）。

## 完成标准

- 每个数学结论至少有一段“数值验证代码”。  
- 至少 2 个脚本包含图像输出（几何直觉）。  
- 形成一个可直接复用的 `linear_algebra_utils`（后续在训练脚本中调用）。
