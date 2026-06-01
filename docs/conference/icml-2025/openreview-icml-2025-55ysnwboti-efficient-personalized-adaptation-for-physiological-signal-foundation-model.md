---
title: Efficient Personalized Adaptation for Physiological Signal Foundation Model
title_zh: 生理信号基础模型的高效个性化适应
authors: "Chenrui Wu, Haishuai Wang, Xiang Zhang, Chengqi Zhang, Jiajun Bu"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=55ysNwbOTI"
tags: ["query:eeg"]
score: 5.0
evidence: 生理信号基础模型的个性化适应，适用于EEG类数据
tldr: 本文提出PhysioPFM框架，用于高效个性化适应时间序列基础模型以适应生理信号。针对医疗环境中计算资源有限和数据隐私问题，PhysioPFM能够快速适配到私有、不均衡的本地数据，在多个生理信号任务上优于通用的基础模型。为EEG信号的分析和适应提供了可行方案。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-55ysnwboti/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 833, \"height\": 533, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-55ysnwboti/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 810, \"height\": 434, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-55ysnwboti/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1685, \"height\": 694, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-55ysnwboti/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1584, \"height\": 368, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-55ysnwboti/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 858, \"height\": 536, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-55ysnwboti/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1418, \"height\": 601, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-55ysnwboti/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1416, \"height\": 597, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-55ysnwboti/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 779, \"height\": 502, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-55ysnwboti/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 787, \"height\": 487, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-55ysnwboti/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 774, \"height\": 302, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-55ysnwboti/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1775, \"height\": 979, \"label\": \"Table\"}]"
motivation: 通用基础模型在医疗私有数据上不如特定方法。
method: 提出PhysioPFM框架，结合个性化适应策略。
result: 在生理信号任务上优于通用基础模型。
conclusion: 为隐私敏感场景下的生理信号建模提供了有效方法。
---

## Abstract
Time series analysis is crucial across various fields like energy, environment, transportation, finance and health. Deep learning has significantly advanced this field, particularly, the Time Series Foundation Model (TSFM) excels in multiple domains due to extensive pre-training. In this work, we focus on TSFM's challenges in medical practice: limited computing resources and medical data privacy. TSFM variants include fine-tuned models and those pre-trained for rapid deployment on diverse data. There may not be enough computing resources to train physiological signals locally in hospitals, and generalized TSFM is still inferior to task-specific methods on private, imbalanced local data. To address this, we propose PhysioPFM, a framework for efficiently personalizing TSFM. Our approach involves low-rank pre-training on public datasets, generator training by trained LoRA weights, and efficient weight generation via local data. Experimental results demonstrate that integrating generated models with TSFM enhances performance, and transferability, and reduces the need for additional sensitive data training.

---

## 论文详细总结（自动生成）

# 详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：在医疗临床实践中，时间序列基础模型（TSFM）面临两大挑战：一是医院本地计算资源有限，无法对生理信号（如 EEG、ECG 等）进行完整微调；二是患者数据隐私受法律限制（如 GDPR），不能上传至云端进行预训练。同时，通用 TSFM 在私有、不平衡的本地数据上表现不如专用方法。
- **研究动机**：现有两类 TSFM（基于 LLM 微调类和大规模通用预训练类）均难以满足隐私保护和轻量级部署的需求。专用生理信号模型（如 SleepFM、ECG-FM）依赖大量私有数据，迁移性差。因此，需要一种既能利用公开数据预训练、又能高效适配私有本地数据、且保护隐私的个性化方案。
- **整体含义**：论文提出 PhysioPFM 框架，通过“训练一次、通用个性化”（train-once-for-all personalization）的思路，在公开生理信号数据集上训练低秩适配器（LoRA）生成器，再利用本地私有数据的形态学特征（shapelets）实时生成定制 LoRA 参数，从而实现轻量级、隐私安全的模型适应。

## 2. 论文提出的方法论

### 核心思想
- 利用公开生理信号数据，对基础 TSFM 进行 LoRA 微调，得到任务与 LoRA 权重的映射对。
- 训练一个扩散 Transformer（DiT）作为权重生成器，以时间序列的判别性子序列（shapelets）为条件，学习生成对应的 LoRA 参数。
- 在本地部署时，仅需提取私有数据的 shapelets，输入 DiT 即可生成定制 LoRA，与通用 TSFM 结合得到个性化模型。

### 关键技术细节
1. **数据准备**：
   - 使用公开生理信号数据集（如 MIT-BIH、PTB-XL、Sleep-EDF 等）的多个子任务，对预训练的 TSFM（6层 GPT-2 架构，预训练于 UTSD 数据集）进行 LoRA 微调。
   - 损失函数：交叉熵损失 + 锚定分类器损失（anchored classifier loss），后者利用神经崩溃理论中的 Simplex ETF 结构缓解类别不平衡。
   - 存储映射对：每个子任务对应的 LoRA 权重（∆W = BA）。

2. **生成器训练**：
   - 输入：LoRA 权重展平并分块（每块 576 维）后加入噪声；条件输入为 shapelets（通过离线 shapelet 发现算法提取）。
   - 网络：扩散 Transformer（DiT），12 层，1000 步扩散，线性噪声调度。
   - 损失函数：最小化预测 LoRA 与真实 LoRA 之间的 L2 距离。

3. **个性化推理**：
   - 本地用户仅需：提取私有数据的 shapelets → 输入 DiT 生成定制 LoRA → 与通用 TSFM 合并（W = W0 + ∆W）→ 直接进行预测。
   - 无需本地微调，仅需生成器推理，可保护隐私。

### 公式或算法流程（文字说明）
- 前向传播：`W0x + BAx`
- 训练目标：`min_ϕ Σ_k Σ_j ||∆W_k - G_ϕ(S(t_k), ∆W^j_k)||_2^2`
- 算法伪代码：每次迭代从映射对中采样，对 LoRA 添加噪声，用 DiT 预测去噪后的权重。

## 3. 实验设计

### 使用的数据集和任务
- **睡眠阶段检测**：Sleep-EDF 数据集（多通道 EEG/EOG/EMG），5 类（Wake/N1/N2/N3/REM）。
- **情绪识别**：DREAMER 数据集（EEG+ECG），三任务（valence / arousal / dominance）。
- **心律失常诊断**：MIT-BIH 心律失常数据集（ECG），二分类（正常 vs 异常）。
- **步态冻结检测**：FOG 数据集（EEG/EMG/ECG/SC/ACC），二分类（FoG vs 非FoG）。
- **训练/验证/测试划分**：60% / 20% / 20%，随机抽样。

### Benchmark
- 对比方法分为三组：
  - 通用时间序列模型：Informer, FEDformer, SimMTM, TimesNet, PatchTST, iTransformer。
  - 时间序列基础模型：OneFitsAll (GPT4TS), Time-LLM, MOMENT。
  - 专用任务模型：SleepFM, SleepDG（睡眠）；LSTM-MLP, OMHGL（情绪）；DeepArr（心律失常）；Extra Tree Classifier（FoG）。

### 实验充分性
- 共 4 个独立任务，每个任务报告 Accuracy、Macro F1、Kappa（睡眠）或 AUC（情绪）或 Precision/Recall/F1（其他）。
- 每个方法运行 3 次取平均值和标准差。
- 消融实验：去除锚定分类器损失、调节温度参数、去除本地 shapelets、去除本地 LoRA。
- 超参数影响分析：LoRA 秩（rank）影响、训练样本数影响、输入 prompt 类型（shapelets vs 全序列 vs 文本）影响。
- 效率对比：在 FOG 任务上比较不同方法的显存占用、适应时间。

## 4. 资源与算力

- 论文未明确说明训练所用的 GPU 型号、数量、总训练时长。
- 但提到：DiT 训练在服务器上需要约 20 GB GPU 显存；本地推理时 DiT 仅需 3 GB GPU 显存。
- 公共数据集 LoRA 微调阶段未给出具体算力信息。

## 5. 实验数量与充分性

### 实验数量
- **主实验**：4 个独立任务，每个任务包含 11~12 个对比方法，报告多项指标。
- **消融实验**：5 个变体（去除锚定损失、调节温度、去除形状条件、去除 LoRA 生成等），在 3 个数据集上对比。
- **超参数分析**：3 组（rank、训练样本数、prompt 类型），各含 4~5 个取值。
- **效率分析**：1 个任务（FoG）上对比 5 种代表性方法。

### 充分性评估
- **客观性**：使用公开数据集，划分固定，所有基线按原论文设置或标准实现，结果取 3 次平均，标准差合理。
- **公平性**：与通用模型、基础模型、专用模型均做了对比；消融实验覆盖了主要模块。
- **不足**：效率分析只用于一个任务；未展示在更多私有数据上的泛化能力；未与联邦学习等隐私保护方法对比。

## 6. 论文的主要结论与发现

- PhysioPFM 在睡眠检测、情绪识别、心律失常、FoG 检测四个任务上均超过所有基线，尤其在睡眠任务上 Accuracy 达 86.39%，比最好基线 MOMENT 高 4.49%。
- 锚定分类器损失（基于 Simplex ETF）能有效缓解类别不平衡，提升约 2~4% 的准确率。
- 使用 shapelets 作为条件比直接使用全序列或文本 prompt 效果更好，且对 prompt 数量更鲁棒。
- LoRA 秩取 4 即可达到最优，过大的秩（8/16）无法带来增益。
- 生成器训练样本越多，生成 LoRA 质量越高。
- 适应效率方面，PhysioPFM 在显存（3GB）和适应时间上显著优于需要本地全微调的方法（如 OneFitsAll），同时准确率远高于零样本方法。

## 7. 优点

- **隐私友好**：私有数据无需离开本地，仅使用公开数据训练生成器，符合 GDPR 等法规。
- **计算高效**：本地只需 DiT 推理（3GB 显存）和 TSFM 前向计算，无需反向传播微调。
- **通用性强**：框架可适配多种生理信号（EEG、ECG、EMG 等）和多种任务（分类、检测）。
- **创新性**：首次将 shapelets 与条件扩散模型结合用于 LoRA 生成，桥接了时间序列与模型参数空间。
- **消融充分**：对各个设计选择（损失函数、条件形式、秩、样本量）都进行了定量分析。

## 8. 不足与局限

- **实验覆盖有限**：仅涉及 4 个公开数据集，未在真实医院私有数据上验证；效率分析只包含一个任务。
- **与联邦学习等对比缺失**：未与联邦学习、差分隐私等主流隐私保护方法进行比较，无法量化其额外隐私风险。
- **生成器训练成本**：DiT 训练需要约 20GB 显存，对于小规模机构可能仍有一定门槛。
- **依赖公开数据质量**：公开数据集覆盖不全（如 EEG 数据类不平衡严重），可能导致生成器偏差。
- **未讨论连续学习场景**：本地数据更新后，需要重新提取 shapelets 并生成 LoRA，未考虑增量更新的开销。
- **理论分析较薄弱**：仅证明了简化 ETF 的最优性，未对生成器的泛化误差给出理论界。

（完）
