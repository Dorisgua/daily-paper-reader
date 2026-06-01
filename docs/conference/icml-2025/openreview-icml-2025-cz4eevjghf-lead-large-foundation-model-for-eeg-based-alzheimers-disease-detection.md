---
title: "LEAD: Large Foundation Model for EEG-Based Alzheimer’s Disease Detection"
title_zh: LEAD：基于EEG的阿尔茨海默病检测的大型基础模型
authors: "Yihe Wang, Nan Huang, Nadia Mammone, Marco Cecchi, Xiang Zhang"
date: 2025-01-23
pdf: "https://openreview.net/pdf?id=cz4EevJGHf"
tags: ["query:eeg"]
score: 8.0
evidence: 基于深度学习的大型EEG基础模型用于阿尔茨海默病检测
tldr: 现有EEG阿尔茨海默病检测方法受限于数据集小和跨被试差异。本文构建了包含813名被试的最大EEG-AD数据集，并提出首个大型基础模型LEAD。通过自监督预训练等完整流程，LEAD在多项评估中达到最先进性能。该工作展示了大型预训练模型在EEG信号处理中的应用价值，其方法学可直接服务于EEG表征学习与通道补全等任务。
source: ICML-2025-Rejected-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-cz4eevjghf/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 724, \"height\": 311, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cz4eevjghf/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1696, \"height\": 917, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cz4eevjghf/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1378, \"height\": 1034, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cz4eevjghf/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1766, \"height\": 336, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-cz4eevjghf/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 876, \"height\": 572, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-cz4eevjghf/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1780, \"height\": 600, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-cz4eevjghf/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1778, \"height\": 1148, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-cz4eevjghf/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1423, \"height\": 614, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-cz4eevjghf/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1775, \"height\": 639, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-cz4eevjghf/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1773, \"height\": 586, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-cz4eevjghf/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 891, \"height\": 349, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-cz4eevjghf/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1776, \"height\": 537, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-cz4eevjghf/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1782, \"height\": 560, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-cz4eevjghf/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 893, \"height\": 699, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-cz4eevjghf/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1780, \"height\": 724, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-cz4eevjghf/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 894, \"height\": 420, \"label\": \"Table\"}]"
motivation: EEG阿尔茨海默病检测面临数据集小和跨被试差异大的挑战。
method: 构建大规模EEG-AD数据集，提出基于自监督预训练的大型基础模型LEAD。
result: 在多项评估中取得最先进性能，显著优于现有方法。
conclusion: LEAD证明了大型预训练模型在EEG信号处理中的有效性，为相关研究提供了新基准。
---

## Abstract
Electroencephalogram (EEG) provides a non-invasive, highly accessible, and cost-effective solution for Alzheimer’s Disease (AD) detection. However, existing methods, whether based on manual feature extraction or deep learning, face two major challenges: the lack of large-scale datasets for robust feature learning and evaluation, and poor detection performance due to inter-subject variations. To address these challenges, we curate an EEG-AD corpus containing 813 subjects, which forms the world’s largest EEG-AD dataset to the best of our knowledge. Using this unique dataset, we propose **LEAD**, the first large foundation model for EEG-based AD detection. Our method encompasses an entire pipeline, from data selection and preprocessing to self-supervised contrastive pretraining, fine-tuning, and key setups such as subject-independent evaluation and majority voting for subject-level detection. We pre-train the model on 11 EEG datasets (4 AD and 7 non-AD) and unified fine-tune it on 5 AD datasets. Our self-supervised pretraining design includes sample-level and subject-level contrastive learning to extract useful general EEG features. Fine-tuning is performed on 5 channel-aligned datasets together. The backbone encoder incorporates temporal and channel embeddings to capture features across both temporal and spatial dimensions. Our method demonstrates outstanding AD detection performance, achieving up to a 9.86% increase in F1 score at the sample level and up to a 9.31% improvement at the subject level compared to state-of-the-art methods. The results of our model strongly confirm the effectiveness of subject-level contrastive pretraining and channel-aligned multi-dataset fine-tuning for addressing inter-subject variation. The source code is at \url{https://anonymous.4open.science/r/LEAD-3B51}.

---

## 论文详细总结（自动生成）

# LEAD：基于EEG的阿尔茨海默病检测的大型基础模型——中文总结

## 1. 核心问题与整体含义（研究动机和背景）

阿尔茨海默病（AD）是最常见的神经退行性疾病，影响65岁以上人群的10%-30%。现有检测工具如MRI和PET成本高昂且需要专业临床经验，往往在症状显著后才被检测。脑电图（EEG）提供了一种非侵入性、高可及性、低成本的替代方案，但面临两大挑战：

- **缺乏大规模数据集**：大多数研究仅包含不超过50名受试者，数据量小导致模型泛化能力差。
- **跨受试者变异**：受试者个体特征（年龄、性别等）干扰AD模式识别，导致模型难以泛化到未见过的新受试者。

本文旨在解决上述问题，通过构建世界最大的EEG-AD数据集（813名受试者），并提出首个用于EEG-based AD检测的大型基础模型 **LEAD**，实现对AD的准确检测。

## 2. 方法论

### 核心思想
- 采用自监督对比预训练 + 统一微调的范式。
- 预训练阶段使用11个数据集（4个AD + 7个非AD），包含2,354名受试者、1,165,361个1秒样本。
- 微调阶段在5个高质量AD数据集上统一进行（共615名受试者、223,039个样本）。
- 关键设计：**subject-level对比学习**，将同受试者的样本视为正样本对，不同受试者的样本为负样本对，以学习对受试者特征不敏感的通用AD特征。

### 技术细节
1. **数据预处理**：
   - 通道对齐：将所有数据集对齐到国际10-20系统的19个标准通道（通过插值或选择最近通道）。
   - 频率对齐：重采样至128Hz，滤波0.5-45Hz。
   - 样本分割：1秒间隔，128个时间点。
   - 标准化：每个通道独立做Z-score归一化。

2. **自监督对比预训练**：
   - 采用SimCLR架构，对每个样本应用两种数据增强（如时间翻转、频率掩码、通道掩码等）。
   - **样本级对比损失**：\( L_{\text{Sam}} = \mathbb{E}_{x_i} \left[ -\log \frac{\exp(\text{sim}(z_i^a, z_i^b)/\tau)}{\sum_j \exp(\text{sim}(z_i^a, z_j^b)/\tau)} \right] \)
   - **受试者级对比损失**：\( L_{\text{Sub}} = \mathbb{E}_{x_i} \left[ \mathbb{E}_{x_k \in \text{same subject}} \left[ -\log \frac{\exp(\text{sim}(z_i^a, z_k^b)/\tau)}{\sum_j \exp(\text{sim}(z_i^a, z_j^b)/\tau)} \right] \right] \)
   - 总损失：\( L = \lambda_1 L_{\text{Sam}} + \lambda_2 L_{\text{Sub}} \)，其中\(\lambda_1 = \lambda_2 = 0.5\)。
   - 采用**索引洗牌算法**确保同一批次中包含来自同一受试者的多个样本。

3. **骨干编码器架构**：
   - 采用简化版ADformer，包含**时间分支**和**空间分支**并行处理。
   - 时间分支：将跨通道的连续时间块（patch）线性映射为token，加位置编码后通过Transformer。
   - 空间分支：对原始数据加通道位置编码，经1D卷积升维后映射为通道token，再通过Transformer。
   - 最终表示：拼接两个分支的最后一个token。
   - 预训练时使用投影头（2层FC）得到密集表示；微调时丢弃投影头，添加线性分类器。

4. **受试者独立评估与多数投票**：
   - 按受试者划分训练/验证/测试集，确保同一受试者仅出现在一个集合中。
   - 受试者级分类：对某受试者的所有样本进行多数投票，确定最终标签。

## 3. 实验设计

### 数据集
- **预训练**：11个数据集，包括4个AD（AD-Auditory、ADFSU、ADSZ、APAVA）和7个非AD（Depression、PEARL-Neuro、REEG-BACA、REEG-PD、REEG-SRM、TDBrain、TUEP）；共2,354名受试者，1,165,361个样本。
- **微调/评估**：5个AD数据集（ADFTD、BrainLat、CNBPM、Cognision-ERP、Cognision-rsEEG）；共615名受试者，223,039个样本；均为二分类（AD vs 健康对照）。

### 基准方法
- 5种全监督方法：TCN、Transformer、Conformer、TimesNet、Medformer（在单一数据集上训练，使用原始通道数）。
- 3种自监督方法：TS2Vec、BIOT、EEG2Rep（预训练+统一微调）。
- 2种大型EEG基础模型：LaBraM、EEGPT（加载预训练模型后在AD数据集上微调）。
- 作者方法三个变体：
  - LEAD-Vanilla：单数据集全监督（原始通道）。
  - LEAD-Sup：统一全监督（5个AD数据集联合训练，通道对齐）。
  - LEAD-Base：自监督预训练（11个数据集）+ 统一微调（5个AD数据集）。

### 评估指标
- 样本级：准确率、宏平均F1。
- 受试者级：经过多数投票后的准确率、宏平均F1。

## 4. 资源与算力

文中明确说明：
- 实验在**NVIDIA RTX 4090 GPU**和配备**4个RTX A5000 GPU**的服务器上进行。
- 软件环境：Python 3.8，PyTorch 2.0.0 + cu118。
- 预训练固定50个epoch，全监督/微调最多100个epoch（早停patience=15）。
- 未给出具体训练时长（小时），但提及批大小：预训练512，微调128。

## 5. 实验数量与充分性

本文实验较为充分，包含：
- **主实验**：在5个AD数据集上对比10个baseline（全监督、自监督、大型基础模型）及作者3个变体，报告样本级和受试者级指标，每个实验使用5个随机种子（41-45）计算均值和标准差。
- **消融实验**：
  - 非AD数据集数量影响（5→7→9→11个预训练数据集）。
  - AD数据集数量影响（在ADFTD上逐步增加训练数据）。
  - 对比学习模块（仅样本级、仅受试者级、两者结合）。
  - 单数据集微调 vs 统一微调 vs 单数据集验证。
  - 仅公开数据集训练（ADFTD和BrainLat）。
- **补充实验**：
  - 不同频段分析（δ、θ、α、β、γ）。
  - 通道重要性分析（在CNBPM上掩码不同脑区）。
- 实验设计客观：受试者独立划分、统一微调、多数据集验证，避免了数据泄露。但部分消融实验仅针对特定数据集（如CNBPM），且未对所有数据集进行同等深度的分析。

总体来看，实验数量充足，对比方法全面，消融实验设计合理，结果可重复性强（代码开源）。

## 6. 主要结论与发现

- LEAD-Base（自监督预训练+统一微调）在5个AD数据集上达到最佳性能，受试者级F1分别达91.34%、89.98%、100.00%、84.42%、91.86%，最高比SOTA提升9.31%。
- **受试者级对比学习**显著优于样本级对比学习，证明subject-level预训练能有效减少跨受试者变异干扰。
- **通道对齐+统一微调**使模型能联合多个数据集训练，性能优于单数据集训练。
- 非AD数据集的加入持续提升AD检测性能（尤其对原本通道少的Cognision数据集）。
- Gamma频段对BrainLat受试者级分类最重要，Theta/Alpha/Beta频段对多数数据集关键；额叶区域对CNBPM分类最重要。
- 多数投票显著提升受试者级性能，且对样本数平衡的数据集改善更明显。

## 7. 优点

- **数据规模**：构建了目前最大的EEG-AD数据集（813受试者），并整合11个数据集进行预训练，打破了“各自为政”的数据孤岛。
- **方法创新**：首次将subject-level对比学习引入EEG AD检测，有效缓解跨受试者变异问题；通道对齐策略解决了多数据集异构问题，使统一微调成为可能。
- **实验严谨**：采用受试者独立评估，避免数据泄漏；统一微调联合所有下游任务，选择全局最优模型，而非为每个数据集独立调参。
- **可复现性**：开源代码和模型权重的做法极大促进了社区后续研究。
- **可解释性**：提供了频段分析和通道重要性分析，增强了模型在医疗场景中的可信度。

## 8. 不足与局限

- **通道对齐的信息损失**：为统一训练，将高密度EEG（如128通道）强行对齐到19通道，可能丢弃了部分有用空间信息。作者承认这一点但认为损失可接受。
- **ADFTD数据集表现异常**：LEAD-Base在ADFTD上的受试者级F1（79.96%）低于LEAD-Sup（91.34%），且预训练反倒造成下降，作者未能给出充分解释。
- **实验覆盖不均匀**：部分消融实验（如通道重要性）仅针对CNBPM数据集，结论的泛化性存疑；未对所有5个下游数据集进行相同深度的分析。
- **频段分析欠缺统计检验**：不同频段性能差异是否显著未报告置信区间或统计检验。
- **计算资源消耗**：预训练需使用4个A5000 GPU，对普通研究团队可能成本较高；但作者未给出具体训练时长。
- **应用限制**：仅针对AD vs 健康对照的二分类，未扩展到MCI或其他痴呆亚型；多数投票依赖受试者样本数，样本不均衡时效果可能打折扣。

（完）
