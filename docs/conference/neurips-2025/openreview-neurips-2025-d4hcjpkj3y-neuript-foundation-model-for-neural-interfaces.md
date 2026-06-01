---
title: "NeurIPT: Foundation Model for Neural Interfaces"
title_zh: NeurIPT：面向神经接口的基础模型
authors: "Zitao Fang, CHENXUAN LI, Zhou Hongting, Shuyang Yu, Guodong DU, Ashwaq Qasem, Yang Lu, Jing Li, Junsong Zhang, Sim Kuan Goh"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=D4hcJPkJ3y"
tags: ["query:eeg-latent"]
score: 9.0
evidence: 基于预训练Transformer的脑电图基础模型用于潜在时空表征
tldr: 脑电图（EEG）基础模型面临跨被试、跨任务和不同电极配置的挑战。本文提出NeurIPT，一个专门用于神经接口的基础模型，采用预训练Transformer同时捕获EEG信号中的同质和异质时空特征。通过在大规模多样EEG数据上预训练，NeurIPT在多个下游任务中展现了强大的泛化能力，为EEG通用表示学习提供了新范式。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4hcjpkj3y/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1452, \"height\": 544, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4hcjpkj3y/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 674, \"height\": 894, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4hcjpkj3y/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1450, \"height\": 635, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4hcjpkj3y/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1457, \"height\": 491, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4hcjpkj3y/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 508, \"height\": 551, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4hcjpkj3y/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1459, \"height\": 388, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4hcjpkj3y/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 956, \"height\": 649, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4hcjpkj3y/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1337, \"height\": 2138, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4hcjpkj3y/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1465, \"height\": 392, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4hcjpkj3y/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1464, \"height\": 395, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4hcjpkj3y/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1465, \"height\": 394, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4hcjpkj3y/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1465, \"height\": 395, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4hcjpkj3y/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1466, \"height\": 393, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4hcjpkj3y/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1466, \"height\": 396, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4hcjpkj3y/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1466, \"height\": 395, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4hcjpkj3y/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1421, \"height\": 333, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4hcjpkj3y/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1197, \"height\": 446, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4hcjpkj3y/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1208, \"height\": 452, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4hcjpkj3y/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1197, \"height\": 448, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-d4hcjpkj3y/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1435, \"height\": 519, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1449, \"height\": 348, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1455, \"height\": 1519, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1429, \"height\": 196, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1372, \"height\": 211, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1365, \"height\": 282, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1232, \"height\": 332, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1224, \"height\": 164, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 440, \"height\": 240, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 508, \"height\": 137, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1081, \"height\": 527, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1229, \"height\": 672, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1011, \"height\": 383, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 845, \"height\": 231, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1027, \"height\": 1187, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 526, \"height\": 471, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 722, \"height\": 485, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 659, \"height\": 482, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1028, \"height\": 456, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1026, \"height\": 457, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1031, \"height\": 255, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 1031, \"height\": 455, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 1027, \"height\": 254, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 1027, \"height\": 455, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-d4hcjpkj3y/table-024.webp\", \"caption\": \"\", \"page\": 0, \"index\": 24, \"width\": 1453, \"height\": 473, \"label\": \"Table\"}]"
motivation: 现有EEG基础模型难以应对跨被试、跨任务和电极配置的多样性。
method: 提出NeurIPT，使用预训练Transformer捕捉EEG信号的同质和异质时空特性。
result: 在多种EEG下游任务上取得优异性能，验证了模型的有效泛化能力。
conclusion: 为EEG通用表征学习和神经接口应用提供了可扩展的基础模型框架。
---

## Abstract
Electroencephalography (EEG) has wide-ranging applications, from clinical diagnosis to brain-computer interfaces (BCIs). With the increasing volume and variety of EEG data, there has been growing interest in establishing foundation models (FMs) to scale up and generalize neural decoding. Despite showing early potential, applying FMs to EEG remains challenging due to substantial inter-subject, inter-task, and inter-condition variability, as well as diverse electrode configurations across recording setups. To tackle these open challenges, we propose **NeurIPT**, a foundation model tailored for diverse EEG-based **Neur**al **I**nterfaces with a **P**re-trained **T**ransformer by capturing both homogeneous and heterogeneous spatio-temporal characteristics inherent in EEG signals. Temporally, we introduce Amplitude-Aware Masked Pretraining (AAMP), masking based on signal amplitude rather than random intervals, to learn robust representations across varying signal intensities beyond local interpolation. Moreover, this temporal representation is enhanced by a progressive Mixture-of-Experts (MoE) architecture, where specialized expert subnetworks are progressively introduced at deeper layers, adapting effectively to the diverse temporal characteristics of EEG signals. Spatially, NeurIPT leverages the 3D physical coordinates of electrodes, enabling effective transfer across varying EEG settings, and develops Intra-Inter Lobe Pooling (IILP) during fine-tuning to efficiently exploit regional brain features. Empirical evaluations across nine downstream BCI datasets, via fine-tuning and training from scratch, demonstrated NeurIPT consistently achieved state-of-the-art performance, highlighting its broad applicability and robust generalization. Our work pushes forward the state of FMs in EEG and offers insights into scalable and generalizable neural information processing systems.

---

## 论文详细总结（自动生成）

# NeurIPT：面向神经接口的基础模型 — 论文详细中文总结

## 1. 核心问题与整体含义

- **研究动机**：脑电图（EEG）在临床诊断、脑-机接口（BCI）等领域应用广泛，但现有深度学习模型通常针对特定任务和设置，泛化能力差。基础模型（Foundation Models）在 NLP 和 CV 中取得巨大成功，但将其应用于 EEG 面临三大挑战：① 电极通道的物理三维空间关系常被忽略；② 主流的随机掩码预训练策略引导模型学习局部插值而非全局表示；③ 现有架构在微调时未充分利用脑区区域特征。
- **整体含义**：本文提出 **NeurIPT**，一个专门为 EEG 神经接口设计的基础模型，通过同时捕获 EEG 信号中的同质性和异质性时空特征，实现跨被试、跨任务、跨电极配置的通用表示学习，推动 EEG 基础模型向通用神经解码系统迈进。

## 2. 方法论

### 核心思想
- 使用预训练 Transformer，在时间维度引入振幅感知掩码和渐进式混合专家，在空间维度利用 3D 电极坐标嵌入和脑叶池化，强化模型对 EEG 时空异质性的适应能力。

### 关键技术细节
1. **3D 电极嵌入**  
   - 根据国际 10-20 系统电极的物理坐标 \((x_d, y_d, z_d)\)，对每个坐标使用正弦函数编码，然后拼接得到位置编码：  
     \(PE^{(s)}_d = \text{Concat}\big(PE_x(x_d), PE_y(y_d), PE_z(z_d)\big)\)  
   - 每个 EEG 数据点同时嵌入时间位置（标准 Transformer 正弦编码）和空间位置，得到输入表示 \(s^{(i)}_{t,d}\)。

2. **振幅感知掩码预训练 (AAMP)**  
   - 并非随机掩码连续段，而是基于信号振幅：对每个通道的幅度值排序，以随机百分位为中心选取 \(T \cdot P\) 个点进行掩码（\(P\) 为掩码率）。  
   - 迫使模型学习信号的结构性特征而非局部插值。预训练损失为 ℓp 重构损失 \(L_{\text{AAMP}}\)。

3. **渐进式混合专家 (PMoE)**  
   - 在编码器的深层逐步增加专家子网络数量（例如配置 \([0,0,2,4,4,6]\)），浅层只保留共享专家。  
   - 通过 TopKSoftmax 门控机制路由，并加入辅助损失确保专家负载均衡。  
   - 共享专家捕捉通用模式，渐进专家处理日益特化的信号特征。

4. **脑叶内-脑叶间池化 (IILP)**  
   - 微调阶段首先对时间维度平均池化得到每个通道的嵌入，然后按脑叶分组（额叶、枕叶等）进行颅内平均池化，最后跨脑叶拼接所有叶级嵌入，并堆叠所有编码器层的输出作为最终表示。  
   - 显式利用区域脑活动模式。

5. **骨干网络**  
   - 采用 Crossformer 架构，包含交替的时间注意力（Cross-Time）和空间注意力（Cross-Dimension），使用 Pre-LN 和 SwiGLU 激活。

## 3. 实验设计

### 预训练数据
- 超过 2000 小时的公开 EEG 数据（14 个数据集，如 TUEG、SEED-Series、TUSZ 等），所有下游数据集在预训练中排除。

### 下游任务与数据集（共 8 个）
| 任务类型 | 数据集 | 类别数 | 样本数 |
|---------|--------|-------|-------|
| 精神压力检测 | MentalArithmetic | 2 | 1,707 |
| 精神障碍诊断 | Mumtaz2016 | 2 | 6,963 |
| P300 事件 | PhysioNetP300 | 2 | 21,179 |
| 睡眠分期 | Sleep-EDFx | 5 | 457,652 |
| 情绪识别 | SEED-V | 5 | 115,001 |
| 运动想象 | BCIC-IV-2A | 4 | 5,184 |
| 异常检测 | TUAB | 2 | 409,455 |
| 事件类型分类 | TUEV | 6 | 112,491 |

### 对比方法
- **非基础模型**：EEGNet、EEGConformer、SPaRCNet、ContraWR、CNN-Transformer、FFCL、ST-Transformer  
- **基础模型**：BENDR、BIOT、LaBraM、EEGPT、NeuroLM、CBraMod

### 评估指标
- 二分类：Balanced Accuracy、AUC-PR、AUROC  
- 多分类：Balanced Accuracy、Cohen’s Kappa、Weighted F1

### 公平性保障
- 严格遵循 CBraMod 的预处理流程（重参考、归一化、段长等），使用相同的数据划分。
- 对于未公开结果的基线，直接引用 CBraMod 或 EEGPT 原文数值。

## 4. 资源与算力

- **预训练**：8 块 NVIDIA RTX 4090 GPU，有效 batch size 480，bfloat16 混合精度，约 **30 小时**完成 400K 步训练。
- **微调**：单个 GPU 上耗时从几分钟到几小时不等，取决于数据集大小。
- **模型参数量**：NeurIPT 激活参数约 **73.5M**（介于 LaBraM-Huge 369M 和 CBraMod 4.2M 之间）。

## 5. 实验数量与充分性

- **主实验**：8 个下游数据集上报告 Balanced Accuracy、Cohen’s Kappa / AUC-PR、Weighted F1 / AUROC，并给出标准差（多次运行）。
- **消融实验**：
  - 掩码策略对比（随机 vs. AAMP）及不同掩码率（30%-70%）
  - MoE 策略对比（无 MoE、均匀 MoE、收缩 MoE、渐进 MoE）及不同专家配置
  - 池化策略对比（无池化、均值池化、半球、冠状、矢状、IILP）
  - 位置编码对比（三角函数、1D/2D 可学习、3D PE）
  - 激活函数对比（ReLU、GELU、SwiGLU）
  - 低资源场景（1%、5%、10% 数据量）
  - 各组件逐步组合的消融（表 6）
- **额外分析**：专家参与热力图、注意力分数可视化、通道扰动相关性等。
- **充分性**：实验覆盖 8 种不同 BCI 任务，消融实验全面，对比基线包含最新 SOTA，预处理一致，结果稳定且有误差线，实验设计较为充分和客观。

## 6. 主要结论与发现

1. **SOTA 性能**：NeurIPT 在 8 个下游数据集中 7 个取得最佳结果，尤其在 MentalArithmetic 上 Balanced Accuracy 提升 13.9%，BCIC-IV-2A 提升 3.66%，PhysioP300 提升 2.29%。
2. **掩码策略有效性**：AAMP 相比随机掩码在下游 SVM 分类中提高 5.25%，且在多数数据集上微调结果也更好。
3. **渐进式 MoE 优势**：渐进增加专家（如 [0,0,2,4,4,6]）优于均匀或收缩配置，说明深度层需要更多特化专家。
4. **3D 电极嵌入关键**：尤其对运动想象任务（BCIC-IV-2A）提升显著，因其对空间信息敏感。
5. **IILP 有效**：分层脑叶池化优于全局均值池化和简单分区池化，在癫痫和精神疾病检测等需要区域特征的任务上效果突出。
6. **低资源鲁棒性**：仅用 1% 数据仍能保持 64%-80% 性能，10% 数据可达 80%-90%。

## 7. 优点

- **创新结合**：首次将 3D 电极物理坐标、振幅感知掩码、渐进式 MoE、脑叶池化统一到一个 EEG 基础模型中，针对 EEG 数据的独特性质进行了专门设计。
- **全面验证**：在 8 个涵盖分类、回归、睡眠、情绪、运动想象、临床异常等任务的公开数据集上评估，消融实验覆盖所有关键组件。
- **可迁移性强**：3D 嵌入支持任意电极蒙太奇，无需重新训练或填充；模型可直接适应不同通道数和采样率。
- **开源友好**：提供完整代码和预训练权重，便于复现和进一步研究。
- **实验公平性**：严格遵循已有基准的预处理和数据划分，确保结果可比。

## 8. 不足与局限

- **计算成本较高**：73.5M 激活参数，预训练需 8×4090 运行 30 小时，对资源受限的研究组仍有门槛。
- **部分指标未达最优**：在 TUAB 数据集上 Cohen’s Kappa 和 AUROC 略低于 CBraMod（但 Balanced Accuracy 更高），说明模型在某些任务上仍有提升空间。
- **探索有限**：未考虑脑功能连接等更高级的 EEG 特性；受 GPU 限制未系统研究缩放定律。
- **潜在风险**：模型可能被用于未经授权的认知监控或神经隐私侵犯，需要伦理框架保护。
- **实际部署差距**：尽管性能 SOTA，但与临床级 BCI 系统的最终需求仍有距离，尤其在低误差要求场景下。

（完）
