---
title: Iterative Missing Data Imputation with Model Form Adaptation and Non-Missing Feature Supervision
title_zh: 基于模型形式自适应和非缺失特征监督的迭代缺失数据插补
authors: "Hao Wang, zhengnan li, Zhichao Chen, Xu Chen, Shuting He, Guangyi Liu, Haoxuan Li, Zhouchen Lin"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=L84DdFuvwV"
tags: ["query:eeg-latent"]
score: 6.0
evidence: 迭代缺失数据插补方法，具有模型形式自适应，适用于EEG通道恢复
tldr: 现有迭代插补方法对所有特征使用同一模型形式，且未充分利用完整特征信息。本文提出核点插补（KPI），一种双层优化框架，允许每个特征自适应最优模型形式，并利用非缺失特征作为监督，提升了插补精度。该方法可直接应用于EEG多通道缺失补全。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-l84ddfuvwv/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 680, \"height\": 285, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-l84ddfuvwv/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 686, \"height\": 273, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-l84ddfuvwv/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1443, \"height\": 504, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-l84ddfuvwv/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1459, \"height\": 644, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-l84ddfuvwv/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1460, \"height\": 635, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-l84ddfuvwv/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1405, \"height\": 314, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-l84ddfuvwv/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1444, \"height\": 829, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-l84ddfuvwv/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 626, \"height\": 658, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-l84ddfuvwv/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 708, \"height\": 657, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-l84ddfuvwv/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1475, \"height\": 685, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-l84ddfuvwv/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1473, \"height\": 686, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-l84ddfuvwv/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1469, \"height\": 684, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-l84ddfuvwv/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1468, \"height\": 682, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-l84ddfuvwv/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1477, \"height\": 687, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-l84ddfuvwv/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1497, \"height\": 638, \"label\": \"Table\"}]"
motivation: 现有迭代插补方法存在模型形式单一和忽略完整特征信息的问题。
method: 提出核点插补（KPI），通过双层优化为每个特征自适应选择模型形式并利用非缺失特征。
result: 在多个数据集上展示了插补性能的提升。
conclusion: 该方法为缺失数据插补提供了更灵活的解决方案，可推广至EEG通道补全。
---

## Abstract
Iterative imputation is a prevalent method for missing data imputation, where each feature is imputed iteratively by treating it as a target variable estimated from all other features. However, iterative imputation method suffers from two principal limitations: 
(1) it imposes a single parametric model form to impute all features, neglecting the potential for optimal models to vary among features, which risks model misspecification; and
(2) it assumes every feature contains missing values, overlooking the potential presence of non-missing features, termed as oracle features, which are informative for imputation. 
To address these limitations, we propose kernel point imputation (KPI), a bi-level optimization framework for iterative missing data imputation. 
At the inner level, KPI adaptively learns the optimal model form for each feature within a reproducing kernel Hilbert space, addressing limitation (1). At the outer level, KPI utilizes oracle features as supervisory signals to iteratively refine the imputations, addressing limitation (2). 
Experiments demonstrate that KPI outperforms competitive imputation methods. Code is available at https://github.com/FMLYD/kpi.git.

---

## 论文详细总结（自动生成）

## 论文中文总结

### 1. 核心问题与整体含义（研究动机与背景）
- **问题背景**：缺失数据广泛存在于实际数据采集与分析中。迭代插补（iterative imputation）是一类流行的缺失数据处理方法，其基本思路是依次将每个特征作为目标变量，利用其余特征对其建模并估计缺失值。
- **现有局限**：作者指出现有迭代插补方法存在两个关键缺陷：
  - **❶ 模型形式固化**：对所有特征采用同一参数化模型（如线性模型或决策树），忽略了各特征间可能存在的异质性依赖关系，导致模型设定偏差（model misspecification）。
  - **❷ 忽略完整特征**：假设每个特征都含有缺失值，从而忽视了那些几乎完整的特征（称为 oracle features）可作为高质量监督信号用于插补。
- **研究含义**：解决上述两个局限对于提升缺失数据插补的精度与鲁棒性具有重要意义，尤其是当数据缺失率高或特征分布复杂时。

---

### 2. 方法论：核心思想、关键技术细节与算法流程
- **总体框架**：提出核点插补（Kernel Point Imputation，KPI），一种**双层优化**框架，将迭代插补重新建模为双层优化问题。
  - **内层**：针对每个特征，在再生核希尔伯特空间（RKHS）中自适应选择最优函数形式，以缓解模型设定偏差。
  - **外层**：利用 oracle features 作为监督信号，迭代更新其他特征的插补值。
- **关键技术细节**：
  - **核函数与通用性**：采用高斯核（universal kernel），其 RKHS 可以逼近任意连续函数，从而灵活建模各特征的非线性依赖。
  - **表示定理**：基于表示定理，最优估计器可表示为核函数的线性组合，从而将无限维优化问题转化为有限维参数求解。
  - **闭式解**：给定两个批次的输入特征 \(X_s, X_t\) 和目标 \(Y_s, Y_t\)，最优模型输出可写为：
    \[
    f^*(X_t) = K_{X_t X_s}(K_{X_s X_s} + \lambda I)^{-1} Y_s
    \]
    最终目标函数为：
    \[
    \mathcal{P} = \left\| Y_t - K^\Delta_{X_t X_s} (K^\Delta_{X_s X_s} + \lambda I)^{-1} Y_s \right\|^2_2
    \]
    其中 \(K^\Delta\) 是多个核矩阵的可学习凸组合。
  - **自适应核集成**：为缓解缺失数据下核超参数（如带宽）选择的困难，采用多个不同参数的核，并通过可学习的单纯型向量 \(\Delta\) 进行加权集成。
  - **训练流程**：初始化使用均值填充；每轮随机采样两个批次，随机选择一个特征作为目标，计算损失 \(\mathcal{P}\)；通过自动微分计算梯度，仅更新缺失位置的值和核权重 \(\Delta\)；迭代直到验证集早停。
- **算法流程图**（图 2 所示）：包括前向计算、反向梯度传播、梯度掩码（只更新缺失值）等步骤。

---

### 3. 实验设计
- **数据集**：7 个公开 UCI 表格数据集：
  - Blood Transfusion (BT), Concrete Compression (CC), Connectionist Bench Vowel (CBV), Ionosphere (IS), Parkinsons (PK), Qsar Biodegradation (QB), Wine Quality White (WQW)。
- **缺失场景**：
  - 缺失率：0.1, 0.2, 0.3, 0.4（MCAR 机制为主）。
  - 额外实验：MAR（缺失依赖于观测值）、MNAR（缺失依赖于自身值）。
- **基线方法**：
  - 简单插补：均值、中位数、众数。
  - 迭代插补：MICE (线性模型), MissForest (随机森林)。
  - 生成式插补：GAIN, MIWAE, CSDI-T, MissDiff, ReMasker, NewImp。
  - 其他：Sinkhorn (最优传输), TDM (分布匹配), MIRACLE (因果感知)。
- **评价指标**：均方误差（MSE）、平均绝对误差（MAE）、Wasserstein 距离（WASS），均只计算缺失位置上的误差。
- **实施细节**：最大迭代 500，早停 patience=10，Adam 优化器，超参数 \(\eta \in [0.0001,0.01]\)，批量大小 \(B \in [64,512]\)，核数 \(E \in [1,7]\)，带宽 \(\sigma \in [0.01,10]\)，通过 5% 验证集调优。

---

### 4. 资源与算力
- **硬件平台**：文中明确说明：“Experiments are performed on a platform with two Intel(R) Xeon(R) Platinum 8383C CPUs @ 2.70GHz and a NVIDIA GeForce RTX 4090 GPU.”
- **算力统计**：未报告总训练时长或各实验的耗时细节。附录 C.1 提供了单次前向/后向传播的时间分析（在给定配置下每轮约 1–4 ms），并指出批量大小和特征数量对时间的影响，但未给出完整训练的总计算量。

---

### 5. 实验数量与充分性
- **实验数量**：非常丰富。包括：
  - 主实验结果（表1）：7 个数据集 × 4 种缺失率 × 多个指标 × 10+ 种基线。
  - 缺失机制实验（附录表8-9）：MAR 和 MNAR 下的 7 个数据集对比。
  - Oracle 特征比例分析（图3）：4 个数据集下随 oracle 比例变化的效果。
  - 核策略消融（表2-3）：核数量（1/3/5/7）与核函数类型（线性/多项式/Laplacian/高斯）的对比。
  - 超参数敏感性（图4）：学习率和批量大小的网格测试。
- **充分性评价**：
  - **客观、公平**：基线涵盖多种范畴（经典迭代、生成式、最优传输等），且所有方法在同一缺失设置下评估。KPI 在几乎所有场景下均优于最强基线，结论稳健。
  - **不足**：缺少对更大规模数据集（如数千特征、百万样本）的测试；仅使用 UCI 数据集，未涉及图像、时序或自然语言等模态。

---

### 6. 主要结论与发现
1. **KPI 在所有 7 个数据集和所有缺失率下均取得最优或次优性能**，尤其在 CC 和 QB 数据集上提升显著。
2. **模型形式自适应有效**：相较于固定模型（如 MICE 的线性模型、MissForest 的随机森林），KPI 通过 RKHS 自适应更灵活地捕捉特征间异质性依赖，缓解了模型误设。
3. **Oracle 特征利用有益**：随着 oracle 特征比例增加，KPI 误差持续下降，而 MissForest 无明显改善，验证了将完整特征作为监督信号的有效性。
4. **核集成策略提升了表达力**：从 1 个核增加到 7 个核，MSE 相对下降约 20%–32%，且高斯核优于线性或多项式核，体现通用核的重要性。
5. **超参数敏感度可控**：学习率 \(\eta \approx 0.01\)、批量大小 \(B \approx 512\) 为较好配置，过大或过小均会导致性能下降。

---

### 7. 优点
- **方法创新性**：首次将迭代插补的双重局限（模型固化 + 忽略完整特征）统一到双层优化框架下解决，理论动机清晰。
- **理论坚实**：基于 RKHS 通用性、表示定理给出闭式解，并证明了自适应核集成的合理性。
- **实现简洁**：整个流程可端到端通过随机梯度下降优化，与主流深度学习框架兼容。
- **实验全面**：覆盖多种缺失机制、缺失率、核策略和超参数，验证了方法的鲁棒性和适用性。
- **可复现性**：提供了 GitHub 代码仓库（https://github.com/FMLYD/kpi.git）。

---

### 8. 不足与局限
- **噪声鲁棒性**：文中承认未考虑数据中的观测噪声，而工业场景中噪声普遍存在。未来可引入鲁棒优化或对核矩阵中的异常值进行截断。
- **核超参数选择**：自适应集成是一种启发式方法，缺乏理论保证。作者建议未来探索元学习等更严格的选择策略。
- **实验覆盖范围**：
  - 仅使用 UCI 小型表格数据集（样本数几百至几千），未在更大规模或更复杂结构（时序、图、图像）上验证。
  - 缺失模式虽模拟了 MCAR/MAR/MNAR，但均为人工生成，实际缺失模式可能更复杂。
- **计算开销**：尽管单次迭代较快，但需多轮迭代（最多 500 轮）且每轮需计算矩阵逆（\(K+\lambda I\)），在特征数 \(D\) 或批量大小 \(B\) 很大时计算成本可能显著上升，论文也未报告完整训练时长。
- **假设强度**：方法默认 oracle features 完全无缺失，实践中若 oracle features 也含少量缺失，则需额外处理。

（完）
