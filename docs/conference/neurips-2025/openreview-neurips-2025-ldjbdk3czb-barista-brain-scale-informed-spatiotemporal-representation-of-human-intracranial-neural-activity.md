---
title: "BaRISTA: Brain Scale Informed Spatiotemporal Representation of Human Intracranial Neural Activity"
title_zh: BaRISTA：基于脑尺度信息的人类颅内神经活动时空表征
authors: "Lucine L Oganesian, Saba Hashemi, Maryam M. Shanechi"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=LDjBDk3Czb"
tags: ["query:eeg-latent"]
score: 4.0
evidence: 脑活动时空表征学习
tldr: 颅内记录具有复杂时空交互，现有模型在空间编码和自监督任务设计上存在挑战。本文提出BaRISTA，一种基于脑尺度信息的时空表征模型，针对不同空间尺度设计编码策略并创新自监督任务。实验证明该方法能有效学习脑网络模式，提升下游解码性能，为脑活动表征提供了新思路。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-ldjbdk3czb/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1433, \"height\": 491, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ldjbdk3czb/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1429, \"height\": 564, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ldjbdk3czb/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1455, \"height\": 816, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ldjbdk3czb/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1347, \"height\": 674, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ldjbdk3czb/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1316, \"height\": 458, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ldjbdk3czb/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1318, \"height\": 717, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ldjbdk3czb/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1284, \"height\": 677, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ldjbdk3czb/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1452, \"height\": 603, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ldjbdk3czb/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1311, \"height\": 631, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-ldjbdk3czb/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1196, \"height\": 306, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ldjbdk3czb/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1358, \"height\": 357, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ldjbdk3czb/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1243, \"height\": 169, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ldjbdk3czb/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1270, \"height\": 1289, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ldjbdk3czb/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1357, \"height\": 425, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ldjbdk3czb/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1344, \"height\": 252, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ldjbdk3czb/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1420, \"height\": 490, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ldjbdk3czb/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1074, \"height\": 485, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ldjbdk3czb/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1355, \"height\": 356, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ldjbdk3czb/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1333, \"height\": 442, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ldjbdk3czb/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1332, \"height\": 408, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ldjbdk3czb/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1446, \"height\": 455, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ldjbdk3czb/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1204, \"height\": 213, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ldjbdk3czb/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1277, \"height\": 213, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ldjbdk3czb/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1109, \"height\": 173, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ldjbdk3czb/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1371, \"height\": 608, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ldjbdk3czb/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1438, \"height\": 306, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ldjbdk3czb/table-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 937, \"height\": 467, \"label\": \"Table\"}]"
motivation: 颅内记录存在复杂时空交互，现有模型在空间编码和自监督任务设计上不足。
method: 提出脑尺度信息引导的时空表征模型，创新自监督任务。
result: 有效学习脑网络模式，提升下游解码性能。
conclusion: 考虑脑尺度信息能显著提升颅内神经活动表征质量。
---

## Abstract
Intracranial recordings have opened a unique opportunity to simultaneously measure activity across multiregional networks in the human brain. Recent works have focused on developing transformer-based neurofoundation models of such recordings that can generalize across subjects and datasets. However, these recordings exhibit highly complex spatiotemporal interactions across diverse spatial scales, from the single-channel scale to the scale of brain regions. As such, there remain critical open questions regarding how best to encode spatial information and how to design self-supervision tasks that enable the learning of brain network patterns and enhance downstream decoding performance using such high-dimensional, multiregional recordings. To allow for exploring these questions, we propose a new spatiotemporal transformer model of multiregional neural activity and a corresponding self-supervised masked latent reconstruction task, designed to enable flexibility in the spatial scale used for token encoding and masking. Applying this model on publicly available multiregional intracranial electrophysiology (iEEG) data, we demonstrate that adjusting the spatial scale for both token encoding and masked reconstruction significantly impacts downstream decoding. Further, we find that spatial encoding at larger scales than channel-level encoding, which is commonly used in existing iEEG transformer models, improves downstream decoding performance. Finally, we demonstrate that our method allows for region-level token encoding while also maintaining accurate channel-level neural reconstruction. Taken together, our modeling framework enables exploration of the spatial scales used for token encoding and masking, reveals their importance towards self-supervised pretraining of neurofoundation models of multiregional human brain activity, and enhances downstream decoding performance.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义

- **研究动机**：颅内脑电图（iEEG）能够同时记录多个脑区的高维神经活动，具有复杂的时空交互。然而，现有的Transformer模型在空间信息编码上通常只使用通道级（single-channel）尺度，自监督预训练任务（如掩码重建）也仅在通道级别进行掩码，缺乏对更大空间尺度（如脑区、脑叶）的探索。
- **整体含义**：本文提出**BaRISTA**框架，旨在灵活选择token编码和掩码重建的空间尺度，系统研究空间尺度对表征学习和下游解码性能的影响。研究发现，采用比通道级更大的空间尺度（如脑区图谱、脑叶）进行编码，能显著提升下游任务性能，并且即使使用区域级编码也能保持通道级的重建精度。这为构建更有效的颅内神经活动基础模型提供了关键设计原则。

### 2. 方法论

- **核心思想**：将iEEG信号的时间序列通过tokenizer编码为token，然后根据可配置的空间尺度（通道坐标、图谱分区、脑叶）添加可学习的空间嵌入，形成时空交织的token序列，输入Transformer编码器。预训练采用**空间掩码潜在重建任务**——根据空间元信息选择某些空间类别的所有token作为目标进行掩码，训练模型从剩余观察token重建被掩码token的潜在表示。
- **关键技术细节**：
  - **tokenizer**：使用共享的**扩张卷积CNN**作为时间编码器，将每个通道的时间序列分割成固定长度的补丁（patches），然后通过线性投影得到维度为d的token。
  - **空间编码**：根据三种尺度（通道级LPI坐标、图谱分区、脑叶）为每个通道添加**可学习的空间嵌入**；对于多维坐标（如LPI），使用每个维度的嵌入向量求和。
  - **模型架构**：将各通道的token按时间-空间交织排列，形成输入序列（一个时间步所有通道的token依次排列，然后是下一时间步）。使用**旋转位置编码（RoPE）**嵌入时间信息。Transformer编码器为12层、4头、隐藏维度64。
  - **预训练任务**：
    - 随机选择目标空间类别，其所有token视为目标。
    - 观察token由在线tokenizer编码，目标token由目标tokenizer（通过EMA更新）编码。
    - 目标token被替换为共享的可学习掩码token，添加空间嵌入后输入Transformer。
    - 使用预测网络（MLP）从掩码token的嵌入重建目标token，损失为MSE。
    - 训练后使用EMA更新后的tokenizer和Transformer骨干进行下游任务。
- **公式/算法流程**（文字说明）：
  1. 对每个时间补丁 \(P_{ij}\)，通过tokenizer \(F\) 得到初始token \(B_{ij}\)。
  2. 根据空间尺度获取空间类别 \(sp(j)\) 对应的嵌入 \(E_j\)，得到空间编码token \(S_{ij} = B_{ij} + E_j\)。
  3. 将所有token按时间-空间交织排序组成序列 \(S\)。
  4. 在线分支（学生）中，目标空间类别的token替换为掩码token \(M\)（加上其空间嵌入），其他token保持不变，形成 \(S_{\text{masked}}\)。
  5. \(S_{\text{masked}}\) 通过Transformer编码器 \(G\) 得到嵌入，对掩码token的嵌入通过预测网络 \(H\) 预测重建token \(\hat{B}_{ij}\)。
  6. 目标token由目标tokenizer \(\tilde{F}\) 产生（停止梯度）。
  7. 计算预测token与目标token之间的平均MSE损失。

### 3. 实验设计

- **数据集**：使用公开的**Brain Treebank**数据集，包含10名癫痫病人共26次会话的iEEG记录（2048 Hz采样率），受试者观看好莱坞电影，提供电影字幕和语音标签。
- **预处理**：去除噪声通道，进行拉普拉斯参考，剔除脑室通道；将数据分割为3秒非重叠片段，z-score标准化；每个片段生成12个时间补丁（每个250ms）。
- **下游任务**：两类语言相关分类任务——**语句起始检测**（句子开头 vs. 无语音）和**语音/非语音分类**；另外还有**掩码通道重建**任务（重构原始时间序列）。
- **基准方法**：
  - **Brant**（Zhang et al., 2023）：现有SOTA iEEG Transformer基础模型。
  - **PopT+Brainbert**（Chau et al., 2025）：另一SOTA模型，使用通道级空间编码和脑区替换检测预训练。
  - **随机初始化的BaRISTA**：验证预训练有效性。
- **评估指标**：分类任务使用ROC-AUC，重建任务使用MSE和R²。报告平均值±标准误（s.e.m.），统计显著性使用Wilcoxon符号秩检验和双因素ANOVA。
- **训练/测试划分**：17个会话预训练，2个验证，7个测试（每个测试会话独立微调评估）。另设**不可见受试者**留出实验和数据量缩放实验。
- **实验数量与充分性**：
  - 主实验（表1、表2）涵盖9种空间编码/掩码组合，每个组合用1个预训练种子+5个微调种子，共35个数据点（每个测试会话7×5）。
  - 补充实验（附录F）用3个预训练种子进行稳健性验证。
  - 额外评估：使用**时间顺序交叉验证**（5折）进一步验证结果一致性（附录K），增加音量分类和光流分类任务。
  - 消融研究：不同时间编码器选择（附录J.1）、分离注意力与交织注意力（附录J.2）。
  - 可解释性分析（附录G）：可视化线性分类器权重映射到脑区。
  - 总体而言，实验设计全面、比较公平，统计检验充分，结论稳健。

### 4. 资源与算力

- **模型大小**：BaRISTA约**1M参数**；PopT约20M；Brant约500M。
- **训练硬件**：BaRISTA预训练使用**4块NVIDIA RTX 6000 Ada或4块RTX A6000 GPU**，训练时间**<4小时**（70 epochs，19500 update steps）。
- **对比模型**：
  - PopT：4块RTX A6000，22小时（500k steps）。
  - Brant：4块Tesla A100，2.8天（750k steps）。
- 下游微调使用相同GPU配置，每个任务约30 epochs。

### 5. 实验数量与充分性

- **数量充分**：包含9种空间尺度组合的主实验、3个预训练种子的重复验证、5折时间交叉验证、跨受试者鲁棒性测试、数据量缩放实验（5%~100%）、消融实验、重建实验、频谱分析、可解释性分析。统计检验（Wilcoxon, ANOVA）验证了差异显著性。
- **客观与公平**：
  - 与SOTA模型（Brant, PopT）在相同数据集、相同任务上进行公平比较，并复现了他们的结果（附录E.1）。
  - 控制种子、拆分方式，报告均值和标准误。
  - 基线模型的超参数尽量与原论文一致，并且进行了充分微调（比BaRISTA更多epochs）。
- **潜在偏差**：实验仅在一个数据集（Brain Treebank）上进行，任务局限于语言相关分类和重建，缺乏跨数据集和更广泛认知任务的验证。

### 6. 主要结论与发现

- **空间编码尺度比掩码尺度更重要**：增大空间编码尺度（从通道级到图谱或脑叶级）能显著提升下游分类性能，而掩码尺度的影响相对较小，且几乎无交互效应。
- **最优配置**：使用**图谱级（parcels）编码+通道级（channels）掩码**获得最佳性能（两个语言任务AUC分别达0.862和0.869），显著优于Brant和PopT。
- **通道级重建能力保持**：即使使用区域级编码，模型仍能准确重建单个通道的时间序列，重建性能与通道级编码模型相当。
- **泛化与缩放**：模型对未曾见过的受试者仍有较好性能（AUC ~0.84），且下游性能随预训练数据量增加而提升（图5）。
- **可解释性**：线性分类器权重集中在语言相关脑区（如听觉皮层、Wernicke区、左额中回），表明模型学到了生物学上合理的表征。
- **消融结果**：扩张CNN优于线性投影或简单卷积；交织的时空注意力优于分离的时空注意力。

### 7. 优点

- **创新性**：首次在iEEG建模中系统探索并解耦空间编码和掩码的不同尺度，揭示了空间尺度对于表征学习的重要性。
- **灵活性与效率**：框架允许用户根据先验知识灵活指定空间类别（通道、图谱、脑叶），且模型参数极少（1M），训练速度快，性能却超过更大模型。
- **全面实验**：包括统计检验、跨受试者泛化、数据量缩放、消融、可解释性分析，结论稳健可靠。
- **实用性**：支持不同会话的不同通道数和时间补丁数（变长输入），易于扩展到新数据集。

### 8. 不足与局限

- **空间尺度的定义局限**：本文仅基于解剖分区（Destrieux图谱、脑叶），未探索功能定义（如任务相关的功能网络）或数据驱动的分区，这可能是未来改进方向。
- **仅使用空间掩码**：未结合时间维度的掩码（如时空联合掩码），可能限制学习更丰富的时空表征。
- **时间编码器选择**：虽然CNN在本任务中表现良好，但或许有更优的时间编码方案（如多尺度卷积、金字塔池化）未被充分探索。
- **数据集和任务单一**：仅在Brain Treebank一个数据集上验证，任务局限于语言相关分类和重建，未能展示在更广泛的认知任务（如运动、情绪、记忆）上的通用性。
- **高频重建性能差**：频谱分析表明模型在低频频段重建较好，高频（>40Hz）重建误差大（NMSE>1），可能丢失重要神经动力学信息。
- **与最新模型比较缺失**：未与同期更新的模型（如Brant-2, Zheng et al. 2024的Du-IN）进行对比。
- **计算资源细节有限**：未报告更细的功耗或总成本。

（完）
