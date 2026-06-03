---
title: "THD-BAR: Topology Hierarchical Derived Brain Autoregressive Modeling for EEG Generic Representations"
title_zh: THD-BAR：用于EEG通用表示的拓扑层次化脑自回归建模
authors: "Wenchao Yang, Weidong Yan, Wenkang Liu, Yulan Ma, Yang Li"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=6Q5WG84uOD"
tags: ["query:eeg-latent"]
score: 8.0
evidence: 提出自回归建模学习EEG通用表示，涉及潜在空间表征
tldr: 现有EEG预训练模型主要依赖简单时序建模，忽略了信号的生理特性和动态空间拓扑。本文提出THD-BAR，一种拓扑层次化自回归建模方法，通过分层建模多通道EEG的拓扑结构来学习通用表示。实验表明该方法在多个下游任务上优于基线，为EEG表示学习提供了新范式。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-6q5wg84uod/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1439, \"height\": 411, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-6q5wg84uod/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1447, \"height\": 303, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-6q5wg84uod/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1295, \"height\": 556, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-6q5wg84uod/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1436, \"height\": 652, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-6q5wg84uod/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1434, \"height\": 739, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-6q5wg84uod/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 581, \"height\": 634, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-6q5wg84uod/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1445, \"height\": 646, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-6q5wg84uod/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1458, \"height\": 535, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-6q5wg84uod/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1454, \"height\": 326, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-6q5wg84uod/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1382, \"height\": 983, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-6q5wg84uod/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1390, \"height\": 1134, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-6q5wg84uod/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1272, \"height\": 480, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-6q5wg84uod/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1330, \"height\": 473, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-6q5wg84uod/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1312, \"height\": 453, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-6q5wg84uod/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 688, \"height\": 1084, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-6q5wg84uod/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1370, \"height\": 785, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-6q5wg84uod/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 846, \"height\": 531, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-6q5wg84uod/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1445, \"height\": 1092, \"label\": \"Table\"}]"
motivation: 现有自回归框架未能充分捕获EEG信号的生理特性和动态空间拓扑。
method: 提出拓扑层次化自回归建模，分层学习多通道EEG的拓扑结构。
result: 在多个EEG下游任务上取得优于基线的表现，验证了通用表示的有效性。
conclusion: THD-BAR为大规模EEG自监督表示学习提供了新的拓扑感知框架。
---

## Abstract
Large-scale pre-trained models hold significant potential for learning universal EEG representations. However, most existing methods, particularly autoregressive (AR) frameworks, primarily rely on straightforward temporal sequencing of multi-channel EEG data, which fails to capture the rich physiological characteristics inherent to EEG signals. Moreover, their time-centered modeling approach also limits the effective representation of the dynamic spatial topology of brain activity. To address these challenges and fully exploit the potential of large-scale EEG models, we propose a novel Topology Hierarchical Derived Brain Autoregressive Modeling (THD-BAR) for EEG generic representations. The core innovation of THD-BAR lies in the introduction of the Brain Topology Hierarchy (BTH), which establishes a multi-scale spatial order for EEG channels. This hierarchical structure enables a redefinition of autoregressive learning as a "next-scale-time prediction" problem, effectively capturing both spatial and temporal dynamics. Based on BTH, we design a Topology-Hierarchical Vector Quantized-Variational Autoencoder (THVQ-VAE) for multi-scale tokenization and develop an enhanced Brain Autoregressive (BAR) module with specialized masking strategies for prediction. Through extensive large-scale pre-training on 17 datasets, followed by rigorous validation on 10 downstream datasets spanning 5 distinct tasks, THD-BAR consistently outperforms existing methods. These results highlight the superior generalization and modeling capabilities of our proposed approach.

---

## 论文详细总结（自动生成）

# THD-BAR: 用于EEG通用表示的拓扑层次派生脑自回归建模 —— 论文详细总结

## 一、核心问题与整体含义（研究动机和背景）

**1. 研究动机：**
- 近年来，大规模预训练模型在脑电（EEG）分析中展现出巨大潜力，尤其是自回归（AR）框架（如基于 GPT 的模型）。
- 然而，现有 AR 方法主要采用**简单的时间序列排列**方式，将多通道 EEG 视为一维时序，进行 "下一个时间步预测"。这种方式忽略了 EEG 信号固有的丰富生理特性，尤其是**脑活动的动态空间拓扑结构**——不同的认知任务会引发不同的空间激活模式，而纯时间序列无法有效捕捉这些空间变化。
- 因此，核心问题：**如何为 EEG 数据定义合理的空间顺序，从而在自回归建模中同时建模空间和时间的依赖关系？**

**2. 整体含义：**
- 本文提出 THD-BAR 框架，通过引入**脑拓扑层次（Brain Topology Hierarchy, BTH）**，将自回归学习重新定义为 "下一个尺度-时间预测"（next‑scale‑time prediction），从而同时捕获 EEG 信号的多尺度空间动态和时间动态，旨在学习更通用的 EEG 表示，提升跨任务、跨数据集的泛化能力。

## 二、方法论：核心思想、关键技术细节与流程

**1. 核心思想：**
- 基于生理结构建立多尺度空间顺序（BTH），将 EEG 建模从 "下一个时间点预测" 扩展为 "下一个尺度-时间预测"——即在每个时间步内，模型需要按尺度从粗到细（全脑→脑区→通道）预测空间令牌，同时跨时间步进行因果建模。

**2. 关键技术细节（三阶段流程）：**

- **阶段一：神经分词器训练（THVQ-VAE）**
  - 对原始 EEG 信号进行分片（patch），输入 VQ‑VAE 框架。
  - 创新点：引入**拓扑层次向量量化（THVQ）**——在下采样和上采样过程中，根据 BTH 的多尺度通道分组（S1~S5），在编码端逐步聚合特征（粗→细），解码端逐步分发特征（细→粗）。
  - 共享码本（codebook），生成多尺度离散令牌图（r1, r2, ..., rS）。
  - 联合优化时域重建损失、频域重建损失以及域分类损失（区分 EEG 与文本模态）。

- **阶段二：脑自回归预训练（BAR）**
  - 使用前一步冻结的 THVQ-VAE 将 EEG 信号转化为多尺度令牌序列。
  - 定义**尺度-时间因果掩码（scale‑time‑wise mask）**：每个令牌只能关注之前时间步的所有令牌，以及当前时间步中更粗尺度的令牌。
  - 采用 GPT-2 系列架构（124M / 354M / 1555M 参数），优化交叉熵损失，学习条件概率 P(r_s^t | prefix)。

- **阶段三：多任务指令微调**
  - 结合 EEG 与文本指令（如情感分类问题），用 [SEP] 分隔，基于答案部分计算损失，实现多任务分类。

## 三、实验设计

**1. 使用的数据集：**
- **预训练集**：17 个公开 EEG 数据集（包括 SEED 系列、TUH 系列、DEAP 等），涵盖情感、运动想象、睡眠、癫痫等多种任务。
- **下游任务评估集**：10 个数据集，分属 5 类任务：
  - 情感识别：DEAP、SEED
  - 运动想象：MIBCI、BCIC4‑1
  - 脑力负荷：EEGMat、STEW
  - 睡眠阶段：EDF、HMC
  - 癫痫检测：TUAB、TUEV

**2. Benchmark 与对比方法：**
- 单任务模型：EEGNet、TSception、LGGNet
- 通用预训练模型：BIOT、LaBraM、EEGPT、NeuroLM
- 所有方法在相同下游任务上对比 **平衡准确率（Balanced Accuracy）**。

**3. 对比方式：**
- 表中列出各方法的模型参数、是否通用/多任务，并在 10 个数据集上逐一报告性能，取均值±标准差。

## 四、资源与算力

- **硬件**：8 块 NVIDIA L40s‑48G GPU。
- **软件**：Python 3.12.9, PyTorch 2.5.0, CUDA 12.2。
- **训练时长**：文中未明确给出总时长或 epoch 耗时，但给出了预训练 epoch 数（20）、tokenizer 训练 epoch 数（50）等超参数，未报告具体天数或小时数。

## 五、实验数量与充分性

**1. 实验数量：**
- **预训练**：在 17 个数据集上进行大规模预训练。
- **主实验**：在 10 个下游数据集上对比 9 种基线方法（含 3 种模型尺寸的 THD-BAR）。
- **消融实验**：
  - 多尺度消融（9 种尺度组合 O1‑O9）
  - 掩码设计消融（3 种掩码策略：尺度掩码、时间掩码、尺度-时间掩码）
- **可视化分析**：包括 tokenizer 训练损失曲线、BAR 预训练损失/准确率、时空重建热图定性比较等。

**2. 充分性与公平性：**
- 覆盖了情感、运动想象、脑力负荷、睡眠、癫痫五大类主流 EEG 任务，具有代表性。
- 与多个主流单任务/通用基线对比，基线结果来自原论文或复现，采用相同评估指标。
- 不同模型尺寸（Base/Large/Huge）均参与对比，结论一致。
- 消融实验系统性地验证了多尺度设计和掩码策略的必要性。
- 可视化展示了 THVQ-VAE 相比 VQ-VAE 在时空重建质量上的优势。
- **评价**：实验设计较为充分，对比公平，结论可信。

## 六、主要结论与发现

1. THD-BAR 在 9/10 个下游数据集上取得最优性能，尤其比强大的 NeuroLM 基线提升显著（如 DEAP 上 +2.2%，SEED 上 +3.3%），证明多尺度空间建模优于纯时间预测。
2. 随着模型参数增大（Base→Large→Huge），性能总体提升，说明更大的容量能更有效捕获层次化依赖。
3. 多尺度令牌（O5：S1~S5 全尺度）相比单尺度或部分尺度组合，在 tokenizer 重建质量和 BAR 预训练/微调准确率上均为最优。
4. 尺度-时间联合掩码策略优于单独的尺度掩码或时间掩码，验证了空间与时间依赖联合建模的有效性。
5. THVQ-VAE 在重构 PCC 上比标准 VQ-VAE 提升超过 8%，且能更忠实地还原时空演化的脑活动热图。

## 七、优点

1. **方法创新性**：首次将层次化空间拓扑引入 EEG 自回归建模，提出 BTH 和 "next‑scale‑time prediction" 范式，超越了单纯时间建模。
2. **设计完整性**：从拓扑结构定义、多尺度向量量化分词器、到因果掩码预训练及微调，形成完整框架，代码已开源。
3. **实验全面性**：在 27 个数据集（17 预训练 + 10 评估）上进行充分验证，涵盖主要 EEG 应用，消融实验证明各组件必要性。
4. **可视化有力**：通过时空热图对比直观展示了 THVQ-VAE 在捕获动态空间拓扑方面的优势。
5. **泛化能力**：在多个差异较大的任务上一致超越专用和通用基线，表明学习到的表示具有良好通用性。

## 八、不足与局限

1. **多模态融合有限**：当前模态融合主要服务于指令微调，与文本的结合较为浅层，未深入融合其他生理信号（如 fMRI、fNIRS）或行为数据。
2. **部署效率未充分讨论**：模型参数量较大（最大 1.5B），实时 BCI 场景可能需要模型压缩或轻量化变体，文中仅提及未来工作。
3. **尺度定义可优化**：当前 BTH 基于先验的电极位置和区域划分，未探索数据驱动的自适应尺度聚类，未来可对比多种划分方法。
4. **计算资源报告不完整**：未给出完整预训练耗时（如 GPU 小时数），复现成本难以精确估算。
5. **仅验证分类任务**：方法在分类下游表现优异，但未验证生成、去噪、异常检测等更广泛的 EEG 应用，通用性论证可进一步扩展。
6. **性能波动与异常点**：在 STEW 数据集上略逊于 EEGPT，作者解释为 EEGPT 在 STEW 上同时预训练和微调，但说明本方法在某些特定设置下可能对训练数据产生依赖。

（完）
