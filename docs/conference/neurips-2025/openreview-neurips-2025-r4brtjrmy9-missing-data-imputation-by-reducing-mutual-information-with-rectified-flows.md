---
title: Missing Data Imputation by Reducing Mutual Information with Rectified Flows
title_zh: 通过减少互信息和矩形流的缺失数据插补
authors: "Jiahao Yu, Qizhen Ying, Leyang Wang, Ziyue Jiang, Song Liu"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=r4BrtJRmy9"
tags: ["query:eeg-latent"]
score: 7.0
evidence: 基于潜空间的插补方法，通过rectified flows可用于多通道EEG缺失通道补全
tldr: 现有缺失数据插补方法在生成质量和分布匹配上仍有不足。本文提出一种通过迭代最小化数据与缺失掩码互信息的插补方法，利用rectified flows求解ODE实现最优插补。该方法在通用数据集上展示了有效性，可直接迁移至多通道EEG的缺失通道补全任务，为EEG信号重建提供了灵活的生成工具。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-r4brtjrmy9/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1399, \"height\": 389, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-r4brtjrmy9/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1313, \"height\": 366, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-r4brtjrmy9/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1446, \"height\": 430, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-r4brtjrmy9/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1450, \"height\": 431, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-r4brtjrmy9/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1350, \"height\": 615, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-r4brtjrmy9/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1385, \"height\": 1220, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-r4brtjrmy9/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1379, \"height\": 813, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-r4brtjrmy9/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1384, \"height\": 1220, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-r4brtjrmy9/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1449, \"height\": 373, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-r4brtjrmy9/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1451, \"height\": 372, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-r4brtjrmy9/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1451, \"height\": 371, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-r4brtjrmy9/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1440, \"height\": 338, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-r4brtjrmy9/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 621, \"height\": 323, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-r4brtjrmy9/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 621, \"height\": 287, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-r4brtjrmy9/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 676, \"height\": 498, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-r4brtjrmy9/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1042, \"height\": 359, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-r4brtjrmy9/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1502, \"height\": 351, \"label\": \"Table\"}]"
motivation: 现有缺失数据插补方法在生成质量和分布匹配上存在不足，需要更有效的迭代方法。
method: 提出迭代最小化数据与缺失掩码互信息的框架，通过rectified flows目标求解ODE进行插补。
result: 在通用数据集上展示了插补性能的提升，方法具有通用性。
conclusion: 该通用插补方法可有效迁移至EEG多通道缺失数据场景。
---

## Abstract
This paper introduces a novel iterative method for missing data imputation that sequentially reduces the mutual information between data and the corresponding missingness mask. Inspired by GAN-based approaches that train generators to decrease the predictability of missingness patterns, our method explicitly targets this reduction in mutual information.
Specifically, our algorithm iteratively minimizes the KL divergence between the joint distribution of the imputed data and missingness mask, and the product of their marginals from the previous iteration. 
We show that the optimal imputation under this framework can be achieved by solving an ODE whose velocity field minimizes a rectified flow training objective. 
We further illustrate that some existing imputation techniques can be interpreted as approximate special cases of our mutual-information-reducing framework. Comprehensive experiments on synthetic and real-world datasets validate the efficacy of our proposed approach, demonstrating its superior imputation performance. Our implementation is available at \url{https://github.com/yujhml/MIRI-Imputation}.

---

## 论文详细总结（自动生成）

# 论文总结：通过减少互信息和矩形流的缺失数据插补

## 1. 核心问题与整体含义（研究动机和背景）

- **问题背景**：缺失数据在调查、fMRI等场景广泛存在。传统方法（如均值插补、MICE、MissForest）存在维度扩展性差、依赖每变量模型选择、难以并行化等问题。生成模型（GAN、归一化流）虽有应用，但GAN训练不稳定、易模式崩溃，归一化流需特殊可逆架构。
- **本文动机**：已有观察表明GAIN的生成器训练隐含减少数据与缺失掩码之间的依赖性。本文将该思想形式化为严格的互信息减少框架，并利用矩形流（Rectified Flow）构建最优插补器，克服对抗训练的不稳定性。

## 2. 方法论：核心思想、关键技术细节

- **核心思想**：提出**互信息减少迭代（Mutual Information Reducing Iterations, MIRI）**，在每轮迭代中最小化插补数据与缺失掩码的联合分布与前一轮边缘分布乘积之间的KL散度，从而逐步降低互信息。最优插补可通过求解ODE实现，该ODE的速度场通过矩形流训练目标获得。

- **关键技术细节**：
  - 定义插补过程：每轮用前一轮插补数据\(X^{(t-1)}\)的分布作为目标，训练速度场\(v^*\)，使得ODE从(0)到(1)将条件分布\(p_{X^{(t-1)}|M}\)传输到\(p_{X^{(t-1)}}\)，从而完成最优插补。
  - 训练目标：\(\min_v \int_0^1 \mathbb{E}[\|X_1 - X_0 - v(X_\tau, \ldots)\|^2] d\tau\)，其中\(X_0\)来自联合分布，\(X_1\)来自边缘乘积分布。
  - 算法流程：初始化插补 → 循环训练速度场 → 用ODE求解器更新插补值。
  - 理论证明：该框架保证互信息非增；最优插补等价于从条件分布\(q(x_{1-m}|x_m)\)中采样。

- **与现有方法的关系**：
  - GAIN可视为MIRI的近似实现（伪似然近似+Gibbs不等式）。
  - MICE、HyperImpute是MIRI在伪似然+Gibbs采样下的特例。
  - 现代条件采样方法（如SVGD、扩散模型inpainting）亦可纳入框架。

## 3. 实验设计

- **数据集与场景**：
  - **合成数据**：2维高斯混合模型（双峰），30% MCAR缺失。
  - **UCI回归基准**：10个数据集（wine, energy, parkinsons, stock, pumadyn32nm, housing, forest, bike, solar, gas），样本量从506到17379，特征数从8到128。缺失机制包括MCAR、MAR、MNAR，缺失率20%/40%/60%（MAR还有80%）。
  - **图像数据**：CIFAR-10（32×32 RGB，5000张训练样本，像素级MCAR，缺失率20%/40%/60%）；CelebA（64×64 RGB，5000张，通道独立MCAR，缺失率60%）。

- **Benchmark方法**：
  - 表格：TabCSDI、GAIN、TDM、KnewImp、MIWAE、HyperImpute。
  - 图像：GAIN、KnewImp、MissDiff、HyperImpute。
  - 指标：MMD（分布保真度）、FID、PSNR、SSIM，以及下游分类准确率。

- **对比设置**：每种方法均进行10次独立重复（不同随机掩码），报告均值±标准差。模型架构尽可能保持一致（如使用相同CNN结构）。

## 4. 资源与算力

- 论文明确说明：
  - **表格实验**：NVIDIA P100 GPU（16GB），Intel Xeon E5-2680 v4 CPU（8核2.4GHz），24GB RAM。
  - **图像实验**：NVIDIA RTX 3090 GPU（24GB），Intel Xeon Gold 6330 CPU（14核2.0GHz），90GB RAM。
  - 未报告单个实验的具体训练时长，但在附录I提供了不同维度下1000样本的墙钟时间比较表（表6），显示MIRI在5000维下约1.3小时，与扩散方法相当，远超循环方法（HyperImpute需57小时）。

## 5. 实验数量与充分性

- **实验数量**：合成数据、10个UCI数据集（3种缺失机制、多个缺失率）、2个图像数据集。消融实验在附录中提及，但本文未在主文中展示消融。
- **充分性**：实验覆盖不同数据模态（合成、表格、图像）和不同缺失机制（MCAR/MAR/MNAR），对比方法涵盖主流生成式、迭代式和传统方法。但未进行自身消融（如不同ODE求解步骤、不同初始插补）的详细分析，仅提到超参数敏感性分析见补充材料。
- **客观公平性**：架构匹配、10次重复、统一评价指标，总体较为公平。但未讨论MIRI对超参数的敏感度（仅在附录提及不敏感）。

## 6. 主要结论与发现

- MIRI在合成数据上能恢复双峰分布的正确比例（对比HyperImpute和KnewImp失败）。
- 在UCI表格数据上，MIRI在MCAR和MNAR下取得最佳平均排名（1.4和1.3），在MAR下稍逊但仍是前两名（2.0）。
- 在CIFAR-10上，MIRI在所有缺失率下的FID、PSNR、SSIM均优于或显著优于最佳基线（例如60%缺失时FID=68.58 vs HyperImpute 130.36）。下游分类准确率也最高（60%缺失时0.364 vs HyperImpute 0.212）。
- CelebA可视化显示MIRI生成质量明显优于其他方法。

## 7. 优点

- **理论严谨**：给出了互信息减少的迭代框架及其最优插补等价条件，并证明与矩形流的自然联系。
- **统一解释性**：揭示GAIN、MICE等方法的底层一致性，为该领域提供了统一视角。
- **生成质量高**：在分布保真度指标（MMD、FID）上显著优于现有方法，尤其在低样本量（5000张）和高度缺失下表现突出。
- **可并行化**：端到端向量化实现，避免了循环方法的串行瓶颈，适用于高维数据。

## 8. 不足与局限

- **计算复杂性**：每轮需完整训练速度场并求解ODE，训练成本高于简单迭代方法（如MICE）。
- **理论局限**：定理1是总体水平结果，未考虑有限样本、优化误差和ODE求解误差的影响。
- **MNAR场景**：互信息减少框架初衷是MCAR，对MAR有扩展讨论，但未明确适用于MNAR（缺失依赖真实值）。论文将其列为未来工作。
- **实验覆盖**：未进行自身组件的消融实验（如初始插补策略、迭代次数影响），超参数分析放在补充材料，正文缺乏讨论。此外，仅测试了5000张图像的CIFAR-10/CelebA，未探索更大规模数据（完整CIFAR-10或ImageNet）。
- **公平性**：虽匹配架构，但基线方法可能未充分调参（使用默认参数）；MIRI调参细节未完全公开。

（完）
