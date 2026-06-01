---
title: "Generalizable, real-time neural decoding with hybrid state-space models"
title_zh: 基于混合状态空间模型的通用实时神经解码
authors: "Avery Hee-Woon Ryoo, Nanda H Krishna, Ximeng Mao, Mehdi Azabou, Eva L Dyer, Matthew G Perich, Guillaume Lajoie"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=1i4wNFgHDd"
tags: ["query:eeg"]
score: 6.0
evidence: 用于BCI的实时神经解码
tldr: 实时神经解码对BCI至关重要，但传统方法泛化差，Transformer方法延迟高。本文提出POSSM混合架构，结合尖峰词元化和跨注意力与循环网络，在保持低延迟的同时实现强的泛化性能。在多个神经解码数据集上验证了其高效性和准确性。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-1i4wnfghdd/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 620, \"height\": 219, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-1i4wnfghdd/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1458, \"height\": 811, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-1i4wnfghdd/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1433, \"height\": 623, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-1i4wnfghdd/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1446, \"height\": 738, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-1i4wnfghdd/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1451, \"height\": 705, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-1i4wnfghdd/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1421, \"height\": 453, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-1i4wnfghdd/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1455, \"height\": 786, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1i4wnfghdd/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 543, \"height\": 512, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1i4wnfghdd/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 467, \"height\": 426, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1i4wnfghdd/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1278, \"height\": 343, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1i4wnfghdd/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1453, \"height\": 640, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1i4wnfghdd/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 605, \"height\": 321, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1i4wnfghdd/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1042, \"height\": 207, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1i4wnfghdd/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1379, \"height\": 209, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1i4wnfghdd/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1063, \"height\": 209, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1i4wnfghdd/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1131, \"height\": 256, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-1i4wnfghdd/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1288, \"height\": 211, \"label\": \"Table\"}]"
motivation: 实时神经解码中，传统方法泛化差，Transformer方法计算开销大。
method: 提出混合架构，结合尖峰词元化交叉注意力和循环状态空间模型。
result: 在低延迟下实现优于传统方法的泛化性能。
conclusion: 混合架构可同时满足实时性和泛化要求，适用于BCI。
---

## Abstract
Real-time decoding of neural activity is central to neuroscience and neurotechnology applications, from closed-loop experiments to brain-computer interfaces, where models are subject to strict latency constraints. Traditional methods, including simple recurrent neural networks, are fast and lightweight but often struggle to generalize to unseen data. In contrast, recent Transformer-based approaches leverage large-scale pretraining for strong generalization performance, but typically have much larger computational requirements and are not always suitable for low-resource or real-time settings. To address these shortcomings, we present POSSM, a novel hybrid architecture that combines individual spike tokenization via a cross-attention module with a recurrent state-space model (SSM) backbone to enable (1) fast and causal online prediction on neural activity and (2) efficient generalization to new sessions, individuals, and tasks through multi-dataset pretraining. We evaluate POSSM's decoding performance and inference speed on intracortical decoding of monkey motor tasks, and show that it extends to clinical applications, namely handwriting and speech decoding in human subjects. Notably, we demonstrate that pretraining on monkey motor-cortical recordings improves decoding performance on the human handwriting task, highlighting the exciting potential for cross-species transfer. In all of these tasks, we find that POSSM achieves decoding accuracy comparable to state-of-the-art Transformers, at a fraction of the inference cost (up to 9x faster on GPU). These results suggest that hybrid SSMs are a promising approach to bridging the gap between accuracy, inference speed, and generalization when training neural decoders for real-time, closed-loop applications.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）
实时神经解码在神经科学和神经技术中至关重要，例如闭环实验和脑机接口（BCI），这些场景对延迟有严格限制。传统方法（如简单循环神经网络）速度快、轻量，但难以泛化到未见数据；而近期基于Transformer的方法通过大规模预训练实现了强泛化性能，但计算需求大，不适合低资源或实时环境。论文旨在同时满足三个需求：稳健准确的预测、因果低延迟推理、灵活泛化到新受试者、任务和实验设置。为此，提出混合状态空间模型架构POSSM，将单个尖峰分词（通过交叉注意力）与循环状态空间模型（SSM）骨干结合，实现快速因果在线预测和高效泛化。

## 2. 论文提出的方法论：核心思想、关键技术细节
- **核心思想**：融合Transformer式的灵活输入处理（POYO风格的尖峰分词和交叉注意力）与SSM的高效在线推理能力。
- **关键技术细节**：
  - **输入处理**：在毫秒级分辨率上处理流式神经活动，使用50 ms连续时间块（也可用20 ms）。每个块中尖峰数量可变，表示为变长尖峰序列。
  - **尖峰分词**：每个神经尖峰用两个信息表示：神经单元身份（学习到的单元嵌入）和发生时间戳（旋转位置编码RoPE）。词元表示为 `x = (UnitEmb(i), t_spike)`，其中UnitEmb映射到D维向量。这使得模型能处理可变数量的单元，便于多会话和跨数据集预训练。
  - **输入交叉注意力**：采用POYO编码器，使用交叉注意力模块将变长尖峰词元序列压缩为固定大小的潜在表示。对每个50 ms时间块，使用单个可学习查询向量q ∈ R^(1×M)与尖峰词元（作为键值）计算注意力，输出单一潜在向量z(t)。
  - **循环骨干网络**：将z(t)输入到SSM（或RNN变体），更新隐藏状态 h(t) = f_SSM(z(t), h(t-1))。支持S4D、GRU、Mamba三种骨干。
  - **输出交叉注意力与读取**：选择最近k个隐藏状态（实验中k=3），使用交叉注意力模块查询进行行为预测。每个查询编码对应时间戳（RoPE）和可学习的会话嵌入，可预测每个时间块内多个输出，支持灵活对齐和预测未来行为。
  - **泛化策略**：
    - **单元识别（UI）**：冻结模型权重，仅学习新单元和会话嵌入，更新不到1%参数。
    - **全微调（FT）**：先UI训练若干epoch，然后解冻整个模型端到端训练。

## 3. 实验设计：数据集、场景、基准与对比方法
- **数据集**：
  - **非人灵长类（NHP）伸手任务**：四个公共数据集（Perich et al., O'Doherty et al., Churchland et al., NLB Maze），包含148个会话，超过670 million个尖峰，来自26,032个神经单元（M1、PMd、S1皮层）。测试包括：同动物其他天（Monkey C）、新动物（Monkey T）、新数据集（Flint et al. Monkey H）。
  - **人类手写解码**：Willett et al. 2021数据集，11个会话，单参与者想象书写字符，记录2个96通道微电极阵列的多单元阈值交叉事件，10 ms分箱，任务为分类31个字符/线条。
  - **人类语音解码**：Willett et al. 2023数据集，24个会话，参与者尝试说话，4个64通道微电极阵列覆盖前运动皮层和布罗卡区，多单元尖峰活动，20 ms分箱，任务为预测音素序列，评估音素错误率(PER)。
- **基准方法**：
  - NHP任务：MLP、S4D、GRU、Mamba、POYO（单会话和预训练版本）、NDT-2。
  - 手写任务：PCA-KNN、S4D、GRU、Mamba、POYO。
  - 语音任务：GRU（单方向/双向，有无噪声增强）、S4D、Mamba。
- **对比设置**：因果评估（模型只能看到当前和过去数据）；NHP任务使用1 s训练窗口，全试验评估（更长序列）；手写任务使用1 s窗口训练，1.6 s试验评估；语音任务使用全可变长度序列。

## 4. 资源与算力
文中明确提及：
- NHP单会话模型：单张NVIDIA RTX8000 GPU，训练时间小于30分钟。
- NHP多数据集预训练：四张NVIDIA H100 GPU，约36小时。
- 手写任务（POYO和POSSM从头训练及微调POYO-1）：单张RTX8000 GPU，LAMB优化器，batch size 256，学习率0.00256（微调o-POSSM时为0.008），训练600/1000 epoch。
- 语音任务基线：单张RTX8000 GPU，AdamW优化器，batch size 64。
- 语音POSSM：单张NVIDIA A100 80GB，batch size 16，学习率调度经交叉验证。

## 5. 实验数量与充分性
- **NHP任务**：包含5个测试子集（同动物其他天2个、新动物2个、新数据集1个），每个子集多个会话。对比了多种单会话模型（MLP、GRU、S4D、Mamba、POYO-SS、三种POSSM-SS）以及预训练模型（NDT-2 FT、POYO-1 UI/FT、o-POSSM三种骨干的UI/FT）。还进行了20 ms时间块实验、未来行为预测、尖峰时间消融、特征混合器MLP消融、循环编码器对比、LoRA微调初步实验。
- **手写任务**：9个会话，3个随机种子，报告平均准确率和标准差；计算了统计显著性（配对t检验）。
- **语音任务**：3个种子，报告平均PER。还进行了双向模型实验、无噪声增强对比、多模态输入初步实验。
- **样本与计算效率**：在NHP任务上进行了小样本实验，比较了微调与从头训练的样本效率和训练计算效率。也测量了推理时间（GPU和CPU）。
- **充分性评价**：实验覆盖多个物种、任务、会话和条件，消融实验充分，统计报告合理。但是语音任务基线较少（主要对比GRU变体），且未与最新Transformer模型对比（因作者指出Transformer不适合长序列语音任务）。

## 6. 论文的主要结论与发现
- **性能与效率**：POSSM在NHP伸手任务上匹配或超越所有基线，同时拥有更快推理速度和更低计算成本。单会话POSSM模型参数最少，o-POSSM约8M参数，推理时间<10 ms，满足实时BCI延迟要求。
- **多数据集预训练提升性能**：在NHP任务上，预训练的o-POSSM（尤其是FT）在跨会话、跨动物、跨数据集上显著优于单会话模型。
- **跨物种迁移学习**：在NHP数据上预训练，然后在人类手写任务上微调，o-POSSM达到SOTA准确率（>97%），显著优于从头训练的基线（~95%）和PCA-KNN（81%）。这是首次证明基于深度学习的解码器可从NHP运动皮层跨物种迁移到人类临床数据。
- **长序列解码**：在语音任务上，POSSM-GRU实现了最低音素错误率（27.32%），优于GRU（30.06%）、S4D（35.99%）、Mamba（32.19%），且即使无噪声增强也保持稳健。POSSM使用更少参数（32M vs GRU 55M）。双向POSSM进一步降低PER至25.80%。
- **混合SSM架构**是平衡准确率、推理速度和泛化性的有前景方法。

## 7. 优点
- **架构创新**：将POYO的灵活尖峰分词与SSM的高效在线推理结合，首次在神经解码中应用混合注意力-SSM模型。
- **实时适用性**：设计因果、低延迟推理（GPU上每块<10 ms，CPU上约2-5 ms），可部署于在线闭环实验。
- **强泛化能力**：通过单元识别和全微调策略，预训练模型可高效适应新会话、新动物、新任务，甚至跨物种（NHP到人类）。
- **跨物种迁移验证**：令人信服地展示了利用丰富NHP数据改善人类BCI解码的潜力，对临床数据稀缺问题有重要意义。
- **全面的实验评估**：涵盖三个物种（猴、人、鼠初步实验）、多种任务（伸手、手写、语音、跑步速度），包括因果评估、样本效率、推理速度、消融等。
- **开源承诺**：代码将通过torch_brain和项目页面公开。

## 8. 不足与局限
- **应用范围**：当前主要处理运动皮层尖峰数据（侵入式），虽提及可扩展至其他模态（如钙成像、EEG），但未实际验证。
- **监督训练**：仅探索了监督学习范式，未涉及自监督预训练，限制了在无行为标签数据上的应用。
- **语音任务预处理限制**：由于只有归一化的分箱尖峰计数（无精确尖峰时间），无法使用POYO风格分词，而是用值嵌入替代，限制了架构灵活性。
- **语音任务基线对比有限**：未与Transformer模型（如NDT-2、POYO）直接比较（因计算限制），但作者指出Transformer在长序列上计算成本高。
- **缺少在线闭环实验**：所有评估为离线模拟，虽设计为实时，但未在实际在线BCI系统中验证。
- **跨物种迁移**：仅在一个人类手写任务上测试，需要更多临床验证。
- **统计显著性**：手写任务报告了p值（与POSSM-GRU对比），但其他任务未系统报告。表格中部分误差棒（SD）较大，可能反映会话间变异性。
- **计算资源**：预训练需要4张H100 GPU 36小时，对于资源有限的实验室可能较高。

（完）
