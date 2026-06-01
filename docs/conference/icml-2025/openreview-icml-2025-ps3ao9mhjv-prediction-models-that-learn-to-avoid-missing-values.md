---
title: Prediction models that learn to avoid missing values
title_zh: 学习避免缺失值的预测模型
authors: "Lena Stempfle, Anton Matsson, Newton Mwai, Fredrik D. Johansson"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=ps3aO9MHJv"
tags: ["query:eeg-latent"]
score: 5.0
evidence: 缺失值避免学习适用于EEG通道补全
tldr: 该论文提出了一种缺失值避免的机器学习框架，通过正则化训练模型在测试时尽量减少对缺失特征的依赖，从而避免传统填补方法的偏差。虽然实验在表格数据上，但该方法可直接应用于EEG多通道缺失补全问题，为EEG缺失通道处理提供新的通用策略。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-ps3ao9mhjv/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 864, \"height\": 437, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ps3ao9mhjv/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 866, \"height\": 256, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ps3ao9mhjv/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1745, \"height\": 962, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ps3ao9mhjv/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1743, \"height\": 468, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ps3ao9mhjv/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 735, \"height\": 561, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ps3ao9mhjv/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1471, \"height\": 644, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-ps3ao9mhjv/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 845, \"height\": 492, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-ps3ao9mhjv/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1743, \"height\": 478, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ps3ao9mhjv/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1803, \"height\": 362, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ps3ao9mhjv/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1356, \"height\": 1247, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ps3ao9mhjv/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1743, \"height\": 481, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ps3ao9mhjv/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1729, \"height\": 1031, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ps3ao9mhjv/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1746, \"height\": 463, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-ps3ao9mhjv/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1730, \"height\": 727, \"label\": \"Table\"}]"
motivation: 传统缺失值处理方法引入偏差或增加模型复杂度，且损害可解释性。
method: 在决策树、树集成和稀疏线性模型中引入分类器特定的正则化项，鼓励模型避免使用缺失特征。
result: 该方法在多个数据集上减少了偏差，同时保持或提升预测性能。
conclusion: 缺失值避免学习是一种有效的通用框架，可扩展至EEG等领域的缺失值问题。
---

## Abstract
Handling missing values at test time is challenging for machine learning models, especially when aiming for both high accuracy and interpretability. Established approaches often add bias through imputation or excessive model complexity via missingness indicators. Moreover, either method can obscure interpretability, making it harder to understand how the model utilizes the observed variables in predictions. We propose *missingness-avoiding* (MA) machine learning, a general framework for training models to rarely require the values of missing (or imputed) features at test time. We create tailored MA learning algorithms for decision trees, tree ensembles, and sparse linear models by incorporating classifier-specific regularization terms in their learning objectives. The tree-based models leverage contextual missingness by reducing reliance on missing values based on the observed context. Experiments on real-world datasets demonstrate that **MA-DT, MA-LASSO, MA-RF**, and **MA-GBT** effectively reduce the reliance on features with missing values while maintaining predictive performance competitive with their unregularized counterparts. This shows that our framework gives practitioners a powerful tool to maintain interpretability in predictions with test-time missing values.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）
- **问题**：在机器学习模型部署（测试阶段）时，特征缺失是一个常见挑战。传统方法如**插补**（imputation）会引入偏差，而**缺失值指示器**（missingness indicators）会增加模型复杂度，两者均可能损害模型的可解释性。尤其在医疗等高风险领域，用户需要理解模型如何利用观测变量进行预测。
- **动机**：现有方法要么依赖插补后回归，要么使用缺失模式指示器，要么采用原生处理缺失值的特殊模型（如XGBoost的默认路径、贝叶斯网络等）。但这些方法要么增加偏差，要么降低可解释性，要么局限于特定模型类。作者希望找到一种通用框架，使模型在测试时主动避免依赖缺失特征，从而兼顾预测性能与可解释性。
- **整体含义**：提出**缺失值避免（Missingness-Avoiding, MA）机器学习**，通过正则化训练模型，使其在测试时尽可能少地需要缺失特征的值。核心思想是利用数据中的冗余性和缺失结构（如**ODDC规则**，即确定性的数据收集规则），在保持预测精度的前提下，将缺失值依赖降至最低。

## 2. 方法论
### 核心思想
- 定义**缺失值依赖**（missingness reliance）$\rho(h,x)$：对于输入$x$，若模型$h$在计算预测时需要用到一个缺失特征，则$\rho=1$，否则为0。期望依赖$\rho(h)=E[\rho(h,X)]$。
- 学习目标：在预测性能与缺失值依赖之间取得平衡，即最小化 $E[L(Y,h(X))] + \alpha \rho(h)$，其中$\alpha \ge 0$是权衡参数。
- 针对不同模型类设计特定的正则化项：
    - **决策树（MA-DT）**：在贪心分裂准则中加入正则项，惩罚使用缺失特征的节点分裂。具体地，分裂准则为 $C(\ell, D; j,\tau) + \alpha \sum_{i \in S_\ell} \frac{\sigma_{i,j}}{|S_\ell|} \mathbf{1}[x_{i,j}=\text{na}]$，其中$\sigma_{i,j}$用于扩展至集成模型。
    - **稀疏线性模型（MA-LASSO）**：对每个特征$j$施加个性化L1惩罚 $\lambda_j = \lambda + \alpha m_j$，其中$m_j$是该特征在训练集中的缺失率。高缺失率特征受到更大惩罚，更易被排除。
    - **随机森林（MA-RF）**：每个决策树独立使用上述正则化分裂准则（$\sigma_{i,j}=1$）。
    - **梯度提升树（MA-GBT）**：在每轮迭代中，根据之前模型对每个样本的依赖情况动态更新$\sigma_{i,j}$，避免重复惩罚已使用的缺失特征。
### 关键技术细节
- 树模型天然支持**上下文缺失避免**：决策路径只经过部分特征，因此模型可以只在某些条件满足时才依赖某特征。例如，只有MRI结果对老年患者是必需的，但对年轻患者无需访问。
- 引入**ODDC规则（Observed Deterministic Data Collection rules）**：当某些条件满足时，某特征必然被观测到。利用这些规则可以构建零缺失依赖的模型。
- 理论上证明了：当数据生成过程满足ODDC规则时，存在同时达到最小预测误差和零缺失依赖的模型（推论1）；但若缺失完全随机且独立（MCAR），则缺失依赖存在下界（命题2）。
### 公式/算法流程
- 算法1（MA-GBT）伪代码：初始化集成$e_0$，设置所有$\sigma_{i,j}=1$；每轮拟合回归树拟合伪残差，使用正则化分裂准则；更新集成和依赖权重$\sigma_{i,j}$。
- 对于MA-DT，具体实现基于CART的贪心分裂，修改分裂函数。
- MA-LASSO通过特征缩放转换可调用标准Lasso求解器。

## 3. 实验设计
### 数据集与场景
- **6个真实数据集**：NHANES（高血压预测，42特征，10000样本）、LIFE（预期寿命分类，18特征，2864样本）、ADNI（认知障碍诊断变化，39特征，1337样本）、Breast Cancer（激素受体状态，16特征，1756样本）、Pharyngitis（咽炎预测，18特征，676样本）、FICO（信用风险，23特征，10549样本）。
- 引入合成缺失机制：在Breast Cancer上添加50%人造缺失（MAR和MNAR），考察不同缺失机制的影响。
### 基准方法（Benchmark）
- **插补-回归**：L1逻辑回归（LR）、决策树（DT）、随机森林（RF），使用零插补（I0）和MICE插补（IM）。
- **缺失指示器方法**：M-GAM（稀疏加性模型，含缺失指示器及交互项）。
- **原生处理缺失值方法**：XGBoost（默认学习缺失方向）、NeuMiss（神经网络架构）、MINTY（广义线性规则模型，专门最小化缺失依赖）。
- **MA模型**：MA-LASSO、MA-DT、MA-RF、MA-GBT。
### 对比指标
- AUROC（预测性能）和缺失值依赖率$\hat{\rho}$（测试集上模型依赖缺失特征的比例）。

## 4. 资源与算力
- **文中未明确说明**使用了多少GPU、型号、数量或具体训练时长。仅提到“The computations and data handling were enabled by resources provided by NAISS (Swedish Research Council)”。对于MA-LASSO训练时间小于1秒，MINTY训练时间18-292秒，但未提及整体实验的硬件细节。
- **结论**：计算资源未详细披露。

## 5. 实验数量与充分性
- **实验数量**：共进行了多组实验：
    - **主实验**（表1）：在4个主要数据集（ADNI, FICO, LIFE, NHANES）上对比所有方法（使用零插补），重复5次不同数据划分，报告95%置信区间。
    - **补充实验**（表4、5）：使用MICE插补重复主实验；在Breast Cancer和Pharyngitis上使用两种插补。
    - **消融实验**（表6、7）：分析不同$\alpha$值（$\alpha=0$，$\alpha=\alpha^*$，$\alpha=\infty$）对MA模型性能的影响。
    - **深度与$\alpha$关系**（图3,5）：在LIFE上变化最大树深度和$\alpha$，观察AUROC和$\hat{\rho}$。
    - **缺失机制分析**（图4c）：在Breast Cancer上添加合成MAR和MNAR缺失，观察AUROC vs $\hat{\rho}$。
    - **示例树可视化**（图6）：展示LIFE上不同$\alpha$下的决策树结构。
- **充分性评价**：
    - **客观**：所有方法使用相同的数据划分（80/20），超参数通过3折交叉验证选择（基于AUROC≥95%最大值的同时最小化$\hat{\rho}$）。报告置信区间，体现了统计严谨性。
    - **公平**：对比了广泛的基线方法（插补、指示器、原生处理、专门优化缺失依赖的方法）。还采用了两种插补方法（零、MICE），覆盖常见实践。
    - **局限性**：主要基于表格数据，未涉及图像、文本等模态。缺失机制分析仅在一个数据集上进行（Breast Cancer），且仅针对线性模型（MA-LASSO）。实验未评估分布漂移或真实世界在线场景。

## 6. 主要结论与发现
- **MA模型显著降低缺失依赖同时保持竞争性性能**：在表1所有数据集中，MA-LASSO、MA-DT、MA-RF、MA-GBT的AUROC与未正则化版本的置信区间几乎全部重叠，而缺失依赖平均降低幅度很大（MA-LASSO: 66.0百分点，MA-DT: 4.4，MA-RF: 70.2，MA-GBT: 64.4）。部分场景（如NHANES）MA模型达到近乎零依赖，而基线依赖高达100%。
- **树模型尤其擅长上下文避免**：MA-DT常能达到最低缺失依赖，通过选择合适的树结构（如先分年龄再分MRI结果）实现零依赖。
- **当缺失模式存在结构（ODDC规则）时，MA效果最优**：如NHANES缺失与年份相关，MA模型能利用这种结构。
- **极端情况**：当$\alpha \to \infty$，MA模型可强制零缺失依赖，但AUROC会大幅下降（如ADNI中MA-LASSO从0.69降到0.50）。这说明需要在性能和依赖之间权衡。
- **对MNAR场景仍有鲁棒性**：合成缺失实验表明，即使在MNAR下，MA-LASSO也能在较大缺失比例下保持合理性能。

## 7. 优点
- **通用性**：框架适用于多种模型类（线性、决策树、随机森林、梯度提升），不是特化于某一种。
- **可解释性**：通过减少依赖缺失特征，决策路径更清晰，用户更易理解模型预测基于哪些观测变量。
- **无需指定缺失机制**：正则化项根据训练数据中的缺失频率自动学习，不假设缺失机制（如MCAR/MAR）。
- **理论支撑**：给出了ODDC规则下存在零依赖最优模型的充分条件（推论1），并分析了不可行情况（命题2）。
- **实验设计严谨**：采用交叉验证选参、Bootstrap置信区间、对比多种基线，且开源代码。

## 8. 不足与局限
- **实验覆盖有限**：仅基于6个表格数据集，且缺失模式主要是结构化的（如医疗调查），未在图像、文本、时间序列等非表格数据上验证。
- **未评估分布漂移**：假设训练与测试时缺失分布相同。当测试时缺失模式发生变化（如新医院的数据收集规则不同），MA模型的性能可能下降。
- **人工合成缺失实验不足**：仅在Breast Cancer（最完整的数据集）上做了合成缺失分析，且仅针对MA-LASSO，未评估树模型。
- **超参数选择依赖数据集**：$\alpha$的选择策略（先保证AUROC≥95%最大值再最小化$\hat{\rho}$）可能不是最优，不同应用场景可能有不同权衡需求。
- **计算成本未量化**：未详细报告训练时间（除MA-LASSO<1秒，MINTY 18-292秒），无法评估MA方法相较于基线的额外计算开销。
- **缺乏人类可读性度量**：虽然声称提高可解释性，但未用任何可解释性评分（如人类评估或量化指标如规则长度）来支撑。
- **未探究$L_0$正则化**：仅使用L1（MA-LASSO），理论上$L_0$更直接惩罚特征使用次数，但未实现比较。

（完）
