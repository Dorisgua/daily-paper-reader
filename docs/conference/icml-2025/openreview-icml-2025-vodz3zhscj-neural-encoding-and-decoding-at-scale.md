---
title: Neural Encoding and Decoding at Scale
title_zh: 大规模神经编码与解码
authors: "Yizi Zhang, Yanchen Wang, Mehdi Azabou, Alexandre Andre, Zixuan Wang, Hanrui Lyu, International Brain Laboratory, Eva L Dyer, Liam Paninski, Cole Lincoln Hurwitz"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=vOdz3zhSCj"
tags: ["query:eeg"]
score: 4.0
evidence: 大规模多任务神经编码解码模型
tldr: 本文提出NEDS模型，通过多任务掩码策略同时进行神经编码与解码，在大规模多动物数据上预训练，解决了现有模型只能单向预测的问题。该方法在多个基准上取得优异表现，为理解神经活动与行为间的双向关系提供了强大工具。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-vodz3zhscj/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1766, \"height\": 782, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vodz3zhscj/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1778, \"height\": 1230, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vodz3zhscj/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1338, \"height\": 619, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-vodz3zhscj/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1588, \"height\": 574, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-vodz3zhscj/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 867, \"height\": 116, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vodz3zhscj/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1437, \"height\": 261, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vodz3zhscj/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 855, \"height\": 331, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vodz3zhscj/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 543, \"height\": 501, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vodz3zhscj/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 764, \"height\": 288, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vodz3zhscj/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 734, \"height\": 586, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vodz3zhscj/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 533, \"height\": 549, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vodz3zhscj/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 863, \"height\": 289, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vodz3zhscj/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1263, \"height\": 236, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vodz3zhscj/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1081, \"height\": 279, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vodz3zhscj/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1770, \"height\": 322, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-vodz3zhscj/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 938, \"height\": 238, \"label\": \"Table\"}]"
motivation: 现有大规模模型仅能单向预测神经活动或行为，缺乏双向建模能力。
method: 采用多任务掩码策略，同时掩盖神经和行为模态，实现双向编码解码。
result: 在IBL数据集上预训练，有效捕捉神经与行为间双向关系。
conclusion: NEDS为系统神经科学提供了可扩展的双向建模框架。
---

## Abstract
Recent work has demonstrated that large-scale, multi-animal models are powerful tools for characterizing the relationship between neural activity and behavior. Current large-scale approaches, however, focus exclusively on either predicting neural activity from behavior (encoding) or predicting behavior from neural activity (decoding), limiting their ability to capture the bidirectional relationship between neural activity and behavior. To bridge this gap, we introduce a multimodal, multi-task model that enables simultaneous Neural Encoding and Decoding at Scale (NEDS). Central to our approach is a novel multi-task-masking strategy, which alternates between neural, behavioral, within-modality, and cross-modality masking. We pretrain our method on the International Brain Laboratory (IBL) repeated site dataset, which includes recordings from 83 animals performing the visual decision-making task. In comparison to other large-scale modeling approaches, we demonstrate that NEDS achieves state-of-the-art performance for both encoding and decoding when pretrained on multi-animal data and then fine-tuned on new animals. Surprisingly, NEDS's learned embeddings exhibit emergent properties: even without explicit training, they are highly predictive of the brain regions in each recording. Altogether, our approach is a step towards a foundation model of the brain that enables seamless translation between neural activity and behavior.

---

## 论文详细总结（自动生成）

### 论文核心问题与整体含义（研究动机和背景）

- **研究动机**：当前大规模神经数据分析模型主要分为两类——从行为预测神经活动的 **编码模型**（如 POSANI 等人，Wang 等人）和从神经活动预测行为的 **解码模型**（如 POYO+、NDT2）。这两类模型是 **单向** 的，无法同时捕获神经活动与行为之间的 **双向关系**。因此，亟需一个统一框架，既能完成编码又能完成解码，以更全面地理解脑-行为耦合。

- **整体含义**：本文提出的 NEDS 模型，通过在同一架构中融合多任务掩码学习，实现了 **同时进行大规模神经编码与解码**。它利用多动物数据（IBL 数据集）预训练，在单会话和多会话场景下均取得了最佳性能，并且学习到的神经元嵌入自动含有脑区信息，向 **基础脑模型** 迈出了关键一步。

---

### 论文提出的方法论

- **核心思想**：采用 **多任务掩码策略**，在训练中交替使用四种不同的掩码方案，使模型学习到神经与行为之间的 **条件分布**，从而统一编码和解码。

- **关键技术细节**：
  - **四种掩码方案**：
    1. **神经掩码**：完全掩盖神经活动，从行为数据中预测神经活动（编码任务）。
    2. **行为掩码**：完全掩盖行为数据，从神经活动中预测行为（解码任务）。
    3. **模态内随机掩码**：在同一模态内随机掩码部分 token，利用本模态未掩码部分重建（增强模态内依赖）。
    4. **跨模态随机掩码**：跨神经和行为模态随机掩码，同时利用两模态未掩码部分重建（促进跨模态联合学习）。
  - **模型架构**（图1B）：
    - 将神经尖峰计数（20ms bin）和行为数据（连续量、离散量）分别通过 **模态特定分词器** 转换为 token 序列。
    - 添加 **时间、模态、会话嵌入** 后拼接成统一序列，输入 **共享 Transformer 编码器**。
    - 将编码器输出按模态拆分，分别输入 **模态特定线性解码器** 进行重建。
    - 会话适应：使用 **会话特定输入矩阵** 和 **会话嵌入** 处理跨会话变异性。
  - **生成过程**（公式1）：
    - 神经活动假定为 **Poisson 发射模型**，损失为负对数似然。
    - 连续行为使用 **MSE 损失**，离散行为使用 **交叉熵损失**。
  - **多任务混合训练**：每个训练批次随机采样一种掩码方案，使模型同时学习所有条件期望：E[X|Y], E[Y|X], E[X_masked|X_unmasked], E[Y_masked|Y_unmasked], E[(X,Y)_masked|(X,Y)_unmasked]。

---

### 实验设计

- **数据集**：
  - **IBL 重复位点数据集**：83只小鼠执行相同视觉决策任务，Neuropixels 记录5个目标脑区（PO, LP, DG, CA1, VISa），共27,380个神经元，225个脑区记录。数据按试次对齐，时长2秒（100个时间bin，20ms）。
  - **额外验证**：附文中还使用了 **猴伸手抓取数据集 MC-RTT**（单会话，未对齐数据）。

- **任务**：
  - 神经编码：预测尖峰活动（所有行为变量联合/单独），指标 **bits per spike (bps)**。
  - 神经解码：预测4个行为变量——选择（分类准确率）、block 先验（分类准确率）、轮速（单试次 R²）、胡须运动能量（单试次 R²）。

- **对比方法**：
  - 线性回归（Ridge）、降秩回归（RRR，多会话）、POYO+、NDT2（均为多会话预训练+微调）。单会话基线包括 NEDS 单模态变体。

- **实验设置**：
  - 留出10只动物作为测试集，训练集73只动物（74个会话）。
  - 单会话实验：在每只留出动物上单独训练+测试。
  - 多会话实验：预训练于73只，微调于10只留出动物的训练集（70%），验证（10%），测试（20%）。
  - 超参数调优：使用 Ray Tune 随机采样50组配置（验证集最优），多会话预训练时仅调优10只动物的子集后固定架构。
  - 脑区分类：从模型输入/输出矩阵提取神经元嵌入，训练线性 SVM，5折交叉验证。

- **消融实验**：
  - 掩码方案消融（依次去除跨模态、模态内掩码，表2）。
  - 模型大小消融（3M vs 12M 参数，表9）。
  - 嵌入消融（去除模态/时间嵌入，表11）。

---

### 资源与算力

- **NEDS 多会话（74会话，12M参数）**：16张 Nvidia RTX8000（48GB）GPU，训练 <2 天，2000 个 epoch。
- **NEDS 单会话**：1张 Nvidia A40 GPU，<2 小时训练，<30 分钟（单模态解码）。
- **NDT2 多会话**：4张 Nvidia H200 GPU，4.5 小时（600 epochs）；后续微调使用1张 H100。
- **POYO+ 多会话**：1张 A100 GPU，约 6 小时。
- **超参数搜索**：使用4张 A40/V100 GPU，1.5天内完成。
- **电力和耗时细节均在附录 F 中明确给出**，算力描述充分。

---

### 实验数量与充分性

- **实验数量**：
  - 单会话实验：在10只留出动物上分别训练，对比4种基线（线性、RRR、单模态NEDS、多模态NEDS）。
  - 多会话实验：预训练于73只，微调于10只，对比 POYO+, NDT2, RRR。
  - 消融实验：3种（掩码方案、模型大小、嵌入），均含10只动物平均结果。
  - 脑区分类：5种脑区，5折交叉验证。
  - 额外验证：猴抓取数据集（表12）。
- **充分性与公平性**：
  - 统计指标：10只动物上的均值±标准误，且每个点（session）单独展示（散点图）。
  - 超参数调优：所有方法均使用随机搜索验证集最优（除 POYO+ 外，但文中说明其调优类似）。
  - 消融实验覆盖关键设计选择（掩码方案、嵌入、模型容量），验证了各组件的贡献。
  - **局限**：多会话预训练超参数调优受限于计算，仅在小子集上进行，可能未达全局最优；但三种方法均采用类似折中，公平性基本可接受。

---

### 论文的主要结论与发现

1. **统一编码解码可行且有效**：多任务掩码策略使 NEDS 能在同一模型上同时进行高精度的编码与解码。
2. **多动物预训练显著提升性能**：相比单会话，多会话 NEDS 在编码任务提升 24%，解码提升 4%-11%（图2B）。
3. **SOTA 性能**：在10只留出动物上，NEDS 的编码和解码性能均优于 POYO+（提升1%-13%）和 NDT2（提升11%-37%），以及线性/降秩基线。
4. **神经元嵌入的涌现属性**：无需显式脑区标签，NEDS 学习到的神经元嵌入即可预测脑区，准确率达 83%（线性SVM），且 UMAP 可视化显示清晰聚类。
5. **运动变量比认知变量更能解释神经变异性**（与 IBL 先前结论一致），且组合变量优于单个变量（表1）。

---

### 优点

- **创新性**：首次在大规模多动物尺度上实现了 **统一的编码与解码**，克服了之前模型的单向限制。
- **方法论健壮**：多任务掩码策略借鉴了 NLP/视觉领域的先进思想（UL2, MAE），并适配到神经行为数据，设计合理。
- **可扩展性**：架构支持多模态输入/输出，能处理缺失模态（如仅神经或仅行为），便于未来加入 LFP、细胞类型等新模态。
- **涌现性质**：验证了大规模预训练可以自动产生富含生物学信息的表示（脑区预测），为无监督发现提供可能。
- **公平实验**：提供了详细的超参数调优流程、消融实验、资源消耗说明，复现性良好。

---

### 不足与局限

1. **仅使用试次对齐数据**：标准但限制预训练数据量。作者指出未对齐数据（如 POYO 原始训练）可能提升泛化能力，是未来方向。
2. **超参数调优受限**：多会话预训练时，因计算成本仅用10只动物子集确定架构，可能不是全局最优。作者呼吁开发标准化基准（如 FALCON）以促进更公平比较。
3. **未探索更大规模训练**：模型参数量最多12M，对比 NLP 基座模型较小，文中也未展示 scaling law 的全面分析（仅有模型大小消融）。
4. **数据集单一**：主要实验仅在 IBL 数据集上进行（虽附有猴抓取验证，但规模小）。缺乏多数据集、多任务泛化性测试。
5. **脑区分类仅使用线性分类器**：虽然简单有效，但可能低估高维非线性可分性；且混淆矩阵显示某些脑区（如 LP 与 DG）易混淆，原因尚待深究。
6. **行为变量有限**：仅使用4个任务变量，可能遗漏其他重要行为维度（如瞳孔、面部表情等），影响编码和解码上限。

---

（完）
