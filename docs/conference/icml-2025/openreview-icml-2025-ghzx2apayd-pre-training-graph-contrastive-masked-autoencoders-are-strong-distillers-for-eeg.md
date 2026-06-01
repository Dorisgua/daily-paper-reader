---
title: Pre-Training Graph Contrastive Masked Autoencoders are Strong Distillers for EEG
title_zh: 预训练图对比掩码自编码器是EEG的强蒸馏器
authors: "Xinxu Wei, kanhao zhao, Yong Jiao, Hua Xie, Lifang He, Yu Zhang"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=gHzx2apaYD"
tags: ["query:eeg-latent"]
score: 8.0
evidence: 提出图掩码自编码器用于EEG，学习潜在表示以桥接高密度与低密度数据
tldr: 充分利用海量无标记高密度EEG数据以提升有限低密度场景性能是挑战。本文提出EEG-DisGCMAE统一预训练范式，融合图对比学习与掩码自编码器，通过图拓扑蒸馏损失函数实现知识迁移。实验证明该方法在跨密度EEG分类中表现优异，为EEG潜在空间表示学习提供了有效框架。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-ghzx2apayd/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1747, \"height\": 786, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ghzx2apayd/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 839, \"height\": 210, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ghzx2apayd/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 857, \"height\": 361, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ghzx2apayd/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1626, \"height\": 258, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ghzx2apayd/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 852, \"height\": 380, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ghzx2apayd/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1541, \"height\": 1720, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ghzx2apayd/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1454, \"height\": 724, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ghzx2apayd/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1555, \"height\": 587, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ghzx2apayd/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1573, \"height\": 664, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-ghzx2apayd/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1759, \"height\": 767, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ghzx2apayd/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 865, \"height\": 220, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ghzx2apayd/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 890, \"height\": 340, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ghzx2apayd/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 883, \"height\": 305, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ghzx2apayd/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 828, \"height\": 254, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ghzx2apayd/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1250, \"height\": 286, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ghzx2apayd/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1398, \"height\": 321, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ghzx2apayd/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1675, \"height\": 243, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ghzx2apayd/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1686, \"height\": 244, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ghzx2apayd/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1542, \"height\": 242, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ghzx2apayd/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1147, \"height\": 239, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ghzx2apayd/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1268, \"height\": 211, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ghzx2apayd/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1436, \"height\": 497, \"label\": \"Table\"}]"
motivation: 高低密度EEG数据间的知识迁移困难。
method: 统一图对比与掩码自编码器预训练，结合蒸馏损失。
result: 在跨密度EEG分类任务上取得最优性能。
conclusion: EEG-DisGCMAE能高效利用无标记EEG数据学习潜在表示。
---

## Abstract
Effectively utilizing extensive unlabeled high-density EEG data to improve performance in scenarios with limited labeled low-density EEG data presents a significant challenge. In this paper, we address this challenge by formulating it as a graph transfer learning and knowledge distillation problem. We propose a Unified Pre-trained Graph Contrastive Masked Autoencoder Distiller, named EEG-DisGCMAE, to bridge the gap between unlabeled and labeled as well as high- and low-density EEG data. Our approach introduces a novel unified graph self-supervised pre-training paradigm, which seamlessly integrates the graph contrastive pre-training with the graph masked autoencoder pre-training. Furthermore, we propose a graph topology distillation loss function, allowing a lightweight student model trained on low-density data to learn from a teacher model trained on high-density data during pre-training and fine-tuning. This method effectively handles missing electrodes through contrastive distillation. We validate the effectiveness of EEG-DisGCMAE across four classification tasks using two clinical EEG datasets with abundant data.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：如何有效利用海量无标注的高密度（HD）EEG数据，提升在仅有少量标注的低密度（LD）EEG数据场景下的分类性能，同时实现知识从高密度到低密度EEG的迁移。
- **研究动机**：临床上高密度EEG设备昂贵、复杂，低密度EEG更易获取但性能较差；而大量未标记的EEG数据未被充分利用。现有方法多聚焦于有监督的GNN架构，或分别采用对比/生成式预训练，缺乏二者的统一整合以及HD-to-LD的高效蒸馏。
- **整体含义**：本文将问题形式化为图迁移学习（GTL）和图知识蒸馏（GKD）的联合问题，旨在通过预训练和蒸馏桥接未标记/标记、高密度/低密度EEG数据，提出一个统一的预训练-蒸馏框架EEG-DisGCMAE。

### 2. 论文提出的方法论：核心思想、关键技术细节

- **核心思想**：  
  1. **统一图自监督预训练范式（GCMAE-PT）**：同时进行图对比学习（GCL）和图掩码自编码器（GMAE）预训练，通过“重构对比样本”和“对比重构样本”实现二者的相互监督与优化，增强教师和学生模型的表示能力。  
  2. **图拓扑蒸馏损失（GTD Loss）**：针对高密度到低密度蒸馏场景，利用丢失电极（Vd）的连接信息，定义正负节点对，通过KL散度对齐学生模型与教师模型的节点相似性分布，从而传递拓扑结构知识。  
  3. **教师-学生联合预训练**：通过共享Key队列，对教师和学生的扩展查询（含重构样本）同时进行对比学习，使预训练模型本身就成为强蒸馏器。

- **关键技术细节**：
  - **EEG图构建**：对静息态EEG时间序列进行带通滤波（α频段），计算功率谱密度（PSD）作为节点特征，使用Pearson相关系数构造邻接矩阵。
  - **教师-学生模型**：教师模型采用大参数量编码器（8层、128维、8头），学生模型采用轻量编码器（4层、64维、4头），支持图Transformer或DGCNN等骨干。
  - **预训练过程**：对HD和LD图进行数据增强（随机丢弃节点/边）获得查询和关键图，将二者混合后以可学习嵌入代替被丢弃节点生成掩码图，经编码器后通过解码器重建节点特征和结构，计算重建损失（MSE）。将重建的查询/关键图与原增强样本混合形成扩展对比样本，与共享Key队列中的正负键计算对比损失。总预训练损失为对比损失与重建损失之和。
  - **下游微调损耗**：交叉熵损失 + 传统logits蒸馏损失（KL散度） + GTD损失。GTD损失设计：对HD和LD图分别计算线性核相似矩阵，根据Vd连接规则定义正对（直接/间接连接）和负对（LD中错误连接），对正对的KL散度取平均除以负对的KL散度平均（加ϵ），鼓励学生模仿教师拓扑。

### 3. 实验设计：使用的数据集/场景、benchmark、对比方法

- **数据集**：
  - **EMBARC**：308名受试者，64/32/16导联（HD/MD/LD），两个任务：性别分类（男/女）和抑郁症严重程度分类（轻度/重度，基于HAMD-17）。
  - **HBN**：1594名睁眼/1745名闭眼受试者，128/64/32导联，两个任务：MDD诊断（健康vs MDD）和ASD诊断（健康vs ASD）。
- **对比方法**：
  - 传统ML：MLP、LSTM
  - GNN模型：GCN、GFormer、Hyper-GCN、EEGNet、EEG-Conformer、RGNN、DGCNN
  - 对比预训练：GCC、GraphCL、GRACE
  - 生成预训练：GraphMAE、GPT-GNN、GraphMAE2
  - 时间序列预训练：LaBraM（仅提及，未在主要表中）
- **基准设置**：所有模型均在同一HD/LD输入下进行公平比较，预训练模型使用相同骨干（图Transformer或DGCNN）。采用10折交叉验证，10次运行，评估指标AUROC和ACC。

### 4. 资源与算力

- **文中有提及**：优化器为Adam，预训练batch size=128，下游batch size=32，预训练200 epochs，下游微调400 epochs。但**未明确说明**使用的GPU型号、数量及具体训练时长。仅提到使用了Lehigh大学的研究计算基础设施（由NSF资助）。

### 5. 实验数量与充分性

- **实验数量丰富**：包含两个数据集上的四个分类任务，与十多种方法对比；进行了大量消融实验（如表2-表4、图3-图5、附录多个表格），覆盖：
  - 电极密度（HD/MD/LD）与模型大小（tiny/large）的影响（表2）
  - 不同蒸馏损失函数的对比（表3）
  - 不同预训练方法（GCL-PT、GMAE-PT、Seq. Comb. vs GCMAE-PT）（表4）
  - 鲁棒性分析（加噪声/随机丢弃电极）（表5）
  - 预训练数据集构成（全量 vs held-out）的影响（表13）
  - 不同脑电频段、连接度量、相似性核等超参数分析。
- **公平性**：实验时统一了骨干网络、输入电极密度、评价指标，并采用多次交叉验证。对比方法使用了各自最佳配置。
- **充分性**：实验覆盖了不同难度场景（HD-to-LD、HD-to-MD、H2H），且包含subject-dependent/independent对比（附录表8），总体较为充分。

### 6. 论文的主要结论与发现

- **性能提升显著**：所提出的EEG-DisGCMAE在所有任务上超越了对比方法，尤其在LD场景下提升幅度更大（例如HBN MDD任务，HD AUROC 87.4%，LD AUROC 84.8%）。
- **统一预训练优于单独或顺序组合**：GCMAE-PT相比单独GCL-PT或GMAE-PT及顺序组合均有明显优势（表4）。
- **GTD损失有效**：在HD-to-LD蒸馏中，加入GTD损失比仅用logits蒸馏或未使用蒸馏效果更好（表3）。
- **模型鲁棒性**：面对噪声和电极脱落，所提模型性能下降最小（表5）。
- **轻量模型可通过预训练+蒸馏达到接近重量级用HD数据的性能**：tiny模型（1.3M参数量）经预训练+蒸馏后，在LD上性能与未经预训练的大模型用HD数据相当。
- **可视化验证**：重建的EEG模式图显示，GCMAE-PT能在高掩盖率下还原关键脑区激活模式，与临床发现一致。

### 7. 优点

- **方法创新性**：首次在图上统一对比学习与掩码自编码器两种主流预训练范式，并实现内部相互监督，而非简单拼接。
- **蒸馏损失针对性强**：GTD损失专门设计用于HD-to-LD电极缺失场景，利用删除节点（Vd）的间接连接定义正负对，可有效传递拓扑信息。
- **统一教师-学生联合预训练**：通过共享Key队列同时对比教师和学生的查询与键，使预训练阶段就具备蒸馏能力，下游微调时自然过渡。
- **实用价值高**：允许使用廉价LD EEG设备达到接近HD效能，降低临床部署成本；且支持模型压缩（轻量学生）。
- **实验扎实**：在多个临床数据集、多种任务、多种骨干（GCN和Graph Transformer）上验证了有效性和鲁棒性。

### 8. 不足与局限

- **实验覆盖有限**：仅使用了一个EEG系统（10-20系统）的数据，未验证跨系统（不同电极布局）的泛化能力。
- **数据异构性处理粗糙**：预处理时直接降采样高密度数据以匹配低密度，导致信息丢失；无法利用低密度数据提升高密度模型（反向蒸馏未探索）。
- **超参数敏感未深入分析**：掩码比例、温度系数、θ阈值等超参数仅给出最优值（如50%掩码），缺乏详细敏感性讨论。
- **资源消耗未报告**：缺少GPU型号、训练时间等具体算力信息，难以复现代价估计。
- **极端低密度场景验证不足**：仅做了8电极的初步实验（表11），但未与更多基线对比。
- **理论分析缺失**：为何统一预训练优于顺序组合缺乏理论解释（仅基于两个假设）。
- **应用偏差风险**：实验仅针对抑郁症和自闭症分类，对其他脑疾病（如癫痫、中风）的迁移性未知。

（完）
