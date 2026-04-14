# gongchenghua_xunlian 模块代码规划

目标：把“实验脚本”升级为“可维护训练工程”。

## 建议新增文件与内容

| 文件名 | 应该写的代码内容 |
|---|---|
| `train.py` | 统一训练入口，支持配置文件、日志、断点恢复。 |
| `evaluate.py` | 独立评估入口，读取 checkpoint 输出完整指标。 |
| `infer.py` | 推理入口，支持单样本与批量推理。 |
| `models/__init__.py` | 模型注册机制，按名称加载模型。 |
| `datasets/__init__.py` | 数据集注册与 DataLoader 构建。 |
| `losses/__init__.py` | 损失函数注册，便于切换。 |
| `optimizers/__init__.py` | 优化器与学习率调度器封装。 |
| `utils/seed.py` | 随机种子与可复现设置。 |
| `utils/logger.py` | 统一日志输出（控制台 + 文件）。 |
| `utils/checkpoint.py` | 模型存取、最佳模型保存、恢复训练。 |
| `configs/base.yaml` | 全局默认配置。 |
| `configs/experiments/*.yaml` | 各实验独立配置，避免硬编码。 |

## 完成标准

- 训练、评估、推理三入口分离。  
- 配置文件可复现实验，不依赖手改脚本。  
- 任意实验可通过“命令 + 配置”一键复跑。
