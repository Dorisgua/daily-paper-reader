---
title: "ASCENSION: Autoencoder-Based Latent Space Class Expansion for Time Series Data Augmentation"
title_zh: ASCENSION：基于自编码器潜空间类别扩展的时间序列数据增强
authors: "Matthieu OLEKHNOVITCH, Dorian Joubaud, Adrien Bolling, Evgeny Zotov, Sylvain KUBLER, Maxime Cordy, Mike Papadakis, YVES LE TRAON"
date: 2025-01-24
pdf: "https://openreview.net/pdf?id=pkdA4gC4p2"
tags: ["query:eeg-latent"]
score: 5.0
evidence: VAE潜空间用于时间序列数据增强
tldr: 本文针对现有生成式数据增强方法在不同时间序列数据集上效果不稳定的问题，提出ASCENSION方法，利用VAE潜空间的概率结构进行类别扩展。该方法在多个非EEG数据集上取得一致提升，为时间序列增强提供了新思路，可迁移至EEG信号增强。
source: ICML-2025-Rejected-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-pkda4gc4p2/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1761, \"height\": 540, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-pkda4gc4p2/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1639, \"height\": 452, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-pkda4gc4p2/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1676, \"height\": 499, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-pkda4gc4p2/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1769, \"height\": 665, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-pkda4gc4p2/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 859, \"height\": 281, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-pkda4gc4p2/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1743, \"height\": 585, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-pkda4gc4p2/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 823, \"height\": 271, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-pkda4gc4p2/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 806, \"height\": 224, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-pkda4gc4p2/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 805, \"height\": 225, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-pkda4gc4p2/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 804, \"height\": 228, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-pkda4gc4p2/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 804, \"height\": 228, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-pkda4gc4p2/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 804, \"height\": 225, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-pkda4gc4p2/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 802, \"height\": 223, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-pkda4gc4p2/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 803, \"height\": 220, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-pkda4gc4p2/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 822, \"height\": 271, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-pkda4gc4p2/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 804, \"height\": 220, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-pkda4gc4p2/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 841, \"height\": 734, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-pkda4gc4p2/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 845, \"height\": 732, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-pkda4gc4p2/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 845, \"height\": 731, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-pkda4gc4p2/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 852, \"height\": 727, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-pkda4gc4p2/fig-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 1770, \"height\": 864, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-pkda4gc4p2/fig-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 1859, \"height\": 2573, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-pkda4gc4p2/fig-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 1858, \"height\": 2639, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-pkda4gc4p2/fig-024.webp\", \"caption\": \"\", \"page\": 0, \"index\": 24, \"width\": 928, \"height\": 2636, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-pkda4gc4p2/fig-025.webp\", \"caption\": \"\", \"page\": 0, \"index\": 25, \"width\": 1875, \"height\": 1429, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-pkda4gc4p2/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1258, \"height\": 653, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-pkda4gc4p2/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 505, \"height\": 181, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-pkda4gc4p2/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1304, \"height\": 243, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-pkda4gc4p2/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1426, \"height\": 447, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-pkda4gc4p2/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1740, \"height\": 459, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-pkda4gc4p2/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1744, \"height\": 429, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-pkda4gc4p2/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1232, \"height\": 2212, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-pkda4gc4p2/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 183, \"height\": 2350, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-pkda4gc4p2/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1141, \"height\": 2224, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-pkda4gc4p2/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1219, \"height\": 1098, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-pkda4gc4p2/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1859, \"height\": 2573, \"label\": \"Table\"}]"
motivation: 现有时间序列数据增强方法在不同数据集上表现不稳定，缺乏通用性。
method: 利用VAE潜空间的概率结构进行类别条件扩展，生成新样本。
result: 在ECG、电力、振动等多个领域数据集上均取得一致改进。
conclusion: ASCENSION为时间序列数据增强提供了鲁棒且通用的方案，可适应不同应用。
---

## Abstract
Achieving effective data augmentation (DA) in time series classification is challenging due to the diverse nature of temporal data.  While state-of-the-art generative models for DA -- based on GANs, diffusion models, or Variational Autoencoders (VAEs) -- demonstrate potential, they often fail to deliver consistent improvements across various datasets and application domains (e.g., ECG, power consumption, vibration sensor data), as confirmed in this study. To address this limitation, we introduce ASCENSION ($\textbf{A}$utoencoder-based latent $\textbf{s}$pace $\textbf{c}$lass $\textbf{e}$xpa$\textbf{nsion}$), a novel generative approach that harnesses the probabilistic structure of the VAE's latent space alongside an innovative controlled and progressive class expansion mechanism. It promotes compact intra-class representations while maximizing inter-class separability, thereby reducing the likelihood of class overlap during latent space exploration. We evaluate ASCENSION on 102~datasets from the UCR benchmark and compare it against six state-of-the-art DA methods. Empirical results show that ASCENSION improves average classification accuracy by approximately 1\%, whereas the strongest competing method leads to an average accuracy change of -0.3\%. ASCENSION achieves a non-negative improvement in classifier performance for 66.2\% of the 102 datasets — a 16.4\% improvement over the previous best method. These results establish ASCENSION as the first DA method that can be reliably applied in real-world scenarios where prior knowledge of method suitability is uncertain. Our study further explores the key factors driving its superior performance.

---

## 论文详细总结（自动生成）

# ASCENSION: 基于自动编码器的潜在空间类扩展用于时间序列数据增广 — 详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

时间序列分类（TSC）面临时间依赖性、非平稳性和标注数据稀缺等挑战。数据增广（DA）能够生成合成样本来缓解这些问题，但现有方法（包括传统变换和基于GAN、扩散模型、VAE的生成方法）在不同数据集和应用领域（如心电图、电力消耗、振动传感器数据）中表现不一致，常常难以带来稳定的性能提升。本文指出，尚未有状态最先进的DA方法能够在时间序列分类中实现可控的、渐进式的类边界扩展，尤其是在训练与测试分布存在差异（如传感器漂移、未知条件、时间偏移）时更为关键。为此，作者提出ASCENSION，一种基于VAE的生成式DA框架，通过利用VAE潜在空间的概率结构，引入可控的类边界扩展机制，旨在生成更丰富、更具代表性的合成样本，从而提升分类性能。

## 2. 论文提出的方法论：核心思想、关键技术细节

### 核心思想
ASCENSION通过结合VAE的概率潜在空间与聚类约束，实现**受控且渐进式的类边界扩展**。与传统生成方法仅在已学习分布内插值不同，ASCENSION允许在保持类内紧凑性和类间分离性的前提下，进行**可控外推**，探索未充分代表或未见过的潜在区域，同时避免类重叠。

### 关键技术细节

1. **VAE训练与潜在空间**：使用标准的变分自编码器（VAE），优化证据下界（ELBO），编码器学习近似后验 \(q_\phi(z|x)\)，解码器重建数据。
2. **聚类约束**：引入聚类损失 \(L_{\text{cluster}}\)，对同类别样本的潜在表示进行距离度量（余弦相似度）惩罚，增强类内紧凑性、最大化类间分离性。
3. **潜在类扩展机制（五步迭代）**：
   - **步骤1**：训练VAE（包含重建损失、KL散度、聚类损失和分类损失）。
   - **步骤2**：对于每个类别 \(y\)，从高斯混合分布中采样新潜在点，该分布由该类别的多个成分的中心和协方差构成，并通过缩放因子 \(\alpha\) 控制协方差扩展程度（\(\alpha \approx 1\) 表示适度扩展）。
   - **步骤3**：如果采样的点落在重叠区域，通过最大化后验概率分配标签，实现风险感知的增广。
   - **步骤4**：解码潜在点为时间序列，并将其（带标签）添加到训练集。
   - **步骤5**：使用增广后的数据集从头重新训练模型，并重复迭代。

**公式与算法**：损失函数为 \(L_{\text{VAE}} = L_{\text{recon}} + L_{\text{KL}} + L_{\text{cluster}} + L_{\text{class}}\)。采样分布为 \(\frac{1}{K_y} \sum_{k=1}^{K_y} \mathcal{N}(\mu_{y,k}, \alpha \Sigma_{y,k})\)。算法流程见Algorithm 1（五步循环）。

## 3. 实验设计

- **数据集**：使用UCR时间序列存档中的102个数据集（原始120个，排除数据量不足的），涵盖传感器、心电图、运动、光谱等多种类型。
- **基准方法**：对比6种最新DA方法：**FAA**（传统自动增广）、**LatentAugment (LA)**、**TTS-GAN**、**Time-DDPM**、**VaDE**、**MODALS**（对于HAR数据集单独比较）。
- **分类模型**：ResNet-50和全连接网络（FCN），基于文献中报告的最优性能选择。
- **评估指标**：分类准确率。报告“改善”、“无变化”、“恶化”的数据集数量及平均准确率变化。

## 4. 资源与算力

论文在正文和附录中**未明确说明**使用的GPU型号、数量或训练时长。仅提及方法的计算效率优于GAN和扩散模型（推理更快），但未提供具体的算力信息。这表明作者可能未将算力作为重点分析内容，或者在匿名版本中省略了细节。

## 5. 实验数量与充分性

- **实验数量**：共在102个UCR数据集上进行了完整的基准测试，每个数据集使用两种分类器（ResNet和FCN），对比6种DA方法。此外，还在HAR数据集上与MODALS比较。总共实验组合数超过 \(102 \times 2 \times 6 = 1224\) 组（部分方法只用部分数据集），加上超参数敏感性分析（α和迭代次数）、特征重要性分析、置信度分析等，实验量非常丰富。
- **充分性与公平性**：实验设计较为充分。采用了标准化的UCR基准，比较了最相关的现有方法（代码可用）。数据集覆盖多种领域，分类器选择基于先前研究的最优结果。但存在一些局限：MODALS由于代码失效只能在一个数据集上比较；部分生成方法（如Time-DDPM）虽平均提升高但恶化也严重，论文如实报告了这一点。超参数分析没有给出全局最优设定，而是建议范围。总体而言，实验客观且具有说服力。

## 6. 论文的主要结论与发现

1. **ASCENSION显著优于现有方法**：在102个UCR数据集上，ASCENSION使平均分类准确率提升约1%（ResNet: +1.7%, FCN: +1.0%），而最强的竞争方法（VaDE）导致平均准确率下降 -0.3%。ASCENSION在66.2%的数据集上实现非负改进，比最好基线高出16.4%。
2. **性能一致性高**：ASCENSION在面临训练-测试分布差异（高 discrepancy）时仍能维持甚至轻微提升性能，而其他方法在该场景下性能显著下降。这使得ASCENSION特别适合现实世界中分布偏移的场景。
3. **受控扩展的关键因素**：扩展因子α建议取值[1,3]，迭代次数需与α协调。通过聚类约束和风险感知标签分配，有效避免类重叠。
4. **特征重要性分析**：不同DA方法依赖不同的时间序列特征（如周期性、波动频率、训练-测试比例等）。ASCENSION对训练-测试差异（F24）较为鲁棒。

## 7. 优点

- **方法创新性**：首次在VAE框架中引入**可控、渐进式的类边界外推**机制，解决了传统生成方法仅能内插的局限性。
- **稳定性与鲁棒性**：在大量数据集上实现了最一致的正向提升，并显著降低了性能退化数据集的比例。
- **实用价值**：适合实际部署中方法选择不确定的场景，提供了一种“可靠”的DA方案。
- **详尽分析**：不仅报告性能，还深入分析了影响DA效果的时间序列特征、超参数敏感性、类置信度以及训练-测试差异的影响，提供了可操作的见解。
- **代码公开**：提供了匿名GitHub仓库，有助于复现和后续研究。

## 8. 不足与局限

- **超参数敏感性**：α和迭代次数需要根据数据集调整，论文未给出自动选择策略，仅建议范围（α ∈ [1,3]），增加应用难度。
- **对比方法的覆盖**：与MODALS的对比仅在一个数据集上进行（由于原代码不可用），缺乏更广泛的横向比较。
- **计算资源未明确**：缺少GPU型号、训练时间等细节，难以评估方法在实际中的计算成本。
- **实验偏差风险**：虽然使用了102个数据集，但UCR存档中的数据集规模普遍较小，可能无法完全代表大规模、高维时间序列场景。
- **应用限制**：方法目前针对时间序列分类，未验证对其他序列数据（如自然语言、视频）或非序列数据（如图像）的迁移性。此外，对于训练数据极少的类别，初始聚类可能不稳定。

（完）
