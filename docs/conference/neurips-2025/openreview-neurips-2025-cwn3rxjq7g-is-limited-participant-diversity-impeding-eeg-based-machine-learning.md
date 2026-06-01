---
title: Is Limited Participant Diversity Impeding EEG-based Machine Learning?
title_zh: 有限的参与者多样性是否阻碍了基于EEG的机器学习？
authors: "Philipp Bomatter, Henry Gouk"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=cWn3RXJQ7G"
tags: ["query:eeg"]
score: 4.0
evidence: 探究影响基于EEG的机器学习性能的因素
tldr: 基于EEG的机器学习模型泛化性依赖于训练数据的多样性和规模。本文将EEG数据生成视为多层级过程，通过大规模实验研究样本量和参与者多样性对性能的影响。发现增加参与者多样性比单纯增加分段数更有效，为EEG数据收集和模型评估提供了重要指导。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-cwn3rxjq7g/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1288, \"height\": 384, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-cwn3rxjq7g/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1327, \"height\": 387, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-cwn3rxjq7g/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1315, \"height\": 567, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-cwn3rxjq7g/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1323, \"height\": 352, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-cwn3rxjq7g/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1307, \"height\": 517, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-cwn3rxjq7g/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 972, \"height\": 471, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-cwn3rxjq7g/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 992, \"height\": 575, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-cwn3rxjq7g/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1408, \"height\": 598, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-cwn3rxjq7g/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1425, \"height\": 613, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-cwn3rxjq7g/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1414, \"height\": 647, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-cwn3rxjq7g/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1420, \"height\": 484, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-cwn3rxjq7g/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1463, \"height\": 399, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-cwn3rxjq7g/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 720, \"height\": 209, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-cwn3rxjq7g/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1351, \"height\": 501, \"label\": \"Table\"}]"
motivation: EEG机器学习模型的泛化性受训练数据多样性和规模影响，但两者作用尚未厘清。
method: 将EEG数据生成建模为多层过程，通过大规模实验分析样本量和参与者多样性的缩放行为。
result: 增加参与者多样性比增加分段数更有效提升模型鲁棒性。
conclusion: 为EEG数据收集策略和模型评估提供了实证依据。
---

## Abstract
The application of machine learning (ML) to electroencephalography (EEG) has great potential to advance both neuroscientific research and clinical applications. However, the generalisability and robustness of EEG-based ML models often hinge on the amount and diversity of training data. It is common practice to split EEG recordings into small segments, thereby increasing the number of samples substantially compared to the number of individual recordings or participants. We conceptualise this as a multi-level data generation process and investigate the scaling behaviour of model performance with respect to the overall sample size and the participant diversity through large-scale empirical studies. We then use the same framework to investigate the effectiveness of different ML strategies designed to address limited data problems: data augmentations and self-supervised learning. Our findings show that model performance scaling can be severely constrained by participant distribution shifts and provide actionable guidance for data collection and ML research. The code for our experiments is publicly available online.

---

## 论文详细总结（自动生成）

# 中文详细总结

## 一、论文的核心问题与整体含义（研究动机和背景）
- **核心问题**：基于脑电图（EEG）的机器学习模型在临床诊断、睡眠分期等应用中，需要泛化到未见过的被试者。然而，当前EEG数据集通常被试者数量有限（许多研究少于13人），而常用做法是将长时记录分割成短片段来增加样本量。这导致模型性能可能受到**被试者多样性不足**的严重制约，但该问题尚未被系统研究。
- **研究动机**：厘清**整体样本量（片段数）** 与**被试者多样性（被试者数）** 对模型泛化性能的独立影响，并评估现有数据增强和自监督预训练策略在缓解数据限制方面的有效性。
- **整体含义**：为EEG数据收集策略提供实证指导，推动开发能更好应对被试者分布漂移的机器学习方法。

## 二、方法论：核心思想、关键技术细节
- **核心思想**：将EEG数据生成过程建模为**两层层级结构**——从人群分布中抽取被试者，每个被试者再产生多个样本片段。基于统计学习理论，在存在显著被试者分布漂移时，泛化误差主要受**被试者数（n）** 而非总样本数（n×m）控制。
- **关键技术细节**：
  - 对三个大规模EEG数据集（TUAB、CAUEEG、PhysioNet）进行系统子采样，分别控制**被试者数**（从5到1600不等）和**每被试者片段数**（从5到640不等），形成网格状实验设计（图1B）。
  - 使用三种不同架构的模型：**TCN**（时序卷积网络）、**mAtt**（流形注意力网络）、**LaBraM**（大型脑电图基础模型）。
  - 评估三种数据增强：**AmplitudeScaling**（幅度缩放）、**FrequencyShift**（频率偏移）、**PhaseRandomisation**（相位随机化），以及**自监督预训练**（LaBraM在16个数据集上预训练后微调）。
  - 使用早停法防止过拟合，重复多次实验（不同随机种子）以获得不确定性估计。

## 三、实验设计
- **数据集与任务**：
  - **TUAB**（Temple University Hospital Abnormal EEG Corpus）：EEG正常性预测（二分类），>2300被试，15-25分钟记录。
  - **CAUEEG**（Chung-Ang University Hospital EEG）：痴呆诊断（正常/轻度认知障碍/痴呆三分类），1379被试。
  - **PhysioNet**（2018挑战赛数据）：睡眠分期（多类），PSG记录，仅使用6个EEG通道。
- **基准方法**：各模型从零训练（不使用时增强/预训练）。
- **对比方法**：
  - 三种数据增强（单独应用）。
  - 自监督预训练（LaBraM预训练权重微调）。
- **评价指标**：**准确率**（对于TUAB和CAUEEG先对被试者投票聚合，再计算平均准确率；PhysioNet直接使用片段级准确率）。

## 四、资源与算力
- 论文明确提到计算资源：使用内部集群，配备**NVIDIA RTX 2080 Ti（11GB）和A40（48GB）GPU**。
- 训练时长估计：
  - 复现所有基线结果约需**1周**（20块RTX 2080 Ti GPU）。
  - 包含增强、预训练和消融实验的完整结果约需**2周**。
- 由于使用早停和不同数据集大小，具体训练时长未逐一记录。

## 五、实验数量与充分性
- **实验规模**：
  - 基线实验：每个组合（n×m）重复**25次**（不同随机种子），三个数据集、三种模型，共超过千次实验。
  - 数据增强实验：每个增强方法在相同网格上运行一次（单种子），共三个增强×三个数据集×三个模型。
  - 预训练实验：LaBraM预训练对比重复25次（TUAB和CAUEEG）或5次（PhysioNet），包含所有网格点。
  - 控制实验：对比均匀子采样与连续子采样（TUAB，TCN，5种子）。
  - 消融实验：验证LaBraM兼容预处理对性能的影响（PhysioNet）。
- **充分性与公平性**：
  - 覆盖了三个不同任务（分类、诊断、分期）、三个不同架构、多种数据规模，结论具有较强的泛化能力。
  - 所有实验使用固定验证集和测试集，无被试者重叠，避免了数据泄露。
  - 超参数（学习率）对预训练和基线分别调优，确保对比公平。
  - 重复实验计算标准误，统计可靠。

## 六、主要结论与发现
1. **Q1：被试者数量是否严重限制性能？**  
   **是**。在所有数据集和模型上，性能随被试者数从25增加到数百人时显著提升，之后增长放缓。许多现有数据集（<13人）正处于性能受制区域。

2. **Q2：增加每被试者数据是否可靠替代被试者多样性？**  
   **否**。在TUAB和CAUEEG上，增加每被试者片段数几乎不提升性能；被试者多样性起主导作用。但PhysioNet睡眠分期更依赖于总样本量，少量被试者也可通过大量片段获得良好性能。

3. **Q3：现有数据增强能否有效提升性能？**  
   **不能**。除LaBraM在PhysioNet上受益于FrequencyShift和PhaseRandomisation外，其他增强效果微弱或不一致（PhaseRandomisation甚至伤害TCN/mAtt在PhysioNet上的性能）。增强可能破坏标签保留性。

4. **Q4：自监督预训练能否有效提升性能？**  
   **能**。LaBraM预训练在所有数据体制（除极少量微调数据外）持续提升性能，效果相当于增加每被试者数据量。预训练使LaBraM在性能上匹配甚至超越更小的模型。

## 七、优点
- **系统性与规模**：首个在大规模（>1000被试）EEG数据集上**显式分解被试者多样性与样本量**的影响研究，覆盖三个不同任务和三种模型架构。
- **实验设计严谨**：采用网格化子采样、重复实验、标准误差汇报、公平超参数调优。
- **理论与实践结合**：从统计学习理论引出假设，并通过大规模实验验证，结论有理论支撑。
- **开源代码**：全部代码公开，利于复现和扩展。
- **对领域有直接指导意义**：强调数据收集应优先增加被试者数，并鼓励发展针对被试者漂移的机器学习方法（如自监督学习）。

## 八、不足与局限
- **实验覆盖有限**：
  - 仅研究需要泛化到新被试者的场景（如临床诊断），未覆盖**BCI中主体特定模型**（该场景下被试者多样性不重要）。
  - 数据增强仅测试了三种，可能遗漏更有效的增强（如模仿被试者差异的增强）。
  - 自监督预训练仅使用LaBraM一种模型（基础版），未探索更大模型或更多预训练数据。
- **潜在偏差**：
  - LaBraM在PhysioNet上的预处理差异（15秒vs30秒片段）导致性能偏低，虽通过消融分析，但仍可能引入混淆。
  - 睡眠分期任务可能受通道选择（仅6个EEG）影响，结果不一定推广到全通道。
- **应用限制**：
  - 结论仅适用于当前三种任务，不能直接推广到所有EEG应用（如情绪识别、运动想象）。
  - 未研究**被试者分布漂移的本质**（解剖差异 vs. 疾病表型差异），这有助于设计更针对性的方法。
- **数据增强的负面效果**：PhaseRandomisation破坏了波形信息，说明现有增强不适合所有场景，未来需要更智能的保标签增强。

（完）
