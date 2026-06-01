---
title: Neighbour-Driven Gaussian Process Variational Autoencoders for Scalable Structured Latent Modelling
title_zh: 基于邻居驱动的高斯过程变分自编码器可实现可扩展的结构化潜变量建模
authors: "Xinxing Shi, Xiaoyu Jiang, Mauricio A Álvarez"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=XlRIub1r5s"
tags: ["query:eeg-latent"]
score: 6.0
evidence: 可扩展的结构化潜变量建模，采用高斯过程变分自编码器
tldr: 本文针对高斯过程变分自编码器（GPVAE）在大规模数据上计算昂贵的问题，提出基于最近邻的近似推理策略，在保持潜变量依赖性的同时实现扩展。该方法允许更灵活的内核选择，在多个合成和真实数据集上提升了潜空间建模的效率和准确性。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-xlriub1r5s/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 868, \"height\": 391, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-xlriub1r5s/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 821, \"height\": 505, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-xlriub1r5s/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 846, \"height\": 500, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-xlriub1r5s/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1755, \"height\": 476, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-xlriub1r5s/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 857, \"height\": 509, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-xlriub1r5s/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 821, \"height\": 485, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-xlriub1r5s/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1757, \"height\": 527, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-xlriub1r5s/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1709, \"height\": 569, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-xlriub1r5s/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1763, \"height\": 1299, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-xlriub1r5s/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 710, \"height\": 702, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-xlriub1r5s/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1767, \"height\": 885, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-xlriub1r5s/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1757, \"height\": 1907, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-xlriub1r5s/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1743, \"height\": 752, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xlriub1r5s/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1531, \"height\": 336, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xlriub1r5s/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1522, \"height\": 470, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xlriub1r5s/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1163, \"height\": 702, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xlriub1r5s/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1051, \"height\": 491, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xlriub1r5s/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1534, \"height\": 186, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xlriub1r5s/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1557, \"height\": 577, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xlriub1r5s/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1459, \"height\": 661, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xlriub1r5s/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1235, \"height\": 295, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xlriub1r5s/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 888, \"height\": 449, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xlriub1r5s/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1215, \"height\": 292, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xlriub1r5s/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1170, \"height\": 637, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xlriub1r5s/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1410, \"height\": 450, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xlriub1r5s/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 990, \"height\": 450, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-xlriub1r5s/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1695, \"height\": 599, \"label\": \"Table\"}]"
motivation: GPVAE在大规模数据上推理复杂，现有方法依赖限制性假设。
method: 利用潜空间中的局部邻接关系，仅对每个数据点的最近邻进行GP计算。
result: 在保持潜变量依赖的同时显著降低计算成本，支持灵活核函数。
conclusion: 为大规模结构化潜变量建模提供了高效的近似方法。
---

## Abstract
Gaussian Process (GP) Variational Autoencoders (VAEs) extend standard VAEs by replacing the fully factorised Gaussian prior with a GP prior, thereby capturing richer correlations among latent variables. However, performing exact GP inference in large-scale GPVAEs is computationally prohibitive, often forcing existing approaches to rely on restrictive kernel assumptions or large sets of inducing points. In this work, we propose a neighbour-driven approximation strategy that exploits local adjacencies in the latent space to achieve scalable GPVAE inference. By confining computations to the nearest neighbours of each data point, our method preserves essential latent dependencies, allowing more flexible kernel choices and mitigating the need for numerous inducing points. Through extensive experiments on tasks including representation learning, data imputation, and conditional generation, we demonstrate that our approach outperforms other GPVAE variants in both predictive performance and computational efficiency.

---

## 论文详细总结（自动生成）

# 基于邻居驱动的高斯过程变分自编码器（Neighbour-Driven GPVAEs）——论文中文详细总结

## 1. 核心问题与整体含义（研究动机与背景）

标准变分自编码器（VAE）假设潜变量服从全因子化高斯先验，这无法刻画序列、空间等结构化数据中潜变量之间的相关性。高斯过程变分自编码器（GPVAE）用高斯过程（GP）先验替代全因子化高斯先验，从而能够建模更丰富的潜变量依赖关系。然而，精确 GP 推理的计算复杂度为 \(O(N^3)\)（\(N\) 为训练样本数），在大规模数据上不可行。现有方案要么依赖特定的核结构（如低秩核、Matern 族），要么使用大量诱导点（inducing points）来近似 GP 后验，但这些方法在核选择上受限，或在数据变化剧烈时需要很多诱导点，且优化困难。为此，本文提出一种**邻居驱动（neighbour-driven）的近似策略**，利用潜空间中的局部邻接性质——即每个数据点仅与少量最近邻（nearest neighbours）发生主要相关——来大幅降低计算负担，同时保留关键的结构化依赖。这一思想受“第一地理定律”和最近邻高斯过程（NNGP）的启发。作者提出了两种具体的近似方案：**分层先验近似（HPA）** 和**稀疏精度近似（SPA）**，使得 GPVAE 可以在小批量（mini-batch）下高效训练，并支持任意核函数，无需大量诱导点。

## 2. 方法论

### 2.1 核心思想
利用数据点辅助信息（如时间戳、空间坐标）的局部邻域，将全 GP 先验的稠密协方差矩阵或精度矩阵稀疏化，使得每个潜变量只与其最近的 \(H\) 个邻居相关。这样，KL 散度项和预测后验的计算只涉及维度为 \(H \times H\) 的小矩阵，从而将复杂度从 \(O(N^3)\) 降至 \(O(N_b H^3)\)（\(N_b\) 为 mini-batch 大小）。

### 2.2 两种近似技术

#### (1) 分层先验近似（Hierarchical Prior Approximation, HPA）
- 引入一个二进制指示向量 \(w \in \{0,1\}^N\)，表示哪些潜变量被“激活”。
- 先验定义为 \(p(Z|w) = \mathcal{N}(Z | 0, D_w K_{XX} D_w)\)，其中 \(D_w = \text{diag}(w)\)。未激活的变量间相关性被切断。
- 变分分布同样采用类似形式：\(q(Z|w) = \mathcal{N}(Z | D_w \mu(Y), D_w \sigma^2(Y) D_w)\)。
- 在训练时，对每个小批量中的样本 \((x_i, y_i)\)，选取其 \(H\) 个最近邻（按辅助信息），对应 \(w\) 中仅这些位置为1。ELBO 近似为：
  \[
  \mathcal{L}_{\text{HPA}} \approx \frac{N}{|I|} \sum_{i\in I} \mathbb{E}_{q(z_i|y_i)}[\log p(y_i|z_i)] - \frac{1}{N} \text{KL}[q(Z_{n(i)}) \| p(Z_{n(i)})]
  \]
  其中 \(Z_{n(i)}\) 是邻居子集。KL 项仅涉及 \(H \times H\) 协方差矩阵。

#### (2) 稀疏精度近似（Sparse Precision Approximation, SPA）
- 将联合分布 \(p(Z)\) 按概率链式法则分解，并假设每个变量仅依赖于其前序的 \(H\) 个最近邻（按辅助信息的顺序）：
  \[
  p(Z) \approx p(z_1) \prod_{j=2}^N p(z_j | z_{n(j)})
  \]
  其中 \(n(j)\) 是 \(x_j\) 在 \(\{x_h\}_{h<j}\) 中的 \(H\) 个最近邻索引。
- 使用标准变分分布 \(q(Z|Y) = \prod_n \mathcal{N}(z_n | \mu_\phi(y_n), \sigma^2_\phi(y_n))\)，得到 ELBO：
  \[
  \mathcal{L}_{\text{SPA}} = \sum_i \mathbb{E}_{q(z_i|y_i)}[\log p(y_i|z_i)] - \sum_j \mathbb{E}_{q(Z_{n(j)})} \text{KL}[q(z_j) \| p(z_j | Z_{n(j)})]
  \]
  可通过对 \(I\) 和 \(J\) 抽样进行 mini-batch 估计。

### 2.3 预测后验
对于新位置 \(x_*\)，仅需考虑其 \(H\) 个最近邻 \(n(*)\)，先求 \(q(z_*|Y) = \int p(z_*|Z_{n(*)}) q(Z_{n(*)}|Y) d Z_{n(*)}\)，再通过 decoder 获得 \(y_*\) 的分布。

### 2.4 计算复杂度
- 最近邻搜索：可使用 Faiss 库加速，最坏情况 \(O(HN)\)。
- KL 项中的 Cholesky 分解：\(O(N_b H^3)\)，其中 \(N_b\) 为 mini-batch 大小，\(H\) 为邻居数。
- 与全 GP 的 \(O(N^3)\) 相比大幅降低，且无需大量诱导点或限制性核。

## 3. 实验设计

论文在**四个主要场景**上进行了评估，涵盖合成与真实数据：

### 3.1 Moving Ball（潜变量轨迹重构）
- **数据**：30帧黑白视频，球轨迹由 RBF 核 GP 生成；每批35个视频。
- **任务**：从像素帧推断球的位置（潜变量均值轨迹）。
- **基线**：VAE、GPVAE-Casale（全GP）、GPVAE-Pearce（全GP）、SVGPVAE。
- **指标**：RMSE。
- **主要发现**：本文方法（HPA/SPA）用很少的邻居（如H=10）即可接近全GP性能，而SVGPVAE需要更多诱导点。

### 3.2 Rotated MNIST（缺失帧插值与生成）
- **版本1（缺失像素插值）**：10帧序列，60%像素随机缺失。数据集50k/10k序列。
- **版本2（缺失帧生成）**：100帧序列，60%帧随机缺失。数据集4k/1k序列。
- **基线**：VAE、HI-VAE、GPVAE-Diag、GPVAE-Band、MGPVAE、SVGPVAE、LVAE。
- **指标**：NLL、RMSE、训练时间（s/epoch）。
- **结果**：本文方法在NLL和RMSE上优于或接近全GP/诱导点方法，且训练时间与SVGPVAE相当或更短。

### 3.3 MuJoCo Hopper Physics（条件生成）
- **数据**：500个14维序列，每个1000时间步，60%时间点完全缺失。320/80/100划分。
- **基线**：SVGPVAE、MGPVAE。
- **指标**：NLL、RMSE、训练时间。
- **结果**：本文方法（尤其HPA）在NLL和RMSE上显著优于基线，训练时间更短。

### 3.4 地统计学数据集（空间插值）
- **Jura**：359个地点，三维输出（Ni、Zn、Cd），缺失Cd的任务。
- **SPE10**：约14万数据点（3D网格），四维输出（孔隙度、渗透率等），50%值随机缺失。
- **基线**：Exact GP、VNNGP、VAE、HI-VAE、SVGPVAE、SGPBAE、MOGP等。
- **结果**：本文方法在RMSE和NLL上全面优于诱导点方法（如SVGPVAE、SGPBAE），且与VNNGP相当但参数更少。对SPE10这样高度异质的大数据，邻居驱动方法明显优于诱导点方法。

**实验充分性**：每个实验均报告10次随机试验的均值和标准差；包含了不同H值（3,5,7,10,15,20等）的消融；与多种代表性基线对比；覆盖了低维到高维、小样本到十万样本的场景。实验设计较为客观公平。

## 4. 资源与算力

论文中明确提及：
- **GPU 型号**：NVIDIA A100-SXM4 或 V100-SXM2（高性能集群），部分训练时间估计使用 NVIDIA RTX-4090，缺失像素插值任务使用 RTX-2080-Ti（软件兼容性原因）。
- **训练时间**：各实验表格给出了每 epoch 的秒数（s/epoch），例如 Moving ball 未具体给出但其他任务中训练时间在几秒到几十秒之间。
- **框架**：PyTorch + GPyTorch + Faiss（最近邻搜索）。
- **未给出**：未明确说明总训练时长（epoch 数×s/epoch）、使用的 GPU 数量（推测单卡即可）。整体算力需求适中，适合单个 GPU 运行。

## 5. 实验数量与充分性

总共进行了**4大类实验**，至少包含：
- Moving ball：3种基线 + 本文2种变体，不同H值（5个档次）。
- Rotated MNIST 像素插值：6种基线 + 本文2种变体（H=5）。
- Rotated MNIST 帧生成：4种基线 + 本文2种变体（H=10，另附H=5,20在附录）。
- MuJoCo：2种基线 + 本文2种变体（H=5,10,20）。
- Jura：8种基线 + 本文2种变体。
- SPE10：6种基线 + 本文2种变体（H=20）。

此外附录中还有额外的可视化与消融实验。每组实验报告多次试验的统计量。可以认为实验数量充分，对比全面，结果可靠。但缺少更多高级核（如周期核、非平稳核）的验证，也未探索不同距离度量。

## 6. 主要结论与发现

1. **邻居驱动近似有效替代诱导点方法**：在多个任务中，本文的 HPA/SPA 用较少的最近邻即可达到甚至超越使用大量诱导点的 SVGPVAE 和 SGPBAE。
2. **支持任意核，无限制性假设**：因为只依赖局部协方差，可灵活选用 RBF、Matern、Cauchy 等内核。
3. **在大型高异质数据上表现突出**：SPE10 实验证明邻居驱动方法比诱导点方法更能捕捉局部快速变化，且参数更少。
4. **训练效率高**：每 epoch 时间与 SVGPVAE 相当，但性能显著提升；对于长序列，避免了 MGPVAE 的串行计算瓶颈。
5. **两种变体各有优势**：在多数任务中 SPA 略优于 HPA，但 HPA 在某些任务表现更稳定（如 MuJoCo NLL）。

## 7. 优点

- **方法简洁、可扩展**：核心思想直观（利用局部性），无需复杂推理，易于实现。
- **兼容小批量训练**：使得 GPVAE 可应用于大规模数据。
- **核选择不受限**：对比许多之前的工作（如 Casale 2018 的低秩核、Zhu 2023 的 Matern SDE），本文支持任意静止核或非静止核。
- **实验全面且有说服力**：覆盖了多种类型数据（合成、图像、物理模拟、地学），指标包含 NLL、RMSE、训练时间，并进行统计重复。
- **开源实现**：代码已公开，可复现。

## 8. 不足与局限

- **距离度量单一**：仅使用欧氏距离，未探索相关性距离或流形感知距离（如 Kang & Katzfuss 2023），在高维复杂空间中可能不是最优。
- **邻居数 H 固定**：未提出自适应选择 H 的机制，实际应用需手动调参。
- **未验证非静止核或深度学习核**：虽理论上支持，但实验未涉及。
- **对顺序敏感（SPA）**：SPA 基于某种顺序（如时间顺序），不同顺序可能影响性能，论文未讨论顺序选择策略。
- **在极大规模（>百万）数据上的表现未知**：最大实验为 14 万点，未测试更大规模。
- **未与最新非线性降维/状态空间模型对比**：如 ODE-RNN、Neural ODE 等处理不规则时间序列的方法未被纳入。

综上，该工作为结构化潜变量建模提供了高效、实用的近似推理方案，在多个基准上验证了优势，但仍有若干可改进方向。

（完）
