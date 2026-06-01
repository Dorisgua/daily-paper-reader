---
title: "LUNA: Efficient and Topology-Agnostic Foundation Model for EEG Signal Analysis"
title_zh: LUNA：高效且拓扑无关的EEG信号分析基础模型
authors: "Berkay Döner, Thorir Mar Ingolfsson, Luca Benini, Yawei Li"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=uazfjnFL0G"
tags: ["query:eeg-latent"]
score: 9.0
evidence: 提出拓扑无关的EEG潜在空间表示，直接匹配EEG潜在空间表示需求
tldr: LUNA提出拓扑无关的EEG基础模型，通过可学习查询和交叉注意力将任意通道数的EEG压缩为固定维度潜在空间，计算复杂度线性增长。在五个数据集上验证了跨布局泛化能力，并在分类和回归任务上达到最优性能。自监督预训练使其无需大量标注数据，可快速适配下游任务。该模型为异构EEG数据统一分析提供了高效方案。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-uazfjnfl0g/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1439, \"height\": 701, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uazfjnfl0g/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1443, \"height\": 1159, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uazfjnfl0g/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1444, \"height\": 618, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uazfjnfl0g/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1416, \"height\": 373, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uazfjnfl0g/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 789, \"height\": 590, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uazfjnfl0g/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1143, \"height\": 910, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uazfjnfl0g/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 789, \"height\": 588, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uazfjnfl0g/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 786, \"height\": 585, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uazfjnfl0g/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 903, \"height\": 720, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-uazfjnfl0g/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1443, \"height\": 616, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-uazfjnfl0g/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1396, \"height\": 655, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-uazfjnfl0g/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1265, \"height\": 854, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-uazfjnfl0g/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1298, \"height\": 602, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-uazfjnfl0g/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1433, \"height\": 299, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-uazfjnfl0g/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1289, \"height\": 1257, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-uazfjnfl0g/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 951, \"height\": 614, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-uazfjnfl0g/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1388, \"height\": 267, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-uazfjnfl0g/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1279, \"height\": 223, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-uazfjnfl0g/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 834, \"height\": 525, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-uazfjnfl0g/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 850, \"height\": 526, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-uazfjnfl0g/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1449, \"height\": 260, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-uazfjnfl0g/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 852, \"height\": 132, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-uazfjnfl0g/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1444, \"height\": 206, \"label\": \"Table\"}]"
motivation: 现有EEG模型因电极布局多样而难以推广，亟需统一拓扑的表示。
method: 使用交叉注意力将任意通道数EEG压缩为固定维度的潜在表示，支持线性复杂度。
result: 在多个数据集上验证了泛化能力和效率，任务性能达到领先水平。
conclusion: LUNA为EEG领域提供了一种可扩展、拓扑无关的基础模型框架。
---

## Abstract
Electroencephalography (EEG) offers a non-invasive lens into human brain activity, but building large‐scale models is hampered by $\textit{topological heterogeneity}$: each public corpus defines its own electrode layout, limiting generalization. We introduce $\textbf{LUNA}$ ($\textbf{L}$atent $\textbf{U}$nified $\textbf{N}$etwork $\textbf{A}$rchitecture), a self-supervised foundation model that reconciles disparate electrode geometries while scaling linearly---not quadratically---with channel count. LUNA compresses multi-channel EEG into a fixed-size, topology-agnostic latent space via learned queries and cross-attention. Downstream transformer blocks then operate exclusively on this latent representation using patch-wise temporal self-attention, decoupling computation from electrode count. Pre-trained on TUEG and Siena ($\>$21,000 h raw EEG across diverse montages) using a masked-patch reconstruction objective, LUNA transfers effectively to four downstream tasks: abnormality detection, artifact rejection, slowing classification, and emotion recognition. It demonstrates highly competitive performance across several benchmarks, achieving state-of-the-art results on TUAR and TUSL, e.g., $\textbf{0.921 AUROC}$ on TUAR, while reducing FLOPs by $\textbf{300}$$\times$ and trimming GPU memory use by up to $\textbf{10}$$\times$. Critically,  these gains are consistent across all evaluated electrode configurations. Code is available at https://github.com/pulp-bio/biofoundation

---

## 论文详细总结（自动生成）

# LUNA: 高效且拓扑无关的EEG信号分析基础模型 — 论文总结

## 1. 核心问题与整体含义（研究动机与背景）

脑电图（EEG）是一种非侵入性的大脑活动观测手段，在临床诊断、认知神经科学和人机交互中具有重要作用。然而，当前EEG深度学习模型面临一个根本瓶颈：**拓扑异构性**（topological heterogeneity）。不同公开EEG数据集采用的电极数量（如20、22、29、62通道）和布局各不相同，导致模型难以跨数据集迁移。例如，运动想象解码器在跨数据集迁移时准确率下降高达14个百分点，情绪识别模型在SEED与DEAP之间下降13–15个百分点。

现有解决方案要么为每种电极布局训练独立模型，要么只保留共有电极（丢弃多达80%的数据），或者采用扁平化空间-时间注意机制（计算复杂度为$O((S \cdot C)^2)$，随通道数二次增长），内存消耗极大。因此，亟需一种**单一、与电极布局无关、计算效率随通道数线性增长的架构**。

本文提出的LUNA（Latent Unified Network Architecture）正是为了解决上述问题，通过**拓扑无关的潜在空间表示**，实现跨异构EEG布局的统一建模。

## 2. 方法论：核心思想、关键技术细节

### 2.1 核心思想
LUNA采用**自监督预训练 + 微调**范式。其核心创新在于：通过一组**可学习查询向量（learnable queries）**和**交叉注意力机制**，将任意数量通道的EEG特征映射到一个**固定大小的潜在空间**，从而解耦后续处理与原始电极布局和通道数。后续的时序自注意力模块仅在该潜在空间上运算，计算复杂度与通道数无关（线性增长）。

### 2.2 关键技术细节

#### （1）输入表示与特征提取
- 原始EEG信号 $\mathbf{x} \in \mathbb{R}^{B \times C \times T}$（批次B，通道C，时间点T）被分割成大小为$P$的非重叠补丁（patches），每个补丁表示一个时间片段。
- 每个补丁通过两条并行路径嵌入：
  - **时序嵌入**：1D卷积网络（含GroupNorm、GELU），提取局部时序特征。
  - **频率嵌入**：对补丁做傅里叶变换，提取幅度和相位，经MLP投影。
- 两部分求和得到补丁特征 $\mathbf{x}_{\text{features}}$，并加上基于3D电极坐标的**NeRF式正弦位置编码**（经MLP投影）。

#### （2）通道统一模块（Channel-Unification Module）
- 定义 $Q$ 个可学习查询向量 $\mathbf{Q}_{\text{learn}} \in \mathbb{R}^{Q \times E}$（正交初始化）。
- 对每个批次-补丁实例（共 $B \cdot S$ 个），将查询重复为 $\tilde{\mathbf{Q}} \in \mathbb{R}^{(B \cdot S) \times Q \times E}$。
- 将输入特征 $\mathbf{X}_{\text{token}}$ 重塑为 $\mathbf{X}' \in \mathbb{R}^{(B \cdot S) \times C \times E}$，作为键（K）和值（V）。
- 执行**多头交叉注意力**（查询=$\tilde{\mathbf{Q}}$，键/值=$\mathbf{X}'$），得到输出 $\mathbf{A}_{\text{out}} \in \mathbb{R}^{(B \cdot S) \times Q \times E}$。
- 经过前馈网络（FFN）和残差连接，再通过$L$层Transformer编码器（作用于查询维度），得到统一的潜在表示 $\mathbf{X}_{\text{unified}} \in \mathbb{R}^{(B \cdot S) \times Q \times E}$。
- 这样，**后续计算与原始电极数量C完全解耦**，计算复杂度为$O(B \cdot S \cdot Q \cdot C \cdot E)$，即**线性于通道数C**。

#### （3）补丁级时序编码器（Patch-wise Temporal Encoder）
- 将 $\mathbf{X}_{\text{unified}}$ 重塑为 $\mathbf{X}'_{\text{unified}} \in \mathbb{R}^{B \times S \times (Q \cdot E)}$，即每个时间步的 token 包含来自所有通道的聚合信息。
- 通过堆叠的Transformer编码器块（带RoPE旋转位置编码）捕捉时序依赖。由于token数量仅为$S$（而非$S \cdot C$），**时序注意力的复杂度为$O(B \cdot S^2 \cdot Q \cdot E)$**，远低于全注意力的$O(B \cdot S^2 \cdot C^2 \cdot E)$。

#### （4）解码器
- **预训练（重建）**：使用$C$个可学习解码器查询，通过交叉注意力从潜在表示重建被掩码与可见的补丁，优化Smooth L1损失和查询特化损失。
- **微调（分类）**：使用单个聚合查询，通过交叉注意力得到池化表示，送入MLP进行分类。

#### （5）训练损失
- **重建损失**：Smooth L1，对掩码和可见补丁分别计算（掩码部分权重1，可见部分权重$\alpha=0.05$）。
- **查询特化损失**：鼓励各查询的注意力分布正交化，避免冗余。通过计算查询-通道亲和矩阵，最小化其Gram矩阵的非对角元素均值。

## 3. 实验设计

### 3.1 数据集
- **预训练**：TUEG（14,987名受试者，21,787小时） + Siena（14名受试者，141小时），共**超过21,900小时**原始EEG数据。电极布局包括20、22、29通道。所有下游测试集的受试者和记录均排除在预训练集外。
- **下游微调与评估**：
  - **TUAB**（异常EEG检测）：二分类，22通道双极导联，官方训练/测试划分。
  - **TUAR**（伪迹检测）：多分类（5类），22通道双极。采用80%/10%/10%随机样本级划分（与EEGFormer一致）。
  - **TUSL**（慢波事件分类）：4类，22通道双极。同样采用80%/10%/10%划分。
  - **SEED-V**（情绪识别）：5类，62通道单极。将15个试次等分为训练/验证/测试。

### 3.2 基准方法
比较对象包括：
- **监督模型**：SPaRCNet、ContraWR、CNN-Transformer、FFCL、ST-Transformer、EEGNet、EEG-GNN、GraphS4mer。
- **自监督模型**：BENDR、BrainBERT、EEGFormer、BIOT、EEG2Rep、FEMBA、CEReBrO、LaBraM、CBraMod。

### 3.3 LUNA配置
- **Base**（7M参数）：Q=4，E=64，隐藏大小256，8层时序编码器。
- **Large**（43M参数）：Q=6，E=96，隐藏大小576，10层。
- **Huge**（311.4M参数）：Q=8，E=128，隐藏大小1024，24层。

### 3.4 预处理与评估
- 所有数据：0.1–75 Hz带通滤波，50/60 Hz陷波，重采样至256 Hz。TUEG/AB/AR/SL使用双极导联，Siena和SEED-V使用单极。每通道z-score归一化。
- 评估指标：对于TUAB报告Balanced Accuracy、AUROC、AUPR；对于TUAR/TUSL报告AUROC和AUPR；对于SEED-V报告Balanced Accuracy、Cohen's Kappa、Weighted F1。所有结果均报告三次随机种子的均值与标准差。

## 4. 资源与算力
- **GPU**：8块NVIDIA A100（预训练Base和Large）；Huge模型使用16块A100。
- **训练时长**：预训练约1天（Base和Large在8块GPU上）；Huge未明确时长但使用更多GPU。
- **软件**：PyTorch 2.4.1，CUDA 12.1，bf16混合精度。
- **计算量评估**：对每个前向传播使用 `fvcore` 的 `FlopCountAnalysis` 测量FLOPs（50个随机输入）。

## 5. 实验数量与充分性

### 5.1 实验数量
- **4个下游任务**（TUAB、TUAR、TUSL、SEED-V）的主实验结果。
- **计算效率对比**：对不同补丁数和通道数，测量FLOPs和GPU内存，与LaBraM、CBraMod比较；还包括与BIOT的详细表格（附录）。
- **消融实验**：在TUAB和TUAR上对以下组件进行消融：
  - 用基于区域的注意力替代可学习查询（Region-based Attention）
  - 去除查询特化损失
  - 去除频率特征
- **超参数探索**：在固定 $Q \cdot E$ 预算下，改变 $Q$ 和 $E$ 的组合（4×64、2×128、8×32、16×16）。
- **潜在空间分析**：t-SNE可视化预训练嵌入在TUAB和TUAR上的分离程度；可视化查询注意力模式（图4）。
- **掩码重建示例**：展示20、22、29通道的重建质量（附录图6-8）。
- **统计检验**：对消融实验进行配对t检验（附录表13）。
- **预训练损失曲线**（附录图5）。

### 5.2 实验充分性与公平性
- **公平性**：所有下游测试集受试者均排除在预训练集外，确保泛化评估无泄露。TUAB使用官方划分；TUAR/TUSL采用与EEGFormer一致的样本级划分（但论文承认受试者独立划分是金标准，建议未来采用）。SEED-V采用试次级划分。
- **充分性**：覆盖了多种任务（检测、分类、识别）、多种电极布局（20/22/29/62通道）、多种模型规模（Base/Large/Huge）。消融实验覆盖了各关键组件。计算效率对比细致。但注意：
  - TUAR/TUSL的样本级划分可能导致信息泄露（同一受试者的不同样本可能跨划分），论文已指出此局限。
  - 消融实验中部分差异（如去除特化损失）经统计检验不显著，但论文仍保留该损失作为正则化手段。
  - SEED-V上LUNA性能低于CBraMod约2–3个百分点，论文承认泛化到全新高密度布局仍有挑战。

## 6. 主要结论与发现
- **拓扑无关性**：LUNA通过可学习查询和交叉注意力，成功将不同电极布局的统一建模为固定大小潜在空间。
- **计算效率**：与LaBraM（全注意力，$O(C^2 S^2)$）和CBraMod（交替注意力，$O(\max(C^2, S^2))$相比，LUNA在通道数增加时计算量近乎恒定（线性缩放），在补丁数增加时也显著更优。具体：FLOPs降低高达300倍，GPU内存降低高达10倍。
- **下游性能**：
  - **TUAB**：LUNA-Huge的AUROC为0.8957，AUPR为0.9029，与LaBraM-Huge（0.9162/0.9204）和CBraMod（0.9156/0.9221）有差距，但超过大多数自监督方法。
  - **TUAR**：LUNA-Huge取得**SOTA** AUROC 0.921。
  - **TUSL**：LUNA-Huge取得**SOTA** AUROC 0.802。
  - **SEED-V**：LUNA-Large最佳Bal. Acc. 39.18%，低于CBraMod（40.91%），但展示了正规模律。
- **消融结论**：频率特征对性能贡献最显著（去除后AUROC下降0.009–0.012）；查询特化损失和可学习查询消融后变化很小（约0.003–0.007），但论文强调其正则化/灵活性价值。
- **查询可视化**：不同查询在电极空间上表现出特化（如局部化或全局聚合），证明交叉注意力学到了数据驱动的空间基函数。

## 7. 优点
- **方法新颖**：将PerceiverIO的潜在瓶颈机制首次系统性引入EEG，实现拓扑无关的端到端自监督基础模型，计算复杂度线性于通道数。
- **效率显著**：实验验证了在大通道数（如256通道）和长序列场景下的巨大优势，适合未来高密度EEG和实时边缘部署。
- **预训练规模大**：使用超过21,900小时EEG数据，涵盖多种布局，是当前EEG基础模型中数据量较大的之一。
- **实验设计全面**：覆盖四种下游任务、多种模型规模、详尽的计算对比、消融实验和潜在空间可视化，统计检验支持。
- **开源可复现**：承诺发布代码和预训练权重，且预处理和超参数细节透明。

## 8. 不足与局限
- **SEED-V泛化不足**：在62通道未见布局上，LUNA性能落后顶尖方法2–3 pp，表明对全新高密度布局的零样本泛化仍有瓶颈，可能源于预训练布局多样性有限（仅20/22/29通道）以及位置编码的局限性。
- **预训练布局多样性有限**：论文承认预训练仅包含三种主导布局，建议未来纳入更多数据集和随机通道丢弃来改进泛化。
- **TUAR/TUSL划分不够严谨**：未采用受试者独立划分（而是样本级随机划分），可能导致信息泄露，论文已建议未来基准采用金标准。
- **部分消融结果统计不显著**：查询特化损失的影响经配对t检验p=0.2136，不显著，但论文仍以其正则化作用保留。需更多证据表明其必要性。
- **未与其他拓扑无关方法深入比较**：如MMM（依赖手工特征）、PopT（依赖外部坐标）、Saeed et al. (2021)（有监督且无3D编码）。论文仅在消融中与“基于区域注意力”（类似MMM思想）做简单比较。
- **实时部署验证不足**：仅提及边缘部署的潜力（附录），但未进行实际边缘设备上的延迟和功耗测试。
- **伦理考虑较浅**：仅在结论段提及公平性和隐私风险，未展开讨论或提出具体缓解措施。

（完）
