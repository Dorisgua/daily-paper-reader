---
title: "Diffusion Transformers for Imputation: Statistical Efficiency and Uncertainty Quantification"
title_zh: 用于插补的扩散变压器：统计效率与不确定性量化
authors: "Zeqi Ye, Minshuo Chen"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=15mlgnyaFt"
tags: ["query:eeg-latent"]
score: 7.0
evidence: 扩散变压器用于插补，可应用于缺失EEG通道重建
tldr: 时间序列数据常存在缺失值，扩散生成模型在插补上表现优异但理论理解不足。本文分析了条件扩散变压器在插补中的统计效率和不确定性量化，推导了样本复杂度界，为使用深度生成网络重建缺失EEG通道提供了理论支撑和方法参考。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-15mlgnyaft/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1404, \"height\": 557, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-15mlgnyaft/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 606, \"height\": 396, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-15mlgnyaft/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1361, \"height\": 296, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-15mlgnyaft/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1436, \"height\": 583, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-15mlgnyaft/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1412, \"height\": 490, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-15mlgnyaft/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 791, \"height\": 95, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-15mlgnyaft/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 789, \"height\": 257, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-15mlgnyaft/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 795, \"height\": 754, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-15mlgnyaft/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 599, \"height\": 753, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-15mlgnyaft/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1439, \"height\": 182, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-15mlgnyaft/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1440, \"height\": 200, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-15mlgnyaft/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1444, \"height\": 179, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-15mlgnyaft/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1440, \"height\": 179, \"label\": \"Table\"}]"
motivation: 扩散基生成插补方法理论理解不足，尤其对时空依赖的捕获。
method: 分析条件扩散变压器的统计效率并推导样本复杂度界。
result: 提供了扩散模型用于插补的理论保证和不确定性量化方法。
conclusion: 该工作为扩散生成模型在缺失数据插补中的应用奠定了理论基础。
---

## Abstract
Imputation methods play a critical role in enhancing the quality of practical time-series data, which often suffer from pervasive missing values. Recently, diffusion-based generative imputation methods have demonstrated remarkable success compared to autoregressive and conventional statistical approaches. Despite their empirical success, the theoretical understanding of how well diffusion-based models capture complex spatial and temporal dependencies between the missing values and observed ones remains limited. Our work addresses this gap by investigating the statistical efficiency of conditional diffusion transformers for imputation and quantifying the uncertainty in missing values. Specifically, we derive statistical sample complexity bounds based on a novel approximation theory for conditional score functions using transformers, and, through this, construct tight confidence regions for missing values. Our findings also reveal that the efficiency and accuracy of imputation are significantly influenced by the missing patterns. Furthermore, we validate these theoretical insights through simulation and propose a mixed-masking training strategy to enhance the imputation performance.

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **研究动机**：时间序列数据常因传感器故障、传输错误等产生缺失值。传统统计插补方法（如均值、线性插值、ARIMA、卡尔曼滤波）依赖强线性或平稳性假设，难以处理复杂非线性依赖。近年来，基于扩散模型的生成式插补方法（如CSDI）取得了优异经验性能，但缺乏理论理解，尤其是对模型如何捕获缺失值与观测值之间的复杂时空依赖、以及缺失模式如何影响性能等问题缺乏理论分析。
- **整体含义**：本文旨在填补这一理论空白，研究条件扩散Transformer（DiT）在时间序列插补中的统计效率，并提供不确定性量化（构建置信区间）。作者从统计学习角度回答了“扩散模型如何捕获缺失值的条件分布”以及“缺失模式如何影响插补性能”这两个核心问题。

## 2. 论文提出的方法论：核心思想、关键技术细节、公式或算法流程

- **核心思想**：将时间序列插补建模为条件分布估计问题。假设数据来自高斯过程（GP），缺失块分布为条件正态分布。训练DiT学习条件得分函数，并通过得分匹配损失进行优化。基于算法展开（Algorithm Unrolling）技术，证明Transformer可以近似条件得分函数，从而推导样本复杂度上界和置信区间覆盖保证。
- **关键技术细节**：
  - **条件得分函数**：高斯过程下，条件得分函数有闭式解，但需矩阵求逆，难以表示。作者将其转化为一个二次优化问题，并用嵌套梯度下降（Nested Gradient Descent）算法求解（Algorithm 2）。外部梯度下降迭代求解主问题，内部辅助梯度下降迭代近似矩阵逆与向量乘积。
  - **Transformer架构**：构造了一个特定的Transformer（DiT）来展开上述嵌套梯度下降算法。通过多重注意力头分别捕获Σ_obs、Σ_cor、Σ_miss等不同协方差分量，并近似矩阵-向量乘积。Transformer的层数、头数等参数与条件数相关。
  - **统计样本复杂度**：Theorem 2给出分布估计的总变差距离上界为 \(\tilde{O}(\sqrt{H} d^2 \kappa^5 / \sqrt{n})\)，其中n是训练样本量，\(\kappa\)是缺失模式诱导的条件数。这表明插补效率受缺失模式影响。
  - **不确定性量化**：Corollary 1证明利用生成样本构建的置信区间的覆盖概率以\(\tilde{O}(n^{-1/2})\)速率收敛到名义水平，且受分布偏移系数影响。
  - **混合掩码训练策略**：为应对训练与测试缺失模式不匹配导致的分布偏移，提出混合不同缺失模式（从完全随机到强分组）进行训练，以覆盖更多场景。
- **算法流程**：Algorithm 1给出扩散插补流程，包括训练阶段（用掩码模拟缺失-观测对，训练条件扩散模型）和插补阶段（对新的观测序列生成多个缺失样本，计算点估计和置信区间）。

## 3. 实验设计：使用了哪些数据集 / 场景，其 benchmark 是什么，对比了哪些方法

- **合成数据**：
  - **高斯过程（GP）数据**：长度H=96，维度d=8，缺失长度16。设计了四种缺失模式（P1-P4），对应的条件数从高到低（415.4, 29.57, 9.47, 3.0）。改变样本量n（10^3 到 10^5）进行训练和测试。
  - **潜在高斯过程（Latent GP）数据**：对GP数据施加非线性变换ϕ(x)+噪声，以评估泛化能力。
- **真实世界数据集**：
  - **BeijingAir**：北京空气质量数据，包含6种污染物和气象变量，12个监控站点，每小时采样，序列长度30。
  - **ETT_m1**：电力变压器温度数据，包括电力负荷和油温，序列长度48，时间间隔15分钟。
  - 缺失率设置为10%、20%、50%进行评测。
- **基准方法**：对比了**CSDI**（条件得分扩散插补）和**GPVAE**（高斯过程变分自编码器）。确保各模型参数数量相当。
- **评估指标**：对于合成数据，主要评估置信区间覆盖率（CR Coverage）和MSE；对于真实数据，评估MAE、MSE、MRE。

## 4. 资源与算力：如果文中有提到，请总结使用了多少算力（GPU 型号、数量、训练时长等）。若未明确说明，也请指出这一点

- 论文在Appendix F中明确说明：实验使用一块 **NVIDIA RTX A6000 GPU（48GB）** 和一颗 **Intel(R) Xeon(R) Gold 6242R CPU @ 3.10GHz**。
- 训练配置：batch size 64，DiT模型隐藏大小256，12层Transformer，16个注意力头。
- **未明确给出具体训练时长**，但提到所有结果均为5次运行的平均值。算力资源适中，未提及多GPU或大规模分布式训练。

## 5. 实验数量与充分性：大概做了多少组实验，这些实验是否充分、是否客观、公平

- **实验数量**：
  - 合成GP实验：不同样本量（5种）× 4种缺失模式，共20组；还做了序列长度变化实验（5种H）。
  - 潜在GP实验：4种缺失模式 × 4种训练策略（S1-S4），对比CSDI、GPVAE，共16组。
  - 真实数据集实验：2个数据集 × 3种缺失率（10%,20%,50%），对比CSDI和GPVAE，共6组（加上混合掩码策略的额外比较）。
  - 消融实验：对混合掩码策略单独对比（S1-S4），以及仅使用单一分组模式（如8×2、4×4、1×16）。
  - 总共约50+组实验，覆盖合成和真实场景，并且报告了均值和标准差（5次重复）。
- **充分性**：实验较为充分：验证了理论预测（条件数影响、样本量影响），测试了提出的混合掩码策略，并在真实数据集上验证。但真实数据集仅有2个，且均为中等规模，缺乏对超长序列或高维大规模数据的测试。
- **客观与公平**：对比方法选择合理（CSDI、GPVAE），且说明确保参数数量相当；结果报告了标准差。但部分实验（如表2中的“Only *”策略）可能未在所有缺失模式上重复足够多次。总体公平性较好。

## 6. 论文的主要结论与发现

- **理论方面**：
  1. DiT能够有效学习缺失值的条件分布，样本复杂度以 \(n^{-1/2}\) 速率收敛，且与序列长度H多项式相关，受缺失模式的条件数 \(\kappa\) 影响显著。
  2. 条件数大的缺失模式（如连续块缺失）需要更多样本，插补更困难；而分散随机缺失模式更容易。
  3. 构建的置信区间覆盖概率以 \(n^{-1/2}\) 速率收敛到名义水平，分布偏移系数会影响实际覆盖。
- **实验方面**：
  1. 合成数据验证了理论：样本量越大，置信区间覆盖越接近名义水平；低条件数的模式所需样本更少。
  2. 提出的混合掩码训练策略显著优于纯随机掩码训练，尤其对于高条件数的测试模式。
  3. 在真实数据集上，DiT在MAE、MSE、MRE上均优于CSDI和GPVAE，且混合掩码策略进一步提升了DiT性能。
  4. 潜在GP实验表明该方法和理论可以推广到非线性场景。

## 7. 优点：方法或实验设计上有哪些亮点

- **理论贡献**：首次为条件扩散Transformer在时间序列插补中提供了严格的统计效率分析，包括样本复杂度、置信区间覆盖保证和缺失模式影响，填补了该领域的理论空白。
- **算法展开技巧**：通过嵌套梯度下降将条件得分函数的矩阵求逆转化为可被Transformer近似表达的迭代过程，为构建近似理论提供了新颖思路。
- **混合掩码训练策略**：从分布偏移理论出发提出的实用训练策略，方法简单有效，且在其他模型（CSDI）上也有增益，说明其通用性。
- **实验设计**：同时使用合成数据和真实数据，合成数据精确控制变量（条件数、样本量）验证理论，真实数据验证实际性能；消融实验充分对比了不同掩码策略。
- **不确定性量化**：不仅做点估计，还构建了置信区间并理论证明其覆盖性质，这对实际应用（如医疗、金融）很重要。

## 8. 不足与局限：包括实验覆盖、偏差风险、应用限制等

- **理论假设限制**：核心假设数据服从高斯过程（GP），且缺失完全随机（MCAR）。实际时间序列可能不满足GP假设（如厚尾、异方差），MCAR也未必成立，理论推广性受限。
- **实验规模**：真实数据集仅两个，且数据维度不高（d≤132），序列长度不长（≤48）。未在更大规模、更高维度的数据集上验证，如传感器网络、金融时间序列等。也未测试极长序列（H>1000）。
- **计算资源细节**：未报告训练时间，且仅使用单GPU。实际部署时大型DiT可能计算开销较大，文章未讨论效率优化。
- **混合掩码最优比例**：文章指出最优比例是实例相关的，未给出通用指导原则，实际操作需凭经验调整。
- **对比方法局限**：对比方法只有两种（CSDI、GPVAE），未包括更近期的扩散模型（如MTSDI、Timediff）或其他生成模型（如GAN-based）。且GPVAE在实验中表现很差，可能代码调参未最优化。
- **偏差风险**：合成数据中的缺失模式为人工构造，实际缺失机制可能更复杂；神经网络训练过程中可能存在未收敛等问题。实验重复5次，但未报告更详细的统计检验。

（完）
