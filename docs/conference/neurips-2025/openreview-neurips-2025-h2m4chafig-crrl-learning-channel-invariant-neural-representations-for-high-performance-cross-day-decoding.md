---
title: "CRRL: Learning Channel-invariant Neural Representations for High-performance Cross-day Decoding"
title_zh: CRRL：学习通道不变神经表示实现高性能跨天解码
authors: "Xianhan Tan, Binli Luo, Yu Qi, Yueming Wang"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=H2m4chAfig"
tags: ["query:eeg-latent"]
score: 7.0
evidence: 通过潜流形学习通道不变神经表示以应对跨天变异性，与EEG潜空间相关
tldr: 该论文针对BCI跨天解码性能不稳定问题（由于神经元死亡或电极移位导致通道级变化），提出学习通道不变神经表示的CRRL框架。通过通道重排模块和潜流形对齐，模型能够在不依赖特定通道顺序的情况下提取鲁棒特征，在神经信号漂移显著时仍保持高性能。其通道不变潜空间思想可直接应用于EEG缺失通道补全和跨天对齐。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-h2m4chafig/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1304, \"height\": 423, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-h2m4chafig/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1421, \"height\": 795, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-h2m4chafig/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1435, \"height\": 321, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-h2m4chafig/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1440, \"height\": 436, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-h2m4chafig/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1284, \"height\": 393, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-h2m4chafig/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1310, \"height\": 550, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-h2m4chafig/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1443, \"height\": 775, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-h2m4chafig/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 870, \"height\": 264, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-h2m4chafig/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1445, \"height\": 208, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-h2m4chafig/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 770, \"height\": 191, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-h2m4chafig/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 621, \"height\": 175, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-h2m4chafig/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1432, \"height\": 346, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-h2m4chafig/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1444, \"height\": 1172, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-h2m4chafig/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 875, \"height\": 222, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-h2m4chafig/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1016, \"height\": 389, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-h2m4chafig/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 734, \"height\": 208, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-h2m4chafig/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 873, \"height\": 432, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-h2m4chafig/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 735, \"height\": 466, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-h2m4chafig/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1015, \"height\": 223, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-h2m4chafig/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 733, \"height\": 196, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-h2m4chafig/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1017, \"height\": 384, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-h2m4chafig/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 728, \"height\": 269, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-h2m4chafig/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 453, \"height\": 117, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-h2m4chafig/table-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 875, \"height\": 153, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-h2m4chafig/table-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 611, \"height\": 411, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-h2m4chafig/table-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 765, \"height\": 376, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-h2m4chafig/table-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 648, \"height\": 490, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-h2m4chafig/table-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 466, \"height\": 370, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-h2m4chafig/table-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 703, \"height\": 370, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-h2m4chafig/table-024.webp\", \"caption\": \"\", \"page\": 0, \"index\": 24, \"width\": 676, \"height\": 331, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-h2m4chafig/table-025.webp\", \"caption\": \"\", \"page\": 0, \"index\": 25, \"width\": 682, \"height\": 451, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-h2m4chafig/table-026.webp\", \"caption\": \"\", \"page\": 0, \"index\": 26, \"width\": 663, \"height\": 451, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-h2m4chafig/table-027.webp\", \"caption\": \"\", \"page\": 0, \"index\": 27, \"width\": 680, \"height\": 411, \"label\": \"Table\"}]"
motivation: BCI跨天信号不稳定，以往潜流形对齐方法在显著漂移时失效。
method: 提出通道重排模块学习通道不变的潜表示。
result: 在跨天神经解码任务上实现了稳定提升。
conclusion: 为BCI跨天泛化提供了有效方法。
---

## Abstract
Brain-computer interfaces have shown great potential in motor and speech rehabilitation, but still suffer from low performance stability across days, mostly due to the instabilities in neural signals. These instabilities, partially caused by neuron deaths and electrode shifts, leading to channel-level variabilities among different recording days. Previous studies mostly focused on aligning multi-day neural signals of onto a low-dimensional latent manifold to reduce the variabilities, while faced with difficulties when neural signals exhibit significant drift. Here, we propose to learn a channel-level invariant neural representation to address the variabilities in channels across days. It contains a channel-rearrangement module to learn stable representations against electrode shifts, and a channel reconstruction module to handle the missing neurons. The proposed method achieved the state-of-the-art performance with cross-day decoding tasks over two months, on multiple benchmark BCI datasets. The proposed approach showed good generalization ability that can be incorporated to different neural networks.

---

## 论文详细总结（自动生成）

# CRRL论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）

- **核心问题**：脑机接口（BCI）在跨日解码中存在严重的性能不稳定性。主要原因在于神经信号的**通道级变异性**，包括：
  - 新神经元的出现与旧神经元的消失（missing neurons）
  - 神经元或电极的漂移（electrode shifts）
- **现有方法局限**：先前方法多尝试将多日神经信号对齐到低维潜在流形，但在信号出现显著漂移时效果不佳。另一类方法依赖大量数据预训练（如POYO、NDT2），但训练成本高、泛化受限。
- **本文目标**：通过学习**通道不变（channel-invariant）的神经表示**，以低成本实现长期稳定的跨日解码性能。

## 2. 方法论：核心思想、关键技术细节

- **核心思想**：将通道变异性分解为两类，分别设计模块处理：
  1. **通道重排模块（Rearrangement, RA）**：处理神经元漂移。学习一个置换矩阵，将目标日的信号通道顺序对齐到第0日。
  2. **通道重建模块（Reconstruction, RC）**：处理缺失神经元。基于VQ-VAE架构，重构缺失或损坏的通道信号。
- **关键技术细节**：
  - **RA模块**：
    - 使用共享参数的MLP从输入数据预测对数几率（logits）。
    - 应用Gumbel-Sinkhorn算法获得可微的双随机矩阵近似置换矩阵。
    - 训练损失：负皮尔逊相关系数损失（关注信号形状与趋势）+ 熵正则化项。
    - 推理时使用匈牙利算法离散化为精确置换矩阵。
  - **RC模块**：
    - 基于通道的VQ-VAE：编码器（含跨通道注意力）→ 向量量化层 → MLP解码器。
    - 对第0日与RA对齐后的目标日信号混合（7:3）进行训练，随机掩码部分通道。
    - 损失函数：时域MSE + 频域MSE（幅度和相位）+ VQ承诺损失。
  - **两阶段训练**：先训练RA模块（固定参数），再训练RC模块。推理时依次通过RA和RC处理目标日数据，然后使用第0日训练的简单解码器（SVM或Wiener Filter）进行下游任务。

## 3. 实验设计

- **数据集**：
  - **仿真数据集**：基于余弦调谐曲线模拟中心-外出任务，包含神经元新增/丢失、通道随机打乱、调谐函数改变三种变异。
  - **真实数据集**：
    - 人类数据集：手写数据集（31字符分类）、语音数据集（7词+“do nothing”分类）。
    - 猴子数据集：两个中心-外数据集(Monkey C & M)、两个等距腕部数据集(Monkey J & S)、一个抓握任务数据集(Monkey G)。任务包括轨迹回归和方向分类。
  - 时间跨度超过两个月。
- **基准方法**：
  - Stabilizedbci（流形对齐）、NoMAD（非线性流形对齐）、SD-Net（语义动态特征提取）、ADAN（对抗域适应）、Cycle-GAN（循环对抗域适应）。
  - 另与大规模模型POYO-1、NDT2多上下文进行对比。
- **评价指标**：回归任务用确定系数R²，分类任务用准确率Acc。
- **数据划分**：前5天作为训练/验证集，第6天及以后作为测试集，按天数分区间评估（[5,10)、[10,20)等）。

## 4. 资源与算力

- 文中提及：训练和推理在**NVIDIA Tesla A100 GPU**上进行，最大显存约22 GB。
- 未明确说明GPU数量、训练总时长等细节，仅提到“所有实验在A100 GPU上执行”。

## 5. 实验数量与充分性

- **实验数量**：
  - 仿真数据集上进行了3种变异的消融实验（表1、表11），包含不同变化比例。
  - 真实数据集上：5个猴子数据集（每个含多种解码任务）+ 2个人类数据集，共7个数据集。
  - 与5种基线方法对比（表2/7），与2种大型模型对比（表4），与2种域适应方法结合实验（表5）。
  - 消融实验（RA/RC单独、组合）在3个真实数据集上（表3）。
  - 参数敏感性分析、统计显著性测试（ANOVA + Tukey HSD）、t-SNE可视化、第0日质量敏感性实验等。
- **充分性与公平性**：
  - 对比方法使用了原文推荐或公开的超参数设置，并报告了标准差。
  - 消融实验全面，验证了两个模块的贡献。
  - 统计测试显示CRRL显著优于SD-Net和NoMAD（p<.001）。
  - 但部分对比方法（如POYO）的实验设置可能不完全对等（CRRL仅使用5天训练数据 vs POYO大规模预训练）。

## 6. 主要结论与发现

- CRRL在跨日解码任务上达到**最先进性能**，尤其时间跨度越长，优势越明显。
- 两个模块（RA + RC）共同使用效果最佳（表3），单独使用任一个均有性能下降。
- 在仿真数据上，RA对处理通道打乱至关重要，RC对处理神经元缺失至关重要。
- 可与现有域适应方法（如Cycle-GAN、ADAN）作为插件结合，进一步提升性能（表5）。
- 无需大量数据预训练，用少量数据即可接近甚至超越大型预训练模型性能（表4）。
- 方法具有良好泛化能力，可嵌入不同神经网络。

## 7. 优点

- **新颖的通道级不变表示思想**：将通道变异性显式分解为漂移和缺失两类，分别设计专用模块，逻辑清晰。
- **关键技术可解释性**：置换学习结合Gumbel-Sinkhorn可微分松弛，VQ-VAE提供离散稳健编码。
- **实验结果全面扎实**：覆盖仿真、多物种、多任务（运动、手写、语音），长期跨日测试，消融与分析充分。
- **兼容性强**：可作插件集成到其他方法，降低使用门槛。
- **资源需求低**：不依赖大规模预训练数据，有利于实际临床应用。

## 8. 不足与局限

- **性能随时间仍缓慢下降**：作者承认观察到长期性能缓慢衰减，可能源于神经元群体调谐模式的缓慢变化，当前方法尚未完美捕捉此变化规律。
- **实验覆盖**：虽然数据集多样，但均来自公开的侵入式记录（猴子和人类ECoG/微电极阵列），未在非侵入式信号（如EEG）上验证，应用场景有待扩展。
- **假设第0日质量良好**：虽然实验显示多日平均可缓解，但第0日数据仍为核心锚点，若第0日本身噪声大或代表性差，可能影响整体效果。
- **训练复杂度**：两阶段训练流程需要顺序完成，且RA模块需对每个目标日独立运行，可能增加计算开销。
- **统计分析有限**：虽报告了标准差并做了ANOVA，但未对所有对比方法在各数据集上逐一报告统计差异，公平性依赖已有结果。

（完）
