---
title: Glocal Information Bottleneck for Time Series Imputation
title_zh: 时序插补的全局-局部信息瓶颈方法
authors: "Jie Yang, Kexin Zhang, Guibin Zhang, Philip S. Yu, Kaize Ding"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=m4rBrmNA9y"
tags: ["query:eeg-latent"]
score: 7.0
evidence: 基于潜空间的时序数据插补
tldr: 时间序列插补在高缺失率下存在局部过拟合与隐表征扭曲问题。本文提出全局-局部信息瓶颈方法，在优化逐点重建损失的同时，通过信息瓶颈引入全局分布约束，使模型在训练和推理阶段保持一致的潜空间分布。实验表明该方法在各种缺失场景下显著优于现有插补方法，为时序数据插补提供了新的训练范式。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-m4rbrmna9y/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1417, \"height\": 761, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-m4rbrmna9y/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1455, \"height\": 543, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-m4rbrmna9y/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1444, \"height\": 575, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-m4rbrmna9y/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1445, \"height\": 550, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-m4rbrmna9y/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1445, \"height\": 540, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-m4rbrmna9y/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 699, \"height\": 323, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-m4rbrmna9y/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1293, \"height\": 311, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-m4rbrmna9y/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 698, \"height\": 275, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-m4rbrmna9y/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1372, \"height\": 912, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-m4rbrmna9y/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1352, \"height\": 880, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-m4rbrmna9y/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1029, \"height\": 2273, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-m4rbrmna9y/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1069, \"height\": 2261, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-m4rbrmna9y/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1031, \"height\": 2271, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-m4rbrmna9y/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1044, \"height\": 2270, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-m4rbrmna9y/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1293, \"height\": 1538, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-m4rbrmna9y/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1307, \"height\": 1910, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-m4rbrmna9y/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1451, \"height\": 614, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-m4rbrmna9y/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1437, \"height\": 1883, \"label\": \"Table\"}]"
motivation: 现有时序插补模型只关注局部数值重建，在高缺失率下隐空间分布畸变。
method: 提出全局-局部信息瓶颈，在逐点重建外增加全局分布一致性约束。
result: 在多种缺失模式下改进插补质量，隐空间分布更稳定。
conclusion: 全局信息引导能有效提升时序插补模型的鲁棒性。
---

## Abstract
Time Series Imputation (TSI), which aims to recover missing values in temporal data, remains a fundamental challenge due to the complex and often high-rate missingness in real-world scenarios. Existing models typically optimize the point-wise reconstruction loss, focusing on recovering numerical values (local information). However, we observe that under high missing rates, these models still perform well in the training phase yet produce poor imputations and distorted latent representation distributions (global information) in the inference phase. This reveals a critical optimization dilemma: current objectives lack global guidance, leading models to overfit local noise and fail to capture global information of the data. To address this issue, we propose a new training paradigm, **Glocal** **I**nformation **B**ottleneck (**Glocal-IB**). Glocal-IB is model-agnostic and extends the standard IB framework by introducing a Global Alignment loss, derived from a tractable mutual information approximation. This loss aligns the latent representations of masked inputs with those of their originally observed counterparts. It helps the model retain global structure and local details while suppressing noise caused by missing values, giving rise to better generalization under high missingness. Extensive experiments on nine datasets confirm that Glocal-IB leads to consistently improved performance and aligned latent representations under missingness. Our code implementation is available in [https://github.com/Muyiiiii/NeurIPS-25-Glocal-IB](https://github.com/Muyiiiii/NeurIPS-25-Glocal-IB).

---

## 论文详细总结（自动生成）

## 论文总结：Glocal Information Bottleneck for Time Series Imputation

### 1. 核心问题与整体含义（研究动机和背景）
- **问题**：现有时序插补（TSI）方法主要优化逐点重建损失（局部数值精度），但在高缺失率下，模型训练损失低却测试性能差，隐空间分布严重扭曲。这种“优化困境”表明模型过度拟合局部噪声，未能捕获数据的全局结构信息。
- **背景**：缺失值在医疗、交通、能源等领域普遍存在，现有方法（如TimesNet、GPVAE）虽能收敛，但推理时插补质量骤降。作者通过可视化发现：当缺失率升高，隐空间分布与完整数据分布偏离越大，插补质量越差。现有基于信息瓶颈（IB）的方法（如GPVAE）仍依赖局部重建，未能解决该问题。

### 2. 方法论
- **核心思想**：提出**Glocal-IB**（全局-局部信息瓶颈），在标准IB框架上增加一个**全局对齐损失**，通过可处理的互信息近似，使掩码输入的隐表示与原始观测数据的隐表示对齐，从而同时保留全局结构与局部细节，抑制缺失噪声。
- **关键技术细节**：
  - 整体目标函数：$\min_{\theta,\phi} [\alpha \cdot L_{Reg} + \beta_1 \cdot L_{Loc} + \beta_2 \cdot L_{Glo}]$。
  - **正则化损失** $L_{Reg}$：最小化隐变量 $Z$ 与掩码输入 $X_o$ 的互信息 $I(Z;X_o)$，通过KL散度上界实现，假设隐变量服从高斯分布，使用重参数化技巧。
  - **局部损失** $L_{Loc}$：最大化 $I(X;Z)$ 的下界，等价于MSE重建损失，确保局部数值精度。
  - **全局对齐损失** $L_{Glo}$：基于InfoNCE推导，使用对比学习思想，将原始数据同一时间步的编码作为正样本，其他时间步作为负样本，通过一个轻量MLP投影后计算相似度。有两种实现：$L_{Glo\_1}$（InfoNCE形式）和 $L_{Glo\_2}$（简化对齐形式）。
- **模型无关性**：仅需在原编码器-解码器架构上加一个MLP投影器，可应用于Transformer、TimesNet、SAITS等任意模型。

### 3. 实验设计
- **数据集**：9个公开数据集：ETTh1/2, ETTm1/2, Beijing Air, PEMS-Traffic, Electricity, Weather, Metr-LA。涵盖电力、交通、空气质量、气象等场景。
- **基准与对比方法**：对比9种方法：Transformer、SAITS、TimesNet、DLinear、FreTS、PatchTST、iTransformer、GPVAE、TimeMixer。此外在泛化分析中额外对比了USGAN、TCN等。
- **评估指标**：MAE和MSE。
- **缺失模式**：主要采用点缺失（随机掩码10%-90%），额外测试了块缺失（Block Missing）。

### 4. 资源与算力
- 文中在附录C明确说明：所有实验在单张NVIDIA 4090 GPU（24GB显存）上运行，使用PyTorch 2.6.0，优化器Adam，学习率0.001，batch size=64，训练30个epoch，隐维度256。**未提供具体总训练时间和能耗数据**。

### 5. 实验数量与充分性
- **实验数量**：共进行了多组实验：
  - 主实验：9个数据集 × 5种缺失率（10%/30%/50%/70%/90%）× 9个基线 + 本方法，共约450个配置。
  - 泛化性分析：在ETTh1上对TimesNet和SAITS使用4种训练范式（Ori, FM_align, Glo_1, Glo_2）对比。
  - 缺失模式分析：点缺失与块缺失对比。
  - 效率分析：内存与时间对比。
  - 消融实验：去除正则化损失、去除全局对齐损失、仅局部损失，在ETTh1/2/ETTm1/2上验证。
  - 敏感性分析：调整三个损失权重。
  - 隐空间可视化：t-SNE或类似降维展示分布变化。
- **充分性与公平性**：
  - 数据集覆盖多领域，基线全面（包括CNN、Transformer、MLP、VAE等）。
  - 所有实验基于固定随机种子平均5次结果，数据切分使用标准协议（60%/20%/20%时序划分）。
  - 模型实现基于PyPOTS基准库，参数遵循原论文。但部分大模型（如iTransformer）在PEMS-Traffic上出现OOM，未完全公平。
  - 消融和敏感性分析充分验证各组件贡献。

### 6. 主要结论与发现
- **性能优越**：Glocal-IB在9个数据集上全部取得最佳或次佳结果，尤其在ETT子集上MSE降低最高达40%。
- **解决隐空间扭曲**：在10%-90%缺失率下，Glocal-IB保持隐空间稳定分布，而其他方法在30%以上即开始扭曲、70%以上崩溃。
- **模型无关性验证**：将Glocal-IB应用于Transformer、TimesNet、SAITS均显著提升性能，且仅增加极少计算开销。
- **全局对齐优于基础模型对齐**：相比使用Time-MoE（时序基础模型）对齐，Glocal-IB的全局对齐效果更好，因为基础模型预训练任务（预测）语义信息有限。
- **缺失模式鲁棒**：在块缺失这种更困难的场景下，Glocal-IB提升仍然显著。
- **轻量高效**：仅增加一个MLP，内存和运行时间开销可忽略（远小于基础模型对齐）。

### 7. 优点
- **理论扎实**：从互信息角度严格推导上下界，将全局对齐有机融入IB框架。
- **方法简洁实用**：仅需一个MLP，无需额外超参数调优（权重灵敏度较低），易于集成到现有TSI模型。
- **实验系统全面**：覆盖多领域、多缺失率、多缺失模式、多骨干网络，并包含丰富的可视化与分析（隐空间、效率、消融）。
- **开源代码**：提供可复现代码和预训练模型，有助于社区验证。

### 8. 不足与局限
- **极低观测率下的性能提升有限**：在90%缺失率下，全局对齐信号太弱，提升不如中等缺失率明显（论文在附录F中承认）。
- **泛化性验证范围有限**：虽然主实验在9个数据集上完成，但模型无关性验证（将Glocal-IB应用到不同骨干）主要集中于ETTh1/2/ETTm1/2四个数据集，对其他更大规模或不同特性数据集（如Metr-LA）的敏感性分析不足。
- **计算资源细节不够完善**：虽然说明了GPU型号和batch size，但未报告每次训练的具体时间（如每个数据集平均运行时间），使得效率比较不够精确。
- **对比基础模型对齐时的公平性**：Time-MoE是大型模型，但论文未详细说明其微调方式，可能导致对齐时的领域适应不足。
- **社会影响讨论**：虽然附录E有简要分析，但未深入讨论潜在地伦理风险（如医疗数据重构可能泄露隐私）。

（完）
