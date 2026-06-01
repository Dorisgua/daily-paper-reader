---
title: Optimal Transfer Learning for Missing Not-at-Random Matrix Completion
title_zh: 非随机缺失矩阵补全的最优转移学习
authors: "Akhil Jalan, Yassir Jedra, Arya Mazumdar, Soumendu Sundar Mukherjee, Purnamrita Sarkar"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=KpWmOJAjr7"
tags: ["query:eeg-latent"]
score: 4.0
evidence: 潜在空间偏移下的矩阵补全
tldr: 该论文针对生物学问题中矩阵整行整列缺失的补全任务，提出使用转移学习框架，利用源矩阵与目标矩阵在潜在空间的特征偏移来指导补全。方法上包含主动和被动采样策略，并达到了理论最优界。虽不直接针对EEG信号，但缺失补全与潜在空间建模的方法对EEG通道补全具有方法论上的借鉴意义。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-kpwmojajr7/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 640, \"height\": 473, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-kpwmojajr7/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 868, \"height\": 687, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-kpwmojajr7/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 848, \"height\": 696, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-kpwmojajr7/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 823, \"height\": 612, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-kpwmojajr7/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1597, \"height\": 670, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-kpwmojajr7/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1600, \"height\": 672, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-kpwmojajr7/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1596, \"height\": 670, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-kpwmojajr7/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1595, \"height\": 671, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-kpwmojajr7/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1596, \"height\": 677, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-kpwmojajr7/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1581, \"height\": 1294, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-kpwmojajr7/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1551, \"height\": 1248, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-kpwmojajr7/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1469, \"height\": 1213, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-kpwmojajr7/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1469, \"height\": 1211, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-kpwmojajr7/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 894, \"height\": 160, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-kpwmojajr7/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 880, \"height\": 249, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-kpwmojajr7/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1130, \"height\": 290, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-kpwmojajr7/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1130, \"height\": 292, \"label\": \"Table\"}]"
motivation: 生物问题中目标矩阵因整行整列缺失难以估计，需借助含噪声且不完整的源矩阵进行转移学习。
method: 利用潜在空间特征偏移连接源矩阵与目标矩阵，提出主动与被动采样下的高效估计框架。
result: 在主动采样设置下达到极小化最优估计误差，避免了对不相干性的假设。
conclusion: 提出了一种无需不相干假设的转移学习矩阵补全方法，具有理论保证和计算效率。
---

## Abstract
We study transfer learning for matrix completion in a Missing Not-at-Random (MNAR) setting that is motivated by biological problems. The target matrix 
$Q$ has entire rows and columns missing, making estimation impossible without side information. To address this, we use
a noisy and incomplete source matrix $P$, which relates to $Q$ via a feature shift in latent space. 
We consider both the *active* and *passive* sampling of rows and columns.  We establish minimax lower bounds for entrywise estimation error in each setting. Our computationally efficient estimation framework achieves this lower bound for the active setting, which leverages the source data to query the most informative rows and columns of $Q$. This avoids the need for *incoherence* assumptions required for rate optimality in the passive sampling setting. We demonstrate the effectiveness of our approach through comparisons with existing algorithms on real-world biological datasets.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）
- **研究动机**：目标矩阵 $Q$ 在缺失非随机（MNAR）场景下存在整行整列缺失，使得传统矩阵补全方法无法直接估计。该问题源于生物学应用（如代谢平衡实验、基因表达微阵列），其中实验设计或数据采集导致行或列整体缺失。
- **背景**：现有矩阵补全工作多假设缺失完全随机（MCAR）或条目独立缺失（MNAR），但无法处理整行/列缺失的极端情况。因此需要利用辅助源矩阵 $P$ 进行迁移学习，允许 $P$ 与 $Q$ 在潜变量空间存在线性特征偏移。
- **整体含义**：建立了一种主动与被动采样设置下的迁移学习框架，理论上证明其极小化最优，并通过真实与合成数据验证有效性。

## 2. 论文提出的方法论
- **核心思想**：利用源矩阵 $P$ 的奇异子空间估计（SVD），将目标矩阵 $Q$ 的估计转化为低维旋转参数 $\Theta \in \mathbb{R}^{d \times d}$ 的最小二乘问题。
- **关键技术细节**：
  - **模型假设**（Definition 1.2）：$P = U \Sigma_P V^\top$，$Q = U T_1 R T_2^\top V^\top$，其中 $U,V$ 为公共子空间，$T_1,T_2,R$ 为任意线性变换（不要求正交）。
  - **估计框架**：
    1. 对噪声源矩阵 $\tilde{P}$ 做 SVD，得到 $\hat{U}, \hat{V}$。
    2. 在观测条目集合 $\Omega$ 上求解最小二乘（公式 5）：$\hat{\Theta}_Q = \arg\min_{\Theta} \sum_{(i,j)\in\Omega} (\tilde{Q}_{ij} - \hat{u}_i^\top \Theta \hat{v}_j)^2$。
    3. 最终估计 $\hat{Q}_{ij} = \hat{u}_i^\top \hat{\Theta}_Q \hat{v}_j$。
  - **主动采样**：采用 G-最优设计（Definition 2.3）选择信息量最大的行和列，利用张量化性质（Proposition 2.4）将行列采样解耦，且无需矩阵不相干假设。
  - **被动采样**：行和列按概率 $p_{\text{Row}}, p_{\text{Col}}$ 独立采样，此时需假设源 $P$ 具有低不相干性（incoherence）以保证估计一致性。
- **理论结果**：
  - 主动设置下的极小化下界（Theorem 2.2）为 $\Omega(d^2 \sigma^2 / |\Omega|)$。
  - 所提主动采样估计器达到该下界（Theorem 2.6），且误差分解为采样误差与子空间估计误差两项。
  - 被动设置下给出理论误差上界（Theorem 2.9）与下界（Theorem 2.12），在不相干假设下极小化最优。

## 3. 实验设计
- **数据集 / 场景**：
  - **真实数据**：
    - 基因表达：来自脓毒症研究（Parnell et al., 2013），$P,Q \in \mathbb{R}^{31 \times 300}$，分别对应第1天和第2天的基因表达水平。
    - 代谢网络：来自 BiGG 数据库（King et al., 2016），$P,Q \in \mathbb{R}^{251 \times 251}$，为两种革兰氏阴性菌的加权代谢邻接矩阵。
  - **合成数据**：
    - 高度相干模型（Stylized Coherent）：$n=200, d=5$，$U,V$ 为单点指示向量，产生最大相干。
    - 矩阵划分模型（Matrix Partition Model）：$m=300, n=200, d=5$，接近社区划分结构，相干性中等。
- **基准方法**：
  - BC22（Bhattacharya & Chatterjee, 2022）：基于 MNAR 矩阵补全。
  - LLL22（Levin et al., 2022b）：基于迁移学习的矩阵补全。
  - not-MIWAE（Ipsen et al., 2021）：深度生成模型基线（仅在附录中比较）。
- **评价指标**：最大平方误差（Max Squared Error）和均方误差（MSE），并报告多次运行的中位数及 10-90 百分位区间。

## 4. 资源与算力
- 文中明确说明（Appendix B）：“所有实验在一台具有 378GB CPU/RAM 的 Linux 机器上运行。整篇论文所有结果的总计算时间少于 4 小时。”
- 未提及 GPU 或特定加速器，推测仅使用 CPU 完成。

## 5. 实验数量与充分性
- **实验组数**：包含 2 个真实数据集、2 个合成模型的对比实验，以及多个消融研究（如 target 噪声 $\sigma_Q$、source 噪声 $\sigma_P$、矩阵维度、秩、掩蔽概率 $p_{\text{Row}},p_{\text{Col}}$、源矩阵缺失程度等）。
- 每个实验独立重复多次（如 50 次或 10 次），报告中位数和百分位区间，体现统计稳健性。
- **公平性**：所有方法在相同标准化、相同掩蔽条件下比较。基线调参时传入真实秩，避免不公平优势。
- **充分性**：实验覆盖了主要变量，验证了理论预言（如相干性高时主动采样优于被动采样）。但缺乏大规模（如 $10^4$ 维度）或更复杂缺失结构（如相关掩蔽）的验证，可视为适量充分。

## 6. 论文的主要结论与发现
- 在整行/列缺失的 MNAR 矩阵补全问题中，若不借助源数据，估计不可能（Proposition 2.1）。迁移学习是必要的。
- 主动采样设置下，所提方法（G-最优设计 + 最小二乘）达到极小化最优，且无需源矩阵的不相干假设。
- 被动采样设置下，同样给出极小化最优的估计器，但需要不相干假设，否则样本复杂度可能极高。
- 真实数据实验表明：主动采样在相干性高的代谢网络数据上显著优于被动采样和现有基线；在相干性较低的基因表达数据上，主动与被动采样本方法表现接近，均优于基线。
- 合成数据进一步验证了主动采样在极端相干场景下的优势，以及理论误差界的正确性。

## 7. 优点
- **理论完整**：同时给出了主动与被动采样下的极小化下界，并设计算法达到该下界，理论保证强。
- **避免强假设**：主动采样无需不相干假设，比多数矩阵补全工作更通用。
- **计算高效**：算法仅需 SVD 和最小二乘，无复杂迭代，总运行时间少于 4 小时。
- **实验验证**：在真实生物学数据上展示有效性，并与现有方法进行公平对比。
- **张量化 G-最优设计**（Proposition 2.4）是核心创新，将行列联合采样问题简化为独立设计，实现简单且理论最优。

## 8. 不足与局限
- **实验规模有限**：真实数据维度较小（31×300, 251×251），未在高维场景（如万级）测试，可能无法反映实际大矩阵性能。
- **缺失结构假设简单**：只考虑整行/列独立缺失，未讨论相关缺失（如行与列同时缺失的概率相关），可能不适应某些实际场景。
- **噪声模型限制**：假设高斯加性噪声，实际中可能为离散、重尾或异方差噪声，方法鲁棒性未验证。
- **被动采样依赖不相干**：被动采样设置需要源矩阵 $P$ 不相干才能达到最优，而实际数据可能相干，此时主动采样是更安全的选择。
- **无代码可复现性说明**：文中未提供代码仓库或复现细节，虽然理论完整但工程复现可能略有不便。

（完）
