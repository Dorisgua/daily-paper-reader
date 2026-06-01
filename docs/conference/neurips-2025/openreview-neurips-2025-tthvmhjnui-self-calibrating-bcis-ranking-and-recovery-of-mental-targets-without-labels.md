---
title: "Self-Calibrating BCIs: Ranking and Recovery of Mental Targets Without Labels"
title_zh: 自校准脑机接口：无标签的心理目标排序与恢复
authors: "Jonathan Grizou, Carlos De la Torre-Ortiz, Tuukka Ruotsalo"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=TtHvmhjNui"
tags: ["query:eeg"]
score: 8.0
evidence: 无需标签的自校准脑机接口用于心理目标恢复
tldr: 从脑电图（EEG）中解码用户心中的目标（如人脸图像）通常需要标签数据。本文提出第一个无需标签的自校准框架CURSOR，通过配对EEG和图像数据学习恢复未知的心理目标，无需预训练解码器。实验表明，CURSOR预测的图像相似度评分与人类感知判断相关，并能有效恢复目标，为无标签脑机接口应用开辟了新途径。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
motivation: 现有心理目标恢复方法依赖标签数据，限制了实际应用。
method: 提出CURSOR算法，利用配对但无标签的EEG和图像数据，通过自校准学习恢复心理目标。
result: 在自然人脸图像实验中，CURSOR能预测与人类感知相关的相似度评分，并成功恢复目标。
conclusion: 首次实现无标签的脑机接口心理目标恢复，推动了自校准BCI的发展。
---

## Abstract
We consider the problem of recovering a mental target (e.g., an image of a face) that a participant has in mind from paired EEG (i.e., brain responses) and image (i.e., perceived faces) data collected during interactive sessions without access to labeled information. The problem has been previously explored with labeled data but not via self-calibration, where labeled data is unavailable. Here, we present the first framework and an algorithm, CURSOR, that learns to recover unknown mental targets without access to labeled data or pre-trained decoders. Our experiments on naturalistic images of faces demonstrate that CURSOR can (1) predict image similarity scores that correlate with human perceptual judgments without any label information, (2) use these scores to rank stimuli against an unknown mental target, and (3) generate new stimuli indistinguishable from the unknown mental target (validated via a user study, N=53). We release the brain response data set (N=29), associated face images used as stimuli data, and a codebase to initiate further research on this novel task.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）

- **问题**：传统脑机接口（BCI）从脑电图（EEG）解码用户心中的目标（如特定人脸图像）需要大量带标签的校准数据（例如已知目标对应的 EEG 响应），这限制了实际应用，尤其是对无法提供可靠反馈的用户（如严重运动障碍者）。
- **核心挑战**：在连续、高维的刺激空间（如图像的潜在嵌入空间）中，仅凭未标注的 EEG 响应和图像刺激对，自动恢复用户持有的心理目标（mental target），而不依赖任何预先训练的编码器或人工标注。
- **意义**：首次提出完全自校准（self-calibrating）的连续域 BCI 框架，称为 **CURSOR**，使系统仅通过交互过程的配对数据就能学会解码心理目标，显著降低校准门槛，有望扩展 BCI 在临床、人机交互等领域的可用性。

### 2. 论文提出的方法论：核心思想、关键技术细节、公式或算法流程

- **核心思想**：利用 EEG 响应与刺激在潜在空间距离之间的成对关系，通过构造假设目标并评估基于该假设的回归模型性能，推断真正的意图目标。关键假设：EEG 响应编码的是“观测刺激与心理目标之间的距离”，且该距离与潜在空间中的欧氏距离线性相关。
- **关键技术细节**：
  1. **相似性函数**：对于任意假设目标 \(h\)，定义 \( \rho_h(z_i) = \|h - z_i\|_2 \) 作为观测刺激 \(z_i\) 到 \(h\) 的距离。
  2. **构造假设数据集**：对每个假设 \(h\)，用 \( \rho_h \) 为每个刺激-响应对 \((z_i, e_i)\) 计算距离 \(d_i^h\)，得到数据集 \(\Gamma_h^N = \{(e_i, d_i^h)\}\)。
  3. **训练回归器**：在 \(\Gamma_h^N\) 上训练一个回归模型 \(f_{\theta_h}\) 从 EEG 响应预测距离。
  4. **计算误差比分数**：为了避免不同假设数据集分布差异的影响，定义 **CURSOR 分数** \(S(h) = \frac{RMSE(f_{\theta_{h,\sigma}}(e_\sigma), \rho_h(z))}{RMSE(f_{\theta_h}(e), \rho_h(z))}\)，其中分子是打乱了刺激-响应对后训练的模型误差（基线），分母是正常训练的模型误差。该比值越高，说明在该假设下 EEG 对距离的预测能力最强，即该假设越可能是真实目标。
  5. **优化与搜索**：在假设空间（潜在空间）上通过优化（如 CMA-ES）或对候选集排序来找到最大 \(S(h)\) 对应的 \(\hat{h}\)，即估计的心理目标。
- **算法流程**（Algorithm 1）：
  - 输入：刺激-响应数据集 \(\{(z_i, e_i)\}\)，假设 \(h\)，距离函数 \(\rho\)，回归器 \(f_\theta\)，误差函数 RMSE。
  - 输出：分数 \(S(h)\)。
  - 步骤：构造 \(\Gamma_h^N\) → 训练 \(f_{\theta_h}\) 计算 RMSE → 打乱数据训练 \(f_{\theta_{h,\sigma}}\) 计算 RMSE_shuffled → 返回比值。

### 3. 实验设计：数据集、基准、对比方法

- **数据集**：
  - **自采数据集**：31 名参与者（2 人因数据损坏剔除），每人观看 17 个目标人脸图像（GAN 生成，512 维潜在空间），使用 RSVP 范式，EEG 记录（32 通道，处理后为 29 通道 × 7 个时间窗 = 203 维特征）。共 9234 个刺激-响应对。
  - **模拟构建**：因原始数据包含不同目标，为统一评估，通过最小化距离匹配目标函数，为每个目标生成了 10 个等效数据集，共 170 个刺激-响应数据集（每个 9234 对）。
  - **假设集**：对每个目标，生成 60 个均匀采样距离的假设人脸（包含真实目标）。
- **基准与对比方法**：
  - **CURSOR 变体**：Linear Regression (LR), Support Vector Regression (SVR), Multi-Layer Perceptron (MLP)
  - **控制条件**：
    - Dummy：预测距离为均值，忽略 EEG。
    - Shuffled LR (S-LR)：训练前打乱刺激-响应配对，消除 EEG 信息。
    - 随机猜测：对 60 个候选，平均排名 30，期望距离 23.08。
- **评估任务**：
  - **排序任务**：对 60 个假设按 \(S(h)\) 排序，评估指标：分数与真实距离的 Pearson 相关（R）、真实目标排名、top-1 假设与真实目标的欧氏距离。
  - **优化任务**：在降低维度的潜在空间（EEG→20D，图像→10D，通过 PCA）使用 CMA-ES 优化寻找最大 \(S(h)\)，评估优化后图像与真实目标距离。
  - **人类验证**：H-Rank（无限时间排序相似度）、H-ID（短暂暴露下识别错误率，53 名参与者）。

### 4. 资源与算力

- 论文未明确提供详细的GPU型号、数量和训练时长。计算在本地（Linux/macOS 工作站）和本地 HPC 集群（AMD EPYC 7452 CPU）上运行，使用 SLURM 调度器。
- 资源消耗：每个估计器任务通常使用 1 个 CPU 核心，LR/MLP 最多 400 MB RAM、4 小时，SVR 最多 600 MB RAM、15 小时。实验以 embarrassingly parallel 方式执行。
- 未提及 GPU 加速，主要依赖 CPU。

### 5. 实验数量与充分性

- **实验数量充分**：
  - 排序实验：10 个数据集变体 × 17 个目标 × 多种数据规模（10 种 N 值）及多类估计器（LR, SVR, MLP, Dummy, S-LR），结果取 10 折交叉验证平均。
  - 优化实验：在降维空间进行 1000 次迭代，并进行了近目标数据剔除（ablation）以及相同规模均匀降采样对照。
  - 数据量影响实验：N 从 100 到 9234，以及距离阈值剔除（0 到 40）的影响。
  - 替代 EEG 表示：使用 EEGNet 嵌入重复部分实验。
  - 人类验证：两项用户研究（H-Rank 和 H-ID），共 53+ 参与者。
- **客观性与公平性**：
  - 控制条件（Dummy, S-LR）本质上仅作为随机基线，未使用任何真实标签，保证无标签信息泄露。
  - 对比方法均使用相同的数据划分和评估指标。
  - 超参数调优（BestMLP, BestSVR）在无标签情况下并不现实，因此主实验使用默认参数，但在附录中额外呈现了调优结果。
  - 充分考虑了数据量、近目标刺激、EEG 表示方式等消融实验，结果稳健。

### 6. 论文的主要结论与发现

- CURSOR 成功从无标签 EEG 响应中恢复心理目标（人脸图像）。
- **主要性能**：
  - LR 在排序任务上最佳：平均相关性 R=-0.77，目标平均排名 6.63/60，top-1 平均距离 2.9（人类几乎无法区分：H-ID 在 d≤1.6 时错误率约 50%）。
  - 优化任务：LR 找到的图像平均距离仅为 0.93（几乎与目标无差异），而控制条件（S-LR/Dummy）距离约 22-24（明显可辨）。
  - 即使移除了距离目标 10 以内的刺激，CURSOR 仍能恢复到距离＜5 的目标，展示了超越观测范围的推断能力。
- **标签恢复**：优化后，可用估计目标重建所有刺激的标签，RMSE 仅 0.18（对比监督基线 0.17），说明自校准效果与监督校准接近。
- **人类验证**：CURSOR 的分数与人类相似度评分高度相关（R=-0.97），人类在短暂曝光下对 top-1 图片无法有效分辨。

### 7. 优点

1. **方法创新性**：首次在连续域实现完全自校准 BCI，无需任何标签或预训练，突破离散分类限制。
2. **算法设计巧妙**：通过构造假设数据集并计算相对 RMSE 比，有效处理了不同假设下距离分布差异，避免绝对误差的偏差，仅需无标签配对数据。
3. **实验严谨**：包含大量消融实验（数据量、近邻刺激、EEG 表示、超参数调优）、两种控制条件、人类行为验证，结论可靠。
4. **数据集贡献**：公开首个适合连续域自校准 BCI 研究的大规模 EEG-人脸配对数据集（9234 对），并开放代码，促进后续研究。
5. **可扩展性**：框架不依赖特定回归器或 EEG 表示，可使用任意回归模型和 EEG 特征，有潜力推广到其他连续刺激域（如声音、文字）。

### 8. 不足与局限

1. **刺激空间受限**：仅使用单一预训练 GAN 生成的人脸图像，未验证在真实人脸或其他类别（物体、场景）上的泛化能力。
2. **距离函数假设**：假设潜在空间欧氏距离与感知相似度线性相关，该假设可能不适用于更复杂的视觉范畴。
3. **采集协议偏差**：刺激采样采用对数间隔（靠近目标更密集），引入偏向性；虽然进行了移除近邻刺激的消融实验，但在线动态采样场景下仍需进一步验证。
4. **降维依赖**：优化任务使用了 PCA 降维（20D EEG + 10D 图像），降维比例选择依赖外部相关性指标，在完全无监督场景下可能不可用。
5. **缺少在线闭环验证**：所有评估为离线（post-hoc），未进行实时、交互式的在线实验，系统在实际延迟、疲劳效应下的表现未知。
6. **跨个体泛化未测试**：实验集中于个体内数据分析，未探索跨被试迁移（如利用先前参与者的数据加速新用户校准）。
7. **计算效率**：每次评估假设分数需训练回归器，搜索空间大时计算开销较高，未探索主动采样或贝叶斯优化加速。
8. **伦理风险**：虽讨论了隐私风险并建议保障措施，但实际部署中知情同意、数据最小化等机制仍需进一步研究和规范。

（完）
