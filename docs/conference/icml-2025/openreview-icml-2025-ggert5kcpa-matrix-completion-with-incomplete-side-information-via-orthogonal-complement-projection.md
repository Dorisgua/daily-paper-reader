---
title: Matrix Completion with Incomplete Side Information via Orthogonal Complement Projection
title_zh: 基于正交补投影的不完整侧信息矩阵补全
authors: "Gengshuo Chang, Wei Zhang, Lehan Zhang"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=ggERt5kcpa"
tags: ["query:eeg-latent"]
score: 6.0
evidence: 矩阵补全方法可应用于EEG缺失通道恢复
tldr: 本文提出正交补矩阵补全（OCMC）模型，解决具有不完整侧信息的矩阵补全问题。该模型利用可用侧信息推导的正交补投影，将传统完美侧信息矩阵补全推广到不完整侧信息场景。理论分析证明其收敛性。该方法可迁移至EEG多通道缺失值插补。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-ggert5kcpa/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 837, \"height\": 600, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ggert5kcpa/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 826, \"height\": 477, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ggert5kcpa/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1775, \"height\": 328, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ggert5kcpa/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1575, \"height\": 510, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ggert5kcpa/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 642, \"height\": 691, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ggert5kcpa/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 701, \"height\": 736, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-ggert5kcpa/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1378, \"height\": 283, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ggert5kcpa/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 860, \"height\": 579, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ggert5kcpa/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1237, \"height\": 277, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ggert5kcpa/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1181, \"height\": 279, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ggert5kcpa/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 837, \"height\": 528, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ggert5kcpa/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1632, \"height\": 381, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ggert5kcpa/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1146, \"height\": 207, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ggert5kcpa/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 970, \"height\": 207, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ggert5kcpa/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1389, \"height\": 187, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ggert5kcpa/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1346, \"height\": 2197, \"label\": \"Table\"}]"
motivation: 现有矩阵补全方法假设侧信息完整，实际中难以满足。
method: 提出OCMC模型，利用正交补投影处理不完整侧信息。
result: 理论证明有效，实验验证了优越性。
conclusion: OCMC扩展了矩阵补全的适用范围。
---

## Abstract
Matrix completion aims to recover missing entries in a data matrix using a subset of observed entries. Previous studies show that side information can greatly improve completion accuracy, but most assume perfect side information, which is rarely available in practice.   In this paper, we propose an orthogonal complement matrix completion (OCMC) model to address the challenge of matrix completion with incomplete side information. The model leverages the orthogonal complement projection derived from the available side information,   generalizing the traditional perfect side information matrix completion to the scenarios with incomplete side information.  Moreover, using probably approximately correct (PAC) learning theory, we show that the sample complexity of OCMC model decreases quadratically with the completeness level. To efficiently solve the OCMC model, a linearized Lagrangian algorithm is developed with convergence guarantees. Experimental results show that the proposed OCMC model outperforms state-of-the-art methods on both synthetic data and real-world applications.

---

## 论文详细总结（自动生成）

# 详细中文总结

## 1. 核心问题与整体含义
- **研究背景**：矩阵补全（Matrix Completion）通过部分已知元素恢复完整矩阵，广泛应用于推荐系统、多标签学习、信道估计等领域。已有研究表明，利用行/列空间的侧信息（side information，如用户特征、物品特征）可显著提升补全精度。
- **核心问题**：现有方法大多假设侧信息是“完美的”，即侧信息能够完全描述目标矩阵的行列空间。然而在实际应用中，侧信息往往是不完整的（例如推荐系统中无法获取用户全部偏好特征）。
- **研究动机**：处理不完整侧信息下的矩阵补全问题，将传统仅适用于完美侧信息的模型推广到更一般的场景，并理论上分析其样本复杂度优势。

## 2. 方法论
- **核心思想**：将目标矩阵投影到四个正交子空间（基于仅有的不完整侧信息A和B），发现正交补投影（orthogonal complement projection）部分具有独特的低秩结构。通过约束该部分的核范数，可以有效缩小可行解集，从而实现即使侧信息不完整也能准确恢复。
- **关键技术细节**：
  - 定义投影算子：\(P_{AB}(X)=P_A X P_B\)，\(P_{A^\perp B^\perp}(X)=X - P_A X - X P_B + P_A X P_B\) 等。
  - 提出OCMC模型：\(\min_X \|X\|_* + \lambda \|P_{A^\perp B^\perp}(X)\|_* \quad \text{s.t. } P_\Omega(X)=P_\Omega(R)\)。核范数约束整体矩阵的低秩性，第二项约束正交补投影的低秩性。
  - 基于PAC学习理论推导泛化误差界，证明样本复杂度为 \(\min\{O(P^2 \log N / \epsilon^2), O(X^2\sqrt{N}/\epsilon^2)\}\)，其中P与侧信息完整性呈线性关系，因此样本复杂度随完整性水平二次下降。
- **算法流程（线性ADMM）**：
  1. 引入辅助变量Y，将约束转为等式。
  2. 构造增广拉格朗日函数。
  3. 交替更新X（通过线性化近似和奇异值阈值运算）、Y（直接奇异值阈值运算）、拉格朗日乘子M1、M2和惩罚参数β。
  4. 收敛率O(1/k)，保证全局最优。

## 3. 实验设计
- **使用数据集/场景**：
  - **合成数据**：100×100秩10矩阵，侧信息由SVD分解后通过随机变换控制完整性水平（20%、50%、80%）。
  - **真实数据**：
    - **多标签学习**：Yahoo.com网页分类数据集（11个主题，如Arts、Business等），每个约5000样本、432特征、21标签。
    - **电影推荐**：MovieLens-100k（943用户、1682电影、10万评分，23项用户特征、20项电影特征）。
- **Benchmark与对比方法**：SVT（无侧信息）、Maxide（完美侧信息假设）、DirtyIMC（含噪声侧信息分解）、FPC、FNNM（特征核范数最小化）。共对比5-6种方法。
- **评估指标**：合成数据使用相对Frobenius范数误差；多标签学习使用平均精度（AP）；MovieLens使用RMSE。

## 4. 资源与算力
- **文中未明确说明使用的GPU型号、数量或训练时长**。仅提供了算法复杂度分析（每次迭代SVD复杂度为O(min(m²n, n²m))），并提到可用随机SVD加速。没有报告具体硬件或运行时间信息。

## 5. 实验数量与充分性
- **实验数量**：
  - 合成数据：3种完整性水平 × 7种采样率 = 21个点，重复10次取平均（图4）。
  - 多标签学习：11个数据集 × 5种采样率（10%~90%） = 55组结果，表9完整呈现。
  - MovieLens：1个数据集 × 5种训练比例（10%~90%） = 5组结果，表3。
  - 附录中还包含：不同噪声水平（表7）、完全侧信息对比（表8）、不同秩的核范数对比（表5）、10%误差所需采样率（表6）等额外实验。
- **充分性与客观性**：实验设计较为充分，覆盖了不同完整性、不同采样率、多个真实应用场景。对比方法包含有/无侧信息、完美/不完美侧信息的多种类型。实验重复多次，统计可靠性较好。
- **不足**：缺少对超参数λ的敏感性分析（只在正文中定性讨论，无单独消融表）；缺少对更大规模数据集或更高维矩阵的验证；未提供计算时间对比。

## 6. 主要结论与发现
- OCMC模型在不完整侧信息场景下显著优于现有方法（SVT、Maxide、DirtyIMC、FPC、FNNM）。
- 样本复杂度随侧信息完整性水平二次下降，理论预测被实验趋势支持。
- 在真实世界多标签学习和电影推荐任务中，OCMC平均取得最佳或次佳性能（55组中43组第一、11组第二）。
- 算法收敛性有保证，实际运行有效。

## 7. 优点
- **方法创新性**：首次系统分析不完整侧信息下矩阵补全问题，提出通过约束正交补投影的低秩性来处理不完美信息，推广了传统模型。
- **理论完善**：基于PAC学习理论给出泛化误差和样本复杂度推导，明确显示完整性水平的影响。
- **算法高效**：线性ADMM算法将子问题通过线性化转换为闭式解，计算效率高，且保证收敛到全局最优。
- **实验全面**：涵盖合成数据和两个真实应用，与多种基线比较，结果优越。

## 8. 不足与局限
- **侧信息完整性定义假设过强**：假设列/行空间不重叠（col(A) ∩ col(Ã) = ∅），实际中侧信息可能与补充部分有重叠，模型未处理此情况。
- **实验规模有限**：最大矩阵仅100×100和MovieLens-100k（约943×1682），未在更大规模（如Netflix数据集）上验证。
- **缺乏消融研究**：对参数λ的影响仅有定性讨论，无定量实验；算法中τ、β、ρ等超参数也未经详细分析。
- **仅考虑平方损失**：文中说明算法可扩展到其他损失，但实验仅采用平方损失，未验证其他损失函数下的性能。
- **未讨论计算时间**：尽管给出复杂度，但未提供实际运行时间比较，难以评估实用性。
- **理论分析基于PAC框架**，泛化误差界不够紧，且未利用侧信息分布假设，可能保守。

（完）
