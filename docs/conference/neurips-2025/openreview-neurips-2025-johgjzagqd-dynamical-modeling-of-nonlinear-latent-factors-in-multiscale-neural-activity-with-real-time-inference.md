---
title: Dynamical modeling of nonlinear latent factors in multiscale neural activity with real-time inference
title_zh: 多尺度神经活动中非线性潜在因子的动力学建模与实时推理
authors: "Eray Erturk, Maryam M. Shanechi"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=jOHgjZaGqd"
tags: ["query:eeg-latent"]
score: 9.0
evidence: 非线性潜在因子建模与缺失数据处理
tldr: 多模态神经活动分析面临不同采样率和缺失样本的挑战，现有非线性模型未解决这些问题。本文提出一种学习框架，能够对多模态神经时间序列（如发放和场电位）进行非线性潜在因子建模，并支持实时递归解码。该框架显式处理不同时间尺度和缺失数据，在仿真和真实数据上展示了有效性和实时推理能力，为脑机接口和神经科学应用提供了可实用的解码方法。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-johgjzagqd/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1456, \"height\": 495, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-johgjzagqd/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 840, \"height\": 371, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-johgjzagqd/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1399, \"height\": 639, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-johgjzagqd/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1460, \"height\": 632, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-johgjzagqd/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1455, \"height\": 1100, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-johgjzagqd/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1449, \"height\": 1020, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-johgjzagqd/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 961, \"height\": 883, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-johgjzagqd/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 975, \"height\": 874, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-johgjzagqd/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1176, \"height\": 517, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-johgjzagqd/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1415, \"height\": 286, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-johgjzagqd/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1448, \"height\": 170, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-johgjzagqd/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1438, \"height\": 141, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-johgjzagqd/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1454, \"height\": 169, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-johgjzagqd/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1449, \"height\": 167, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-johgjzagqd/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1455, \"height\": 173, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-johgjzagqd/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1419, \"height\": 265, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-johgjzagqd/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 760, \"height\": 305, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-johgjzagqd/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1256, \"height\": 309, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-johgjzagqd/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1257, \"height\": 259, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-johgjzagqd/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 509, \"height\": 303, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-johgjzagqd/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 682, \"height\": 464, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-johgjzagqd/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 757, \"height\": 221, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-johgjzagqd/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 848, \"height\": 431, \"label\": \"Table\"}]"
motivation: 多模态神经数据存在不同采样率和缺失样本，现有非线性模型无法处理这些问题。
method: 提出一个学习框架，对多模态神经时间序列进行非线性潜在因子建模，支持实时递归解码并处理缺失数据。
result: 在仿真和真实数据上验证了模型能有效处理不同时间尺度和缺失样本，实现实时解码。
conclusion: 提供了一种通用的多模态神经数据实时解码方法，可应用于脑机接口等领域。
---

## Abstract
Real-time decoding of target variables from multiple simultaneously recorded neural time-series modalities, such as discrete spiking activity and continuous field potentials, is important across various neuroscience applications. However, a major challenge for doing so is that different neural modalities can have different timescales (i.e., sampling rates) and different probabilistic distributions, or can even be missing at some time-steps. Existing nonlinear models of multimodal neural activity do not address different timescales or missing samples across modalities. Further, some of these models do not allow for real-time decoding. Here, we develop a learning framework that can enable real-time recursive decoding while nonlinearly aggregating information across multiple modalities with different timescales and distributions and with missing samples. This framework consists of 1) a multiscale encoder that nonlinearly aggregates information after learning within-modality dynamics to handle different timescales and missing samples in real time, 2) a multiscale dynamical backbone that extracts multimodal temporal dynamics and enables real-time recursive decoding, and 3) modality-specific decoders to account for different probabilistic distributions across modalities. In both simulations and three distinct multiscale brain datasets, we show that our model can aggregate information across modalities with different timescales and distributions and missing samples to improve real-time target decoding. Further, our method outperforms various linear and nonlinear multimodal benchmarks in doing so.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

多模态神经活动记录（如离散的神经发放信号 spiking activity 和连续的场电位 local field potentials, LFP）能够提供不同时空尺度的脑活动信息，对于下游解码（如运动意图、视觉刺激等）具有重要意义。然而，现有非线性动力学模型存在三个关键挑战：

- **不同时间尺度（采样率）**：spikes 通常以毫秒级采样（如10 ms），而 LFP 采样率可能更低（如50 ms），导致模态间时间不对齐。
- **不同概率分布**：spikes 常被建模为 Poisson 过程（离散计数），LFP 多为 Gaussian 分布（连续值）。
- **缺失样本**：由于记录设备差异、信号丢失或时间不对齐，某些时间步下某一模态可能完全缺失。

现有非线性多模态模型（如 mmPLRNN、MMGPVAE）既未支持不同时间尺度，也未考虑缺失样本，且部分模型无法实时（因果）推理。线性多尺度模型（如 MSID）虽能处理时间尺度，但缺乏非线性表达能力。

**本文贡献**：提出 MRINE（Multiscale Real-time Inference of Nonlinear Embeddings）框架，能够对多模态神经时间序列进行非线性动力学建模，同时支持实时递归解码、不同时间尺度、不同概率分布以及缺失样本下的鲁棒融合。

## 2. 方法论：核心思想、关键技术细节

### 核心思想
将多模态观测通过一个**多尺度编码器**非线性融合为统一的嵌入因子 `a_t`，再通过**多尺度线性动力学模型（LDM）** 提取潜在因子 `x_t`，最后通过模态特定解码器重建观测。整个模型支持实时（滤波）和非因果（平滑）推理。

### 关键技术细节

- **生成模型**：
  - 潜在动力学：`x_{t+1} = A x_t + w_t`（线性状态空间模型）
  - 嵌入因子：`a_t = C x_t + r_t`
  - 观测模型：
    - Spikes：`s_t ~ Poisson(λ(a_t))`，其中 `λ = f_{θs}(a_t)`
    - LFP：`y_{t'} ~ N(μ(a_{t'}), σ)`，其中 `μ = f_{θy}(a_{t'})`

- **多尺度编码器（图1b）**：
  - 每个模态首先通过时间不变的 MLP 提取模态特定嵌入因子 `a_s^t` 和 `a_y^t`。
  - 通过**模态特定 LDM**（公式6-7）对每个模态独立进行卡尔曼滤波，得到实时滤波估计 `a_{s,t|t}` 和 `a_{y,t|t}`。若某模态在当前时间步缺失，则利用其动力学模型进行一步前向预测（如 `a_{y,t|t} = A_y a_{y,t-1|t-1}`）。
  - 将滤波后的模态嵌入拼接，再通过融合网络 `φ_m` 得到多尺度嵌入 `a_t`。

- **推理与解码**：
  - 多尺度 LDM（公式1-2）使用卡尔曼滤波实现实时推理（`x_{t|t}`），或使用卡尔曼平滑实现非因果推理（`x_{t|T}`）。
  - 目标变量（如运动速度）通过线性回归从潜在因子解码。

- **训练目标**：
  - `L_k`：多步前向预测损失（k-step ahead prediction）
  - `L_smooth`：平滑重建损失（使用 `x_{t|T}` 重建观测）
  - `L_sm`：**平滑正则化**（KL 散度惩罚相邻时间步之间的分布差异），分别施加于 spiking、LFP 和潜在因子 `x_t` 上，防止学习平凡变换。
  - 额外使用 L2 正则化和 **time-dropout**（训练时随机丢弃时间步掩码，提高对缺失样本的鲁棒性）。

## 3. 实验设计

### 数据集
- **随机 Lorenz 吸引子仿真**：生成三维非线性动力学，分别映射为 Poisson 和 Gaussian 观测（5/10/20 通道），测试潜在重建精度（CC）。
- **NHP 网格到达数据集**：猴子控制光标进行二维网格到达，记录多单元发放（10 ms）和 LFP（50 ms 与 10 ms 两种设置），解码二维光标速度。
- **NHP 中心外出到达数据集**：猴子进行中心-外围到达任务，记录发放和 LFP 功率信号，解码二维操纵杆速度。
- **视觉刺激数据集**（Allen Institute）：高维（800-D）神经像素发放（120 Hz）和钙成像（30 Hz）数据，进行帧ID解码。

### 对比的基准方法
- 单尺度模型（仅 spike 或仅 LFP）
- **MSID**（线性多尺度子空间辨识）
- **mmPLRNN**（非线性多模态分段线性 RNN）
- **MMGPVAE**（多模态高斯过程 VAE）
- **MVAE**（多模态 VAE）
- **CEBRA**（对比学习）
- **LFADS**（单模态序列自编码器，用于消融比较）

### 评估指标
- 行为解码：皮尔逊相关系数（CC）或 R²
- 神经重建：spikes 用 AUC-ROC，LFP 用 CC
- 缺失样本鲁棒性：在不同样本丢弃概率下测试

### 实验条件
- 对每个数据集采用 5 折交叉验证，多次重复（不同随机种子或 session）。
- 统计显著性使用单侧 Wilcoxon 符号秩检验。

## 4. 资源与算力

论文在附录 A.3 提到推理时间（使用 Intel i7-10700K），但**未明确说明训练所用的 GPU 型号、数量或训练时长**。文中仅说明模型在 CPU 服务器（AMD Epyc 7513/7542, 2.90 GHz, 32 核）上训练，并使用并行化。因此，算力细节不够充分，读者难以复现或评估训练成本。

## 5. 实验数量与充分性

- **总体实验量**：涵盖 1 个仿真 + 3 个真实数据集，每个数据集包含多种通道组合（5/10/20/30/60）、两种时间尺度设置（相同/不同）、缺失样本概率变化（0.2~0.8）、多种基准对比。
- **消融实验**：
  - 时间 dropout 的影响（附录 A.6.1）
  - 损失项（平滑正则化、平滑重建）的贡献（附录 A.6.2）
  - 不同观测模型（附录 A.6.3）
  - 多尺度编码器与零填充对比（附录 A.6.4）
- **公平性**：所有方法在同一超参数搜索范围内优化，使用相同的训练/测试划分。但对某些基准方法（如 mmPLRNN、MMGPVAE）在缺失样本下使用了零填充，而 MRINE 使用自身多尺度编码器，条件不完全对等（但正是 MRINE 的优势所在）。统计检验合理。
- **充分性**：实验覆盖了多种信息丰富度和缺失场景，但高通道（30/60）只在 NHP 网格数据集上测试，未在另两个数据集上验证泛化性。

## 6. 论文的主要结论与发现

1. **MRINE 能有效融合不同时间尺度和缺失的多模态神经数据**，在行为解码和神经重建上显著优于单尺度模型和所有对比的线性/非线性多模态基准。
2. **双向信息融合均有提升**：无论以 spike 还是 LFP 为主要模态，添加另一模态均能提高解码性能，说明两类信号包含非冗余信息。
3. **对缺失样本高度鲁棒**：在高达 80% 样本丢失的情况下，MRINE 的性能下降最小，优于所有基线。
4. **多尺度编码器设计是关键**：相比于直接零填充，MRINE 的模态特定 LDM 能更好地利用动力学预测缺失值，避免输入失真。
5. **平滑正则化和多步预测损失** 对性能提升有重要贡献（消融实验证实）。
6. **MRINE 同样适用于同时间尺度场景**，并在该场景下与最佳基线（MMGPVAE）水平相当或略优，但支持实时推理。

## 7. 优点

- **创新性**：首次在非线性多模态神经动力学建模中同时解决时间尺度差异、缺失样本和实时推断问题。
- **实用性**：推理速度（~1.82 ms/时间步）满足实时 BCI 需求；支持因果与非因果两种推理模式。
- **架构设计巧妙**：模态特定 LDM + 卡尔曼滤波天然处理缺失；时间 dropout 增强鲁棒性；平滑正则化防止退化解。
- **实验全面**：在多个真实神经数据集上验证，并与多种先进基准对比，消融实验完整。
- **可复现性**：代码已开源，超参数和训练细节在附录中详细给出。

## 8. 不足与局限

- **动力学时不变假设**：MRINE 假设潜在动力学参数（A, C, W, R）随时间不变，无法跟踪非平稳变化（如电极退化、精神状态变化）。作者提及未来可扩展到切换动力学或自适应方法。
- **超参数调参复杂**：引入了多个缩放超参数（γ_s, γ_y, γ_x 等），需要手动搜索，可能影响易用性。
- **未探索跨模态生成**：MRINE 未尝试直接从一种模态生成另一种完全缺失的模态，而该能力在某些场景下有意义。
- **未包含外部输入**：不能区分输入驱动动力学与内在动力学（如行为协变量），限制了因果解释性。
- **算力开销未报告**：缺少训练所需 GPU/CPU 时间和资源明细，不利于读者评估复现成本。此外，大多数实验采用 CPU 训练，对于更大规模数据可能效率不足。

（完）
