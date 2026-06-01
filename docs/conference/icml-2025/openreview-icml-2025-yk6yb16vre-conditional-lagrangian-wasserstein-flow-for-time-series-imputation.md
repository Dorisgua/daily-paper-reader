---
title: Conditional Lagrangian Wasserstein Flow for Time Series Imputation
title_zh: 条件拉格朗日Wasserstein流用于时间序列插补
authors: "Weizhu Qian, Dalin Zhang, Yan Zhao, Yunyao Cheng"
date: 2025-01-09
pdf: "https://openreview.net/pdf?id=yK6yb16vRe"
tags: ["query:eeg-latent"]
score: 6.0
evidence: 时间序列插补方法，使用拉格朗日 Wasserstein 流和去噪自编码器
tldr: 针对扩散模型插补方法收敛慢的问题，本文提出条件拉格朗日Wasserstein流（CLWF），基于最小作用量原理学习速度场，并集成去噪自编码器减小采样方差。实验显示CLWF在多个基准数据集上达到竞争性能，为时间序列插补提供了高效方案。
source: ICML-2025-Rejected-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-yk6yb16vre/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1318, \"height\": 554, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yk6yb16vre/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1744, \"height\": 453, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yk6yb16vre/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1199, \"height\": 816, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-yk6yb16vre/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1286, \"height\": 562, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-yk6yb16vre/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 868, \"height\": 580, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yk6yb16vre/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 874, \"height\": 745, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yk6yb16vre/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 887, \"height\": 319, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yk6yb16vre/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 886, \"height\": 321, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yk6yb16vre/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 886, \"height\": 210, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yk6yb16vre/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 883, \"height\": 202, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yk6yb16vre/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 889, \"height\": 373, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yk6yb16vre/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1761, \"height\": 217, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yk6yb16vre/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1761, \"height\": 235, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yk6yb16vre/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1717, \"height\": 235, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yk6yb16vre/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1761, \"height\": 311, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-yk6yb16vre/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1412, \"height\": 147, \"label\": \"Table\"}]"
motivation: 扩散模型插补方法推理收敛慢，需要更高效的插补方案。
method: 基于拉格朗日力学最小作用量原理学习速度，结合时间相关去噪自编码器估计势函数梯度。
result: 在时间序列插补任务上取得竞争性性能，优于现有扩散模型方法。
conclusion: CLWF为时间序列插补提供了新的高效框架，可推广至EEG等多变量序列。
---

## Abstract
Time series imputation is important for numerous real-world applications. To overcome the limitations of diffusion model-based imputation methods, e.g., slow convergence in inference, we propose a novel method for time series imputation in this work, called Conditional Lagrangian Wasserstein Flow (CLWF). Following the principle of least action in Lagrangian mechanics, we learn the velocity by minimizing the corresponding kinetic energy. Moreover, to enhance the model's performance, we estimate the gradient of a task-specific potential function using a time-dependent denoising autoencoder and integrate it into the base estimator to reduce the sampling variance. Finally, the proposed method demonstrates competitive performance compared to other state-of-the-art imputation approaches.

---

## 论文详细总结（自动生成）

# 论文总结：Conditional Lagrangian Wasserstein Flow for Time Series Imputation

## 1. 核心问题与整体含义（研究动机与背景）
- **研究动机**：时间序列插补（imputation）在交通、环境、医疗等众多实际应用中至关重要。深度学习（RNN、VAE、GAN）已展现优势，但近期流行的扩散模型（如DDPM、SBGM）虽然在建模能力上突出，却存在推理收敛慢、计算成本高的严重瓶颈，限制了其实时或大规模部署。
- **整体含义**：本文提出一种全新的条件生成框架——**条件拉格朗日Wasserstein流（CLWF）**，结合最优传输理论与拉格朗日力学，在保证生成质量的同时大幅加速推理，为时间序列插补提供快速、准确的替代方案。

## 2. 方法论
### 2.1 核心思想
- 将多变量时间序列插补视为**条件最优传输问题**：源分布（随机噪声）→ 目标分布（缺失数据），观测数据作为条件。
- 遵循拉格朗日力学中**最小作用量原理**，学习将源分布移动到目标分布的最优速度场（velocity field），最小化动能。
- 通过**时变去噪自编码器（TDAE）** 估计任务特定势函数（potential function）的梯度，将其集成到基础估计器中，降低采样方差（Rao-Blackwellization）。

### 2.2 关键技术细节
1. **Wasserstein空间插值**：
   - 首先通过小批量最优传输（mini-batch OT）将源和目标分布投影到Wasserstein空间。
   - 构造时变中间样本：  
     \( X_t = \frac{t}{T}(X_T + \gamma_t) + (1-\frac{t}{T})X_0 + \alpha(t)\sqrt{\frac{t(T-t)}{T}}\epsilon \)，其中\(\gamma_t\)为注入噪声，\(\alpha(t)\)为时变标量。
2. **速度估计（Flow Matching）**：
   - 变分速度函数\(\mu_\theta(x_t^{\text{in}}, t)\)通过最小化流动匹配损失学习：  
     \(\min_\theta \mathbb{E}\left[ \left\| \frac{x_t^{\text{tar}} - x_0}{T} - \mu_\theta(x_t^{\text{in}}, t) \right\|_2^2 \right]\)
   - 此损失等价于最小化拉格朗日动能，且无需轨迹模拟（仿真自由）。
3. **势函数梯度整合**：
   - 假设势函数\(U_t(X_t) \approx -\log \mathcal{N}(X_t|\hat{X}_t, \sigma_p^2)\)，导数\(\nabla_x U_t = \frac{X_t - \hat{X}_t}{\sigma_p^2}\)。
   - 用TDAE预测\(\hat{X}_t\)，得到控制信号\(v_{\phi,t}(X_t,t) = -s\frac{X_t - \text{TDAE}(X_t)}{\sigma_p^2}\)，其中\(s = s_0 t(T-t)/T\)。
4. **重采样技巧**：
   - 推理时，通过插值条件区域和生成区域，将观测数据缝合进生成的中间样本，进一步提升插补质量。

### 2.3 算法流程
- **训练**：
  1. 抽样时间\(t\)、初始噪声\(x_0\)和目标数据\(x_T\)。
  2. 可选：计算小批量OT映射。
  3. 根据插值公式生成\(x_t\)。
  4. 最小化流动匹配损失更新\(\theta\)。
  5. 基于观测数据训练TDAE（预训练或联合训练）获得梯度估计\(\phi\)。
- **推理（采样）**：
  1. 初始噪声\(x_0 \sim \mathcal{N}(0,\sigma_0^2)\)，条件数据\(x_{\text{cond}}\)。
  2. 迭代\(N\)步：输入\(x_t^{\text{in}} = \text{concat}(x_{\text{cond}}, \hat{x}_t)\)，用\(\mu_\theta\)更新\(\hat{x}_{t+1}\)。
  3. 可选：添加势函数梯度修正（Rao-Blackwellization）。
  4. 可选：应用重采样缝合观测区域。

## 3. 实验设计
### 3.1 数据集
- **合成数据**：\(x = t \sin(10t + 2\pi\epsilon)\)，缺失率0.4/0.6/0.8。
- **PM2.5**：空气质量数据，特征36，序列长度36，原始缺失13%。
- **PhysioNet**：ICU数据，特征35，序列长度48，原始缺失80%，随机掩码10%和50%。
- **ETTh1**：电力负荷数据，特征24，序列长度96，掩码25%/37.5%/50%。

### 3.2 基准与对比方法
- **对比方法**：
  - 传统深度模型：GP-VAE
  - 扩散模型：CSDI、CSBI、DSPD-GP
  - 时间序列专用模型：DLinear、LightTS、Etsformer、TimesNet（仅在ETTh1上进行对比）
- **评估指标**：RMSE、MAE（5次重复实验的平均值）。

## 4. 资源与算力
- 文中明确说明：使用**单张 NVIDIA A100-PCIE-40GB GPU**，CPU为Intel Xeon Gold-6248R 3.00GHz。
- 训练最大轮次200，学习率0.001（Adam优化器），批量大小64。
- 推理步数：CLWF为15步，对比扩散模型（CSDI等）为50步。
- 蒙特卡洛样本数：CLWF为20。
- 未提及总训练时间或GPU小时数，但暗示比传统扩散模型快。

## 5. 实验数量与充分性
- **数量**：共进行6大类实验，包括合成数据、3个真实数据集，每个数据集多个缺失率，总计超过12组指标报告。
- **消融实验**：
  - 单样本采样对比（CSDI vs CLWF）
  - 不同扩散步数（5/10/15/20）下的性能
  - Rao-Blackwellization（Base vs RB）
  - 重采样技巧（Resampling）
  - 综合（Resampling + RB）
- **充分性**：实验设计较好，覆盖多数据集、多缺失率、关键组件消融、与多种现有方法对比。但缺少与更多基于流匹配的最新工作（如Rectified Flow）的对比，也未在更大型数据集（如大型气候序列）上验证。总体客观公平，重复5次报告平均值和标准差。

## 6. 主要结论与发现
1. **性能竞争力**：CLWF在PM2.5、PhysioNet、ETTh1、合成数据上均实现了最优或次优的RMSE和MAE，尤其在某些设置下显著优于CSDI、CSBI等扩散模型。
2. **收敛快速**：仅用15步即可达到或超过扩散模型50步的效果，推理大幅加速。
3. **方差降低**：Rao-Blackwellization（结合TDAE梯度）进一步降低了采样方差，单样本采样已接近多样本结果。
4. **理论统一**：建立了最优传输、拉格朗日力学、随机最优控制、路径测度之间的联系，并通过Rao-Blackwell定理解释了方差缩减。

## 7. 优点
- **方法创新**：将物理原理（最小作用量）与生成模型结合，实现仿真自由、线性路径采样，避开传统扩散的迭代求解。
- **高效推理**：15步即可高质量生成，计算成本低。
- **理论严谨**：提供了从OT到SOC到path measure的完整理论链条，并用Rao-Blackwell定理给出方差缩减的理论保证。
- **实用技巧**：重采样技巧巧妙融合观测数据，无需额外训练。
- **实验充分**：在多个真实数据集上验证，消融实验清晰量化各组件贡献。

## 8. 不足与局限
- **实验覆盖**：仅在有限的数据集（PM2.5、PhysioNet、ETTh1）上进行测试，缺失在更大规模、更高维度、更长时间跨度（如金融、气候变化）上的验证。
- **对比局限**：未与除扩散模型外的近期流匹配方法（如Rectified Flow、Stochastic Interpolants）直接对比；在ETTh1上对比的基线多为时间序列预测模型，而非通用插补模型。
- **潜在偏差风险**：所有数据都使用随机掩码，未考虑非随机缺失模式，实际应用中缺失可能具有结构性。
- **算力报告不完整**：未提供具体训练/推理时间，仅提及步数少于扩散模型，无法准确评估绝对效率。
- **局限性声明**：论文本身未明确讨论局限性，但实际应用时，TDAE的联合训练可能增加内存开销，且势函数假设为高斯形式可能限制复杂分布的表达。
- **应用限制**：本文针对时间序列插补，但方法泛化到图像、语音等非时序数据的能力未经检验。

（完）
