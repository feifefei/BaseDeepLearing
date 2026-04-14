# BaseDeepLearing 学习与实验仓库

这个仓库当前定位：

- `question.md`：第一部分理论笔记（已扩展）。
- 各章节目录：**只放“代码规划说明”**，不放具体实现代码。
- 目标：先把实验结构搭好，再逐步补代码，确保完整、可复现、可对比。

## 当前目录结构

```text
.
├── question.md
├── yinyan/
├── xianxingdaishu/
├── gailv_yu_xinxi_lun/
├── shuzhi_jisuan/
├── jiqi_xuexi_jichu/
├── duibi_chuantong_biaoshi_shendu/
├── gongchenghua_xunlian/
└── shuju_yu_shiyan_guanli/
```

## 每个目录负责什么

| 目录 | 作用 | 你接下来要补的代码类型 |
|---|---|---|
| `yinyan/` | 引言与表示学习 | 感知机/XOR、反向传播、激活函数、表示可视化 |
| `xianxingdaishu/` | 线性代数 | 特征分解、SVD、范数、二次型、条件数 |
| `gailv_yu_xinxi_lun/` | 概率与信息论 | Bayes 更新、CLT、熵/交叉熵/KL、因果对比 |
| `shuzhi_jisuan/` | 数值计算 | 稳定 softmax、logsumexp、梯度检查、优化器对比 |
| `jiqi_xuexi_jichu/` | 机器学习基础 | 数据划分、防泄漏、泛化、正则化、指标评估 |
| `duibi_chuantong_biaoshi_shendu/` | 三类方法对比 | 统一数据协议下的传统/表示/深度学习对照实验 |
| `gongchenghua_xunlian/` | 工程化训练 | train/evaluate/infer 入口、配置、日志、checkpoint |
| `shuju_yu_shiyan_guanli/` | 数据与实验管理 | 实验模板、结果表、可复现检查清单 |

## 使用方式

1. 打开每个目录下的 `README.md`。  
2. 按 README 中“建议新增文件与内容”创建代码文件。  
3. 每补完一个文件，就在对应 README 打勾并记录实验结果。  
4. 优先完成 `duibi_chuantong_biaoshi_shendu/`，先把主线跑通。

## 推荐实施顺序

1. `duibi_chuantong_biaoshi_shendu/`：先得到第一版对比结论。  
2. `yinyan/` + `xianxingdaishu/`：补理论支撑和基础算子理解。  
3. `gailv_yu_xinxi_lun/` + `shuzhi_jisuan/`：补损失函数与稳定训练。  
4. `jiqi_xuexi_jichu/`：建立标准评估流程。  
5. `gongchenghua_xunlian/` + `shuju_yu_shiyan_guanli/`：工程化与复现闭环。

## 备注

- 本阶段故意不放实现代码，避免目录被早期草稿污染。  
- 代码补全后建议统一风格（格式化、日志格式、参数命名、随机种子控制）。
