---
title: Multi-dataset Joint Pre-training of Emotional EEG Enables Generalizable Affective Computing
title_zh: 情感脑电图的多数据集联合预训练实现可泛化的情感计算
authors: "Qingzhu Zhang, Jiani Zhong, Li ZongSheng, Xinke Shen, Quanying Liu"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=xaxuzubN31"
tags: ["query:eeg"]
score: 6.0
evidence: 情感EEG的多数据集联合预训练，使用跨数据集协方差对齐
tldr: 现有EEG通用预训练模型在情感识别等复杂任务上表现不佳，原因是任务特定特征与泛化预训练之间存在不匹配。本文提出面向情感EEG的多数据集联合预训练框架，通过跨数据集协方差对齐解决分布差异和类别定义不一致问题。实验表明该方法在跨数据集情感识别上实现了鲁棒泛化。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-xaxuzubn31/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 689, \"height\": 529, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xaxuzubn31/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1441, \"height\": 1093, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xaxuzubn31/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1439, \"height\": 540, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xaxuzubn31/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1125, \"height\": 741, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xaxuzubn31/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1464, \"height\": 588, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xaxuzubn31/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1482, \"height\": 649, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xaxuzubn31/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1147, \"height\": 1829, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xaxuzubn31/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1438, \"height\": 948, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xaxuzubn31/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1459, \"height\": 1191, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-xaxuzubn31/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1445, \"height\": 385, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xaxuzubn31/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1539, \"height\": 312, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xaxuzubn31/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1469, \"height\": 1459, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xaxuzubn31/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1187, \"height\": 239, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xaxuzubn31/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 455, \"height\": 352, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xaxuzubn31/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1306, \"height\": 207, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xaxuzubn31/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1308, \"height\": 208, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xaxuzubn31/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 857, \"height\": 594, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xaxuzubn31/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1184, \"height\": 656, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xaxuzubn31/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1437, \"height\": 179, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xaxuzubn31/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1437, \"height\": 181, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xaxuzubn31/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1475, \"height\": 205, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xaxuzubn31/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1422, \"height\": 180, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xaxuzubn31/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 739, \"height\": 296, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xaxuzubn31/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1609, \"height\": 378, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xaxuzubn31/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 499, \"height\": 294, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xaxuzubn31/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 495, \"height\": 256, \"label\": \"Table\"}]"
motivation: 通用EEG预训练模型无法有效处理情感识别等复杂任务，存在任务特征不匹配和跨数据集差异。
method: 提出跨数据集协方差对齐损失，联合预训练多个情感EEG数据集，对齐二阶统计特性。
result: 在跨数据集情感识别任务上，无需大量微调即可取得鲁棒泛化性能。
conclusion: 任务特定的多数据集预训练策略可有效提升EEG情感计算的泛化能力。
---

## Abstract
Task-specific pre-training is essential when task representations diverge from generic pre-training features. Existing task-general pre-training EEG models struggle with complex tasks like emotion recognition due to mismatches between task-specific features and broad pre-training approaches. This work aims to develop a task-specific multi-dataset joint pre-training framework for cross-dataset emotion recognition, tackling problems of large inter-dataset distribution shifts, inconsistent emotion category definitions, and substantial inter-subject variability. We introduce a cross-dataset covariance alignment loss to align second-order statistical properties across datasets, enabling robust generalization without the need for extensive labels or per-subject calibration. To capture the long-term dependency and complex dynamics of EEG, we propose a hybrid encoder combining a Mamba-like linear attention channel encoder and a spatiotemporal dynamics model. Our method outperforms state-of-the-art large-scale EEG models by an average of 4.57% in AUROC for few-shot emotion recognition and 11.92% in accuracy for zero-shot generalization to a new dataset. Performance scales with the increase of datasets used in pre-training. Multi-dataset joint pre-training achieves a performance gain of 8.55\% over single-dataset training. This work provides a scalable framework for task-specific pre-training and highlights its benefit in generalizable affective computing. Our code is available at https://github.com/ncclab-sustech/mdJPT_nips2025.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与研究动机

- **背景**：现有EEG通用大模型（如LaBraM、MMM、EEGPT）通常采用跨任务异质数据预训练，在睡眠分期、异常检测等任务上表现良好，但在情感识别这类复杂任务上效果不佳。原因在于通用预训练提取的特征与任务特定表示之间存在严重不匹配，且大规模异质预训练会稀释任务相关信号。
- **核心问题**：情感EEG面临三大挑战：跨数据集分布偏移（不同设备、通道数、采样率）、情感类别定义不一致（如SEED为3类、SEED-IV为4类、FACED为9类）、个体间差异大。现有方法多采用一对一的域适应或需要逐个受试者微调，难以泛化到未见数据集或新情感类别。
- **研究目标**：开发一个任务特定的多数据集联合预训练框架，实现无需大量标注或逐个受试者校准的鲁棒跨数据集情感识别。

## 2. 方法论

### 2.1 核心思想
- 利用EEG信号在不同数据集中具有相似二阶统计特性（协方差结构）的先验，通过协方差对齐缩小分布差异。
- 结合对比学习进行跨主体对齐，学习情感相关表示，无需情感标签。

### 2.2 关键技术细节
1. **多数据集联合预训练框架 (mdJPT)**  
   - 三阶段流程：① 在多个数据集上预训练EEG编码器（使用CDA损失和ISA损失）；② 冻结编码器，在目标数据集少量标注受试者上微调分类器（MLP）；③ 在剩余受试者上测试。零样本设置则跳过微调阶段。
2. **混合时空编码器**  
   - **MLLA通道编码器**：将每个通道的EEG信号分割为重叠滑动片段，独立输入Mamba-like线性注意力模块，捕获长期依赖。该模块包含输入门、线性注意力、遗忘门，计算高效。
   - **时空动态模型**：先通过可训练空间投影层将多通道表示映射到潜在空间；再使用空间过渡卷积（带不同膨胀率的卷积核）提取多尺度时空变化模式；最后通过局部注意力机制动态加权，得到最终的EEG表示。
3. **跨数据集协方差对齐损失 (CDA Loss)**  
   - 在每个训练batch中，取每数据集两个受试者，计算每个受试者在隐空间表示的协方差矩阵的质心。
   - 对齐损失为所有受试者协方差质心之间的Frobenius距离（平方和再取对数），目的是使不同数据集的协方差结构尽可能相似。
4. **跨主体对齐损失 (ISA Loss)**  
   - 基于对比学习：同一刺激下不同受试者的样本构成正对，不同刺激的样本为负对。使用温度归一化交叉熵损失，拉近不同受试者相同情感状态的表示，推远不同情感状态的表示。

### 2.3 公式与算法流程（文字说明）
- CDA损失：对每个隐藏维度d，计算受试者s所有trial的协方差矩阵平均得到Γ_s^{(d)}，然后计算所有受试者两两之间的Frobenius距离和L_d，对所有维度求和后取log得到LCDA。
- ISA损失：对每个数据集m，对两个受试者A、B的样本，按时间对齐形成正对，计算InfoNCE损失。总损失L = L_ISA + λ L_CDA。

## 3. 实验设计

### 3.1 数据集
| 数据集         | 受试者数 | 试次数/人 | 情感类别数 | 通道数 | 采样率 |
|----------------|----------|-----------|------------|--------|--------|
| SEED           | 15       | 45        | 3          | 62     | 1000Hz |
| SEED-IV        | 15       | 72        | 4          | 62     | 1000Hz |
| SEED-V         | 16       | 45        | 5          | 62     | 1000Hz |
| SEED-VII       | 20       | 80        | 7          | 62     | 1000Hz |
| FACED          | 123(取前20)| 28       | 2或9       | 32     | 250/1000Hz|
| DEAP           | 32       | 40        | 2（效价/唤醒度二分）| 32 | 512Hz |

预处理：降采样至125Hz、带通滤波0.5-47Hz、ICA去伪迹、通道插值至标准60通道（10-20系统）、共平均参考。

### 3.2 Benchmark与对比方法
- 对比方法：DE基线（直接提取差分熵特征）、MMM、LaBraM、EEGPT（使用公开预训练权重）。
- 评估设置：
  - **少样本跨数据集分类**：目标数据集按1:3比例划分受试者（训练/测试），留一数据集验证。在6个数据集上循环留一，报告准确率、精确率、召回率、F1、AUROC。
  - **零样本泛化**：预训练后直接测试，基于余弦相似度最近邻分类。

## 4. 资源与算力
- 论文明确说明：所有实验在NVIDIA GeForce RTX 3090 GPU上运行，使用PyTorch 2.3.1框架，Adam优化器。
- 未给出具体训练时间、模型参数量（1.0M参数，小于对比模型），但未提训练周期具体耗时。

## 5. 实验数量与充分性
- 共进行了**两大类实验**：
  1. **少样本跨数据集分类**：在6个数据集上分别作为目标，报告5项指标，每个结果重复6次随机划分取均值标准差。
  2. **零样本泛化**：在6个数据集上报告准确率。
- **消融实验**：4组，包括CDA系数敏感性、ISA损失必要性、MLLA vs Transformer、时空动态模型 vs Transformer。
- **额外分析**：
  - 预训练数据集数量对性能的影响（以SEED-V为目标，逐步增加训练集）。
  - 从DEAP到其他数据集的迁移。
  - DEAP上做维度情感分类（唤醒度、优势度、效价-唤醒度四象限）。
  - EmoEEG-MC数据集（想象诱导）的泛化测试。
  - 特征可视化（t-SNE、轮廓系数）、特征重要性一致性分析。
- **充分性**：实验覆盖了多个数据集、两种泛化场景、多种消融、模型规模对比、迁移验证，设计较为充分。但未报告统计显著性检验（如t检验）。

## 6. 主要结论与发现
1. mdJPT在少样本跨数据集情感识别上平均AUROC比SOTA方法提升4.57%，准确率（零样本）提升11.92%。
2. 预训练数据集越多，性能越好（最佳比单数据集训练提升8.55%）。
3. CDA损失和ISA损失均不可或缺，ISA损失对学习情感表示至关重要。
4. MLLA编码器优于标准Transformer，时空动态模型优于Transformer层。
5. 模型参数更少（1.0M），性能更强，证明任务特定预训练优于通用预训练。

## 7. 优点
- **任务特定预训练思路**：针对情感EEG设计，利用协方差对齐和对比学习，有效解决跨数据集、跨主体分布差异。
- **损失设计巧妙**：CDA损失无需标签，仅对齐二阶统计量；ISA损失利用时间对齐提供强监督信号，无需情感类别标签，解决类别定义不一致问题。
- **编码器高效**：MLLA线性注意力降低计算复杂度，时空动态模型符合EEG生理特性。
- **实验全面**：在多个数据集、多种设置下验证，消融清晰，可视化丰富。
- **开源代码**：提供GitHub链接，可复现。

## 8. 不足与局限
- **细粒度情感性能仍有限**：在FACED的9分类任务上准确率仅23.46%，未达到实用水平，残差分布偏移尚存。
- **情感诱发范式单一**：主要基于视频诱发，对想象/自传体诱发等内部情感（EmoEEG-MC）泛化较差（20.56%），跨上下文能力待提升。
- **未建模个体差异**：忽略受试者情感体验的个体差异性，可能遗漏细微情感状态。
- **人口多样性不足**：当前情感EEG数据集受试者年龄、文化、健康状态有限，结果外推性受限。
- **伦理风险**：存在情感监控或画像的潜在滥用风险，需加强隐私保护框架。
- **缺少统计显著性检验**：结果以均值±标准差报告，未做配对t检验等，说服力稍弱。
- **硬件限制**：EEG穿戴设备尚未普及，实际部署困难。

（完）
