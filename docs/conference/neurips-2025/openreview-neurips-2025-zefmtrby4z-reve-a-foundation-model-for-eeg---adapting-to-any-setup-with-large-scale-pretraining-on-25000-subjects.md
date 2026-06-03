---
title: "REVE: A Foundation Model for EEG - Adapting to Any Setup with Large-Scale Pretraining on 25,000 Subjects"
title_zh: "REVE: 一个基于25,000名被试大规模预训练的通用EEG基础模型"
authors: "Yassine El Ouahidi, Jonathan Lys, Philipp Thölke, Nicolas Farrugia, Bastien Pasdeloup, Vincent Gripon, Karim Jerbi, Giulia Lioi"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=ZeFMtRBy4Z"
tags: ["query:eeg-latent"]
score: 8.0
evidence: EEG基础模型学习通用嵌入作为潜在表示
tldr: "该论文提出REVE，一个基于25,000名被试预训练的EEG基础模型。通过新颖的4D位置编码方案，学习到跨不同记录配置通用的潜在空间表示，在分类和回归任务上超越现有方法，为EEG分析提供了强大的通用表示。"
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-zefmtrby4z/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1352, \"height\": 539, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1419, \"height\": 463, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1453, \"height\": 916, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1198, \"height\": 554, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1456, \"height\": 441, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 979, \"height\": 895, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 905, \"height\": 225, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 891, \"height\": 751, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1259, \"height\": 576, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1154, \"height\": 534, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1156, \"height\": 533, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1453, \"height\": 449, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1156, \"height\": 535, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1152, \"height\": 630, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1147, \"height\": 428, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1157, \"height\": 607, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1157, \"height\": 606, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1276, \"height\": 518, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 908, \"height\": 282, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1329, \"height\": 363, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1399, \"height\": 285, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 774, \"height\": 379, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-zefmtrby4z/table-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 1457, \"height\": 191, \"label\": \"Table\"}]"
motivation: 现有EEG基础模型难以泛化到异构数据配置。
method: 提出4D位置编码和遮蔽自编码预训练，学习通用EEG嵌入。
result: 在多个下游任务上取得最优性能，尤其在线性探测中表现突出。
conclusion: 为EEG表示学习提供了大规模可泛化的基础模型方案。
---

## Abstract
Foundation models have transformed AI by reducing reliance on task-specific data through large-scale pretraining. While successful in language and vision, their adoption in EEG has lagged due to the heterogeneity of public datasets, which are collected under varying protocols, devices, and electrode configurations. Existing EEG foundation models struggle to generalize across these variations, often restricting pretraining to a single setup, resulting in suboptimal performance, in particular under linear probing.
We present REVE (Representation for EEG with Versatile Embeddings), a pretrained model explicitly designed to generalize across diverse EEG signals. REVE introduces a novel 4D positional encoding scheme that enables it to process signals of arbitrary length and electrode arrangement. Using a masked autoencoding objective, we pretrain REVE on over 60,000 hours of EEG data from 92 datasets spanning 25,000 subjects, representing the largest EEG pretraining effort to date.
REVE achieves state-of-the-art results on 10 downstream EEG tasks, including motor imagery classification, seizure detection, sleep staging, cognitive load estimation, and emotion recognition. With little to no fine-tuning, it demonstrates strong generalization, and nuanced spatio-temporal modeling. We release code, pretrained weights, and tutorials to support standardized EEG research and accelerate progress in clinical neuroscience.

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：EEG 数据具有高度异构性：不同设备、电极配置、记录协议、受试者差异导致模型很难跨设置泛化。已有的 EEG 基础模型（如 BIOT、LaBraM、CBraMod）大多局限在单一固定蒙太奇（如 TUH 的 19/21 通道）上预训练，面对多样化布局时性能严重下降，尤其在线性探测（linear probing）场景下表现不佳。
- **整体含义**：本文旨在构建一个能够**任意 EEG 设置**（任意电极数量、任意布局、任意长度）下**通用**的 EEG 基础模型，从而推动 EEG 分析在临床、BCI 等领域的标准化与可迁移性。

## 2. 论文提出的方法论

- **核心思想**：结合**灵活的 4D 位置编码**与**大规模异构预训练数据**，通过**掩码自编码（MAE）** 自监督学习，使模型学到鲁棒的通用 EEG 表示。
- **关键技术细节**：
  1. **4D 位置编码**：
     - 利用电极的 3D 空间坐标 (x,y,z) 加上时间维度 t，构成 4D 坐标。
     - 加入高斯噪声增强鲁棒性；扩展至 4D 傅里叶位置编码（基于 Défossez et al. 的 2D 方法），生成高频/低频混合的固定特征。
     - 同时加入可学习的线性层 + GELU + LayerNorm 分支，产生最终位置编码，兼具结构先验与适应能力。
     - 该编码可直接处理任意电极布局和任意时间长度，无需固定蒙太奇或重新训练。
  2. **时空块掩码（Spatio-temporal Block Masking）**：
     - 在空间（围绕选定通道的半径 Rs）和时间（半径 Rt）上连续掩码，而非随机掩码，增加重建难度，促进更有效的学习。
     - 另设 Dropout 策略，整通道丢弃部分掩码。
  3. **掩码自编码（MAE）框架**：
     - 编码器处理可见块，解码器重建被掩码块；两者共享同一位置编码。
     - 使用 L1 损失（对噪声更鲁棒），并引入**二级损失（Secondary Loss）**：通过注意力池化从所有编码器层的输出中生成全局紧凑表示，再重建掩码块。
     - 二级损失鼓励编码器各层均贡献有用信息，避免最终层过拟合重建，提升冻结表示的质量。
  4. **Transformer 改型**：
     - 使用 RMSNorm、GEGLU 激活函数、Flash Attention v2、去除偏置等，提升训练稳定性和效率。
- **公式/算法流程**（文字说明）：
  - 输入 EEG \( X \in \mathbb{R}^{C \times T} \)，分割成重叠的 \( C \times p \times w \) 的块。
  - 线性嵌入 → 添加 4D 位置编码 → 应用掩码（保留约 45% 可见块） → 编码器只处理可见块 → 解码器用可学习掩码令牌和位置编码重建原始信号。
  - 总损失 = 主 L1 损失 + λ× 二级 L1 损失。

## 3. 实验设计

- **预训练数据集**：92 个公开数据集，总共 61,415 小时、24,274 名受试者、150,833 次会话。来源包括 OpenNeuro、MOABB、TUH 等，涵盖临床、BCI、认知等多种场景。
- **下游任务与数据集**（10 个）：
  - 运动想象：PhysioNet-MI (4 类)、BCIC-IV-2a (4 类)
  - 事件类型：TUEV (6 类)
  - 异常检测：TUAB (2 类)
  - 睡眠分期：HMC (5 类)、ISRUC (5 类)
  - 情绪识别：FACED (9 类)
  - 精神疾病：Mumtaz (2 类)
  - 精神压力：MAT (2 类)
  - 想象语音：BCIC2020-3 (5 类)
- **对比方法**：
  - 非基础模型：EEGNet、EEGConformer、SPaRCNet、ContraWR、CNN-Transformer、FFCL、ST-Transformer 等。
  - 基础模型：BIOT、LaBraM-Base、CBraMod。
- **评估指标**：平衡准确率（Balanced Accuracy），部分报告 Cohen's Kappa 和加权 F1。

## 4. 资源与算力

- **训练硬件**：使用 NVIDIA A100 GPU（80GB），CPU 为 Intel Cascade Lake SP 6248，40 核，节点内存 192 GB，共享全闪存并行文件系统。
- **训练时长估计（附录 F.1）**：
  - REVE-Base 模型约需要 **260 A100 GPU 小时**（基于 FLOPs 估算公式）。
  - 论文未明确报告总数或节点数，但说明使用了 HPC 集群资源（IDRIS 和 Digital Alliance Canada）。
- **预训练数据规模**：19 TB 原始数据 → 6 TB 预处理后数据。

## 5. 实验数量与充分性

- **实验数量**：覆盖 10 个下游任务，每个任务多组随机种子（标准差报告）；另有多组消融实验：
  - 掩码比例与策略（随机 vs 块掩码，对比表 18）
  - 次级损失效果（表 17）
  - 位置编码各组件（表 19）
  - 激活/归一化选择（表 20）
  - 稀疏通道设置（表 21）
  - 少样本学习（表 22）
  - 模型大小缩放（Base vs Large，线性探测表 4）
- **充分性与客观性**：
  - 所有下游任务使用与先前工作完全一致的数据划分和预处理，确保公平比较。
  - 对 ISRUC 数据集修正了基线代码中错误包含颏电极的问题，提高公正性。
  - 报告了误差带（标准差），并采用多次重复随机初始化。
  - 实验设计相对全面，消融验证了各组件贡献。

## 6. 论文的主要结论与发现

- **REVE在10个下游任务中取得新SOTA**，平均平衡准确率较之前最佳基础模型 CBraMod 提升 **2.5%**。
- **线性探测（冻结表示）** 性能大幅领先 CBraMod：REVE-Large 平均 0.654 对比 CBraMod 0.501（提升约 15%）。
- **预训练收益显著**：REVE 无预训练时低于 CBraMod，但加预训练后提升 11%，而 CBraMod 仅提升 2%，说明 REVE 真正从预训练中学习到有用表示。
- **泛化能力强**：能处理未见过的蒙太奇（如双极导联 TUEV）和更长的时间窗口（30 秒睡眠数据）。
- **缩放规律**：更大模型（Large）在线性探测上表现更好，提示存在缩放效应。

## 7. 优点

1. **架构灵活性**：4D 位置编码无需固定电极布局，可处理任意长度和配置，这是现有模型不具备的。
2. **大规模异构预训练**：数据集规模（25k 受试者、60k 小时）和多样性远超先前工作，为泛化奠定数据基础。
3. **二级损失**：鼓励层间信息共享，显著提升冻结表示质量，对线性探测和少样本场景尤其有效。
4. **方法论完整**：时空块掩码、GEGLU、RMSNorm 等技术经过消融验证选择合理。
5. **可重复性与开放贡献**：开源代码、模型权重、教程，利于社区复现和应用。

## 8. 不足与局限

1. **输入长度限制**：要求信号至少 1 秒且为 1 秒的整数倍，不适用于任意非整数长度（论文建议未来可用因果掩码+填充）。
2. **数据分布偏差**：预训练数据主要来自北美和欧洲，人口多样性不足；论文承认需要更广泛的数据收集。
3. **未涉及零样本/少样本系统评估**：虽做了简单的少样本实验，但零样本和更系统的少样本基准尚未建立。
4. **简单 SSL 方法**：仅使用基础 MAE，未探索对比学习或其他更先进的自监督方法（论文列为未来工作）。
5. **缩放定律未精确建模**：观察到缩放效应，但未量化精确的 scaling law。
6. **计算开销**：虽然4D PE计算量小，但整体模型（Large 408M 参数）仍需较多 GPU 资源，对中小实验室可能门槛较高。

（完）
