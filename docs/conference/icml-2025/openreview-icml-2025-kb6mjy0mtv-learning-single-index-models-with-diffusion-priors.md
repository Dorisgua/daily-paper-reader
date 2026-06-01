---
title: Learning Single Index Models with Diffusion Priors
title_zh: 使用扩散先验学习单指标模型
authors: "Anqi Tang, Youming Chen, Shuchen Xue, Zhaoqiang Liu"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=kB6mJY0MTV"
tags: ["query:eeg-latent"]
score: 6.0
evidence: 扩散模型作为生成先验用于信号恢复，可应用于EEG重建
tldr: 现有基于扩散模型的信号恢复方法要么针对特定重建问题，要么无法处理含不连续或未知链接函数的非线性测量。本文提出一种高效方法，利用扩散先验从半参数单指标模型中恢复信号，涵盖了多种非线性模型。该方法适用于EEG信号重建等任务，能够处理非线性和未知失真，提高了重建质量。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-kb6mjy0mtv/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 805, \"height\": 164, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-kb6mjy0mtv/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 860, \"height\": 929, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-kb6mjy0mtv/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 861, \"height\": 349, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-kb6mjy0mtv/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 856, \"height\": 825, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-kb6mjy0mtv/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 848, \"height\": 644, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-kb6mjy0mtv/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1730, \"height\": 831, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-kb6mjy0mtv/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1758, \"height\": 302, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-kb6mjy0mtv/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1691, \"height\": 1601, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-kb6mjy0mtv/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1767, \"height\": 642, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-kb6mjy0mtv/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 901, \"height\": 448, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-kb6mjy0mtv/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 852, \"height\": 232, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-kb6mjy0mtv/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 870, \"height\": 406, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-kb6mjy0mtv/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 855, \"height\": 233, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-kb6mjy0mtv/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1403, \"height\": 334, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-kb6mjy0mtv/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1243, \"height\": 216, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-kb6mjy0mtv/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1830, \"height\": 368, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-kb6mjy0mtv/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1828, \"height\": 368, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-kb6mjy0mtv/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1026, \"height\": 444, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-kb6mjy0mtv/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 711, \"height\": 360, \"label\": \"Table\"}]"
motivation: 现有扩散模型信号恢复方法对非线性测量模型支持不足。
method: 提出利用扩散先验恢复半参数单指标模型中的信号，处理不连续未知链接函数。
result: 在多个非线性恢复任务中取得优异效果，重建质量显著提升。
conclusion: 该方法通用且有效，可扩展到EEG等信号重建领域。
---

## Abstract
Diffusion models (DMs) have demonstrated remarkable ability to generate diverse and high-quality images by efficiently modeling complex data distributions. They have also been explored as powerful generative priors for signal recovery, resulting in a substantial improvement in the quality of reconstructed signals. However, existing research on signal recovery with diffusion models either focuses on specific reconstruction problems or is unable to handle nonlinear measurement models with discontinuous or unknown link functions. In this work, we focus on using DMs to achieve accurate recovery from semi-parametric single index models, which encompass a variety of popular nonlinear models that may have {\em discontinuous} and {\em unknown} link functions. We propose an efficient reconstruction method that only requires one round of unconditional sampling and (partial) inversion of DMs. Theoretical analysis on the effectiveness of the proposed methods has been established under appropriate conditions. We perform numerical experiments on image datasets for different nonlinear measurement models. We observe that compared to competing methods, our approach can yield more accurate reconstructions while utilizing significantly fewer neural function evaluations.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义
- **研究动机**：扩散模型（DMs）在信号恢复中展现了强大潜力，但现有方法通常局限于**特定线性问题**（如超分辨率、去模糊）或要求**已知的、连续的链接函数**，无法处理**非线性、不连续或未知**的链接函数。
- **核心问题**：如何利用扩散先验，从**半参数单指标模型（SIM）**（如1-bit量化、立方测量等）中准确恢复原始信号，且不依赖链接函数的具体形式。
- **整体含义**：提出通用、高效的信号重建框架，扩展扩散模型在**更广泛非线性测量场景**（包括未知非线性）中的应用，具有重要的理论价值和实际意义。

---

### 2. 提出的方法论
- **核心思想**：利用扩散模型的**采样过程**和**逆过程**，将观测数据通过简单线性投影（\( \frac{1}{m}A^\top y \)）视为带噪版本，并选择一个**中间扩散时间** \( t^* \) 来平衡噪声水平，然后执行**部分逆**（从 \( t^* \) 逆到 \( T \)）和**完整采样**（从 \( T \) 采样到 \( \epsilon \)），从而重建信号。
- **关键技术细节**：
    - 根据理论分析（Lemma 2），\( \frac{1}{m}A^\top y \approx \mu x^* + \mathcal{O}(1/\sqrt{m}) \) 的噪声。选择 \( t^* \) 使得扩散噪声水平 \( \sigma_{t^*}/\alpha_{t^*} = C_s/\sqrt{m} \)（\( C_s \) 为调节参数）。
    - 提出三种变体：
        - **SIM-DMFIS**：全逆 + 全采样（性能差）。
        - **SIM-DMS**：仅从 \( t^* \) 开始采样（无逆过程，性能中等）。
        - **SIM-DMIS**（主要方法）：先部分逆（\( t^* \to T \)），再全采样（\( T \to \epsilon \)），仅需一次无条件采样和部分逆。
    - 采用DDIM或二阶DM2M求解器，利用**数据预测网络** \( x_\theta(x,t) \) 驱动逆/采样。
- **算法流程**（Algorithm 1）：
    1. 根据 \( \sigma_{t^*}/\alpha_{t^*} = C_s/\sqrt{m} \) 计算 \( t^* \)。
    2. 计算输入 \( \alpha_{t^*} \frac{C'_s}{m} A^\top y \)（\( C'_s \) 为另一调节参数）。
    3. 执行部分逆 \( G^\dagger_{>t^*} \) 得到 \( \hat{x}_T \)，然后执行完整采样 \( G \) 得到最终重建 \( \hat{x} \)。
- **理论保证**：在神经网络Lipschitz连续等假设下（Assumption 1），给出重建误差上界（Theorem 3）：\( \|\bar{x}_\epsilon - G \circ G^\dagger_{>t}(\bar{x}_t)\|_2 = \mathcal{O}(\sqrt{n}(h_{\max}^{k_2} + L h_{\max}^{k_1})) \)。

---

### 3. 实验设计
- **数据集**：
    - **FFHQ** \( 256\times256 \)（\( n=196608 \)）
    - **ImageNet** \( 256\times256 \)
    - **CIFAR-10** \( 32\times32 \)（补充实验）
- **非线性测量模型**：
    - **1-bit测量**：\( y = \text{sign}(Ax^* + e) \)
    - **立方测量**：\( y = (Ax^*)^3 + e \)
    - 噪声 \( e \sim \mathcal{N}(0,\sigma^2 I_m) \)，\( \sigma=0.05 \)
- **对比方法**：
    - QCS-SGM（仅1-bit，基于VE调度）
    - DPS-N / DPS-L（分别利用/不利用链接函数知识）
    - DAPS-N / DAPS-L
    - 自身变体 SIM-DMS、SIM-DMFIS
- **评估指标**：PSNR（↑）、SSIM（↑）、LPIPS（↓）
- **实验设置**：
    - 采样使用DDIM，逆使用DM2M。
    - SIM-DMIS：NFE = 150；SIM-DMS：NFE = 50；QCS-SGM：>11000 NFE；DPS/DAPS：1000 NFE。
    - 预训练模型来源：DPS提供的FFHQ/ImageNet模型，ADM分类器，DDPM for CIFAR-10。

---

### 4. 资源与算力
- 论文未明确提及训练算力（模型均为预训练，无需重新训练）。
- **推理算力**（附录H）：在**单张 NVIDIA GeForce RTX 4090 GPU**上测试重建速度，SIM-DMIS推理10张FFHQ图像耗时约5.66秒（NFE=150），SIM-DMS耗时约1.96秒（NFE=50），远快于DPS（142秒）和DAPS（160秒）。
- 所有实验均在此单卡上完成，无需大规模分布式计算。

---

### 5. 实验数量与充分性
- **主要实验组**：
    - FFHQ + ImageNet 上的 1-bit 和立方测量（各1组，共4组定量+定性结果）。
    - CIFAR-10 补充实验（1-bit两组m=500/1000，立方两组m=500/1000）。
    - **消融实验**（附录F、G）：
        - 对SIM-DMS和SIM-DMIS在CIFAR-10上调节参数 \( C_s, C'_s, \text{NFE} \)。
    - **性能与效率对比**（附录H）：FFHQ上对比相同NFE下SIM-DMS与SIM-DMIS，并记录推理时间。
- **充分性评价**：
    - 实验覆盖了图像数据集从低分辨率（32×32）到高分辨率（256×256），非线性模型包括离散（1-bit）和连续（立方）未知道路，对比方法包括当前最先进的后验采样方法，**较为全面**。
    - **公平性**：对比方法使用相同的预训练骨架（如DPS提供的模型），参数调优按各方法原始设置。
    - 不足：消融实验仅在一个数据集上（CIFAR-10）进行，缺乏在其他高分辨率数据集上的参数敏感性分析；对噪声鲁棒性的系统性实验较少（仅固定σ=0.05）。

---

### 6. 论文的主要结论与发现
- 提出的 **SIM-DMIS** 在1-bit和立方测量下，**在所有指标上显著优于** QCS-SGM、DPS、DAPS 等竞争方法，同时所需**NFE仅为其1/7到1/70**，计算效率极高。
- **部分逆（SIM-DMIS）** 远优于全逆（SIM-DMFIS）和仅采样（SIM-DMS），验证了从中间时间 \( t^* \) 开始逆的理论动机。
- 理论分析（Theorem 3）为方法有效性提供了严格保证，匹配实验观察。
- 即使链接函数**未知且不连续**（如sign函数），方法仍能鲁棒重建，克服了DPS/DAPS依赖梯度信息的局限。

---

### 7. 优点
- **高效性**：仅需150次神经函数评估，远少于现有方法（1000-11555次），推理速度快。
- **通用性**：不依赖链接函数知识，适用于非线性、未知、不连续的测量模型。
- **理论保证**：在合理假设下给出重建误差界，支撑方法可靠性。
- **简洁实现**：仅需一次无条件采样和部分逆，无需迭代优化或任务特定训练。
- **广泛的实验验证**：在多个数据集和测量模型上一致表现优越，且与多个强基线对比。

---

### 8. 不足与局限
- **应用限制**：方法假设信号位于扩散模型生成器范围内（\( x^* \in \mathcal{R}(G) \)），且要求 \( \mu \neq 0 \)（见Remark 1），因此不适用于相位恢复（\( \mu=0 \)）等模型。
- **参数选择**：\( C_s, C'_s \) 需要手动调节，虽然通过理论引导，但仍需针对不同问题调优，消融研究仅覆盖CIFAR-10。
- **实验覆盖**：仅在图像数据上验证，未在EEG、音频等模态上展示；对比方法中的OneShot（GAN基）仅在CIFAR-10立方测量中比较，缺少更多GAN基线。
- **噪声鲁棒性**：实验仅测试了固定噪声水平（\( \sigma=0.05 \)），未系统分析不同噪声强度的影响。
- **理论条件**：Lipschitz连续性假设对神经网络未必严格成立，且误差界中的常数依赖于难以直接计算的量（如 \( L_t \)、\( h_{\max} \)）。
- **可复现性**：代码和预训练模型未公开（论文中未提供仓库链接），可能影响复现。

（完）
