# shuju_yu_shiyan_guanli 模块代码规划

目标：建立数据与实验资产管理规范，避免“实验做完无法复现”。

## 建议新增文件与内容

| 文件名 | 应该写的代码内容 |
|---|---|
| `data_manifest.md` | 数据集来源、版本、字段说明、许可协议。 |
| `split_protocol.md` | 数据切分协议与防泄漏规则。 |
| `experiment_template.md` | 单次实验记录模板（数据、配置、结果、结论）。 |
| `ablation_template.md` | 消融实验模板（变量、对照、结果解释）。 |
| `result_table_template.csv` | 统一结果表头（指标、seed、耗时、参数量）。 |
| `error_analysis_template.md` | 错误样本分析模板（类型、原因、改进动作）。 |
| `reproducibility_checklist.md` | 可复现清单（种子、环境、版本、命令）。 |

## 完成标准

- 任意结果都能追溯到“数据版本 + 配置 + commit id”。  
- 每次实验都有结构化记录，而不是散落截图。  
- 形成固定复盘流程（结果 -> 错误分析 -> 下轮实验）。
