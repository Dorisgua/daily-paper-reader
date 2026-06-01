---
title: "GeoDynamics: A Geometric State‑Space Neural Network for Understanding Brain Dynamics on Riemannian Manifolds"
title_zh: GeoDynamics：基于黎曼流形的几何状态空间神经网络理解脑动力学
authors: "Tingting Dan, Jiaqi Ding, Guorong Wu"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=7WPi6VbtH0"
tags: ["query:eeg-latent"]
score: 5.0
evidence: 脑动力学的隐状态建模
tldr: 现有脑动力学模型通常将大脑视为松散连接的区域或强加简化的网络先验。本文提出GeoDynamics，一种基于黎曼流形的几何状态空间神经网络，将每个时刻的脑功能连接视为对称正定矩阵并建模其演化。该方法能够捕捉潜在神经状态的非线性动态，在模拟和真实fMRI数据上展现出更优的拟合能力，为理解脑网络动态提供了几何视角。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-7wpi6vbth0/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 835, \"height\": 414, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-7wpi6vbth0/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1436, \"height\": 313, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-7wpi6vbth0/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1439, \"height\": 777, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-7wpi6vbth0/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1357, \"height\": 517, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-7wpi6vbth0/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 557, \"height\": 556, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-7wpi6vbth0/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1169, \"height\": 165, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-7wpi6vbth0/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1242, \"height\": 313, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-7wpi6vbth0/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1243, \"height\": 298, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-7wpi6vbth0/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1408, \"height\": 403, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-7wpi6vbth0/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1093, \"height\": 189, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-7wpi6vbth0/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1334, \"height\": 597, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-7wpi6vbth0/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1171, \"height\": 255, \"label\": \"Table\"}]"
motivation: 现有脑动力学模型忽略功能连接矩阵的黎曼流形结构。
method: 提出基于黎曼流形的几何状态空间网络，对SPD矩阵进行非线性动态建模。
result: 在模拟和真实fMRI数据上拟合更优。
conclusion: 几何状态空间模型能更准确地刻画脑网络动态。
---

## Abstract
State‑space models (SSMs) have become a cornerstone for unraveling brain dynamics, capturing how latent neural states evolve over time and give rise to observed signals. By combining deep learning’s flexibility with SSMs’ principled dynamical structure, recent studies have achieved powerful fits to functional neuroimaging data. However, most approaches still view the brain as a set of loosely connected regions or impose oversimplified network priors, falling short of a truly holistic, self‐organized dynamical system perspective. Brain functional connectivity (FC) at each time point naturally forms a symmetric positive definite (SPD) matrix, which lives on a curved Riemannian manifold rather than in Euclidean space. Capturing the trajectories of these SPD matrices is key to understanding how coordinated networks support cognition and behavior. To this end, we introduce *GeoDynamics*, a geometric state space neural network that tracks latent brain state trajectories directly on the high‑dimensional SPD manifold. *GeoDynamics* embeds each connectivity matrix into a manifold‑aware recurrent framework, learning smooth, geometry‑respecting transitions that reveal task‐driven state changes and early markers of Alzheimer’s, Parkinson’s, and autism. Beyond neuroscience, we validate *GeoDynamics* on human action recognition benchmarks (UTKinect, Florence, HDM05), demonstrating its scalability and robustness in modeling complex spatiotemporal dynamics across diverse domains.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 论文的核心问题与整体含义（研究动机和背景）

- **研究动机**：大脑是一个复杂的动态系统，功能连接（FC）矩阵在每个时间点自然形成对称正定（SPD）矩阵，生活在弯曲的黎曼流形上，而非欧氏空间。现有脑动力学模型（如RNN、LSTM、传统SSM）大多在欧氏空间操作，将大脑视为松散连接的区域或强加简化的网络先验，忽略了FC矩阵内在的几何结构，难以捕捉真正的整体、自组织动态系统视角。
- **整体含义**：理解脑动力学需要同时尊重FC矩阵的空间几何结构（流形）和时间演化规律（状态空间模型）。本文首次将状态空间模型（SSM）与黎曼几何深度融合，提出**GeoDynamics**，直接在SPD流形上追踪潜在脑状态轨迹，揭示任务驱动的状态变化及阿尔茨海默症、帕金森症、自闭症等疾病的早期标志。此外方法还可推广到人体动作识别领域。

## 2. 论文提出的方法论：核心思想、关键技术细节

### 核心思想
- 将经典SSM的欧氏变量扩展为SPD流形上的元素：输入 \(X(t)\)、系统状态 \(S(t)\)、输出 \(Y(t)\) 均为SPD矩阵。
- 用**加权Fréchet均值**（沿测地线的内蕴平均）替代欧氏线性组合，用**正交群作用**（等距平移）替代加法更新，确保系统轨迹始终保持在流形上。

### 关键技术细节

1. **状态更新与观测方程**（公式7）：
   - 时间步 \(k\) 的状态更新：通过加权Fréchet均值聚合过去 \(\tau\) 步的状态和输入，再用正交群作用进行平移。
   - 观测方程类似：聚合当前状态和输入后平移得到输出。
   - 可学习参数 \(\{A_j, B_j, C_j, D_j\}\) 控制历史贡献。

2. **加权Fréchet均值**（公式8）：
   \[
   \mathcal{F}(\{Z_j\},\{w_j\}) = \arg\min_{F\in\mathcal{M}} \sum_{j} w_j d^2(Z_j, F)
   \]
   距离 \(d\) 采用Stein度量（避免重复特征分解），计算效率高。

3. **群作用平移**（公式9）：
   \[
   \mathcal{T}(U,V) = g(V)\, U\, g(V)^\top, \quad g(V)\in O(N)
   \]
   在Stein度量下保持等距，保证输出SPD。

4. **离散化与矩阵指数**（公式10）：
   \[
   e^A = \exp(\Delta A), \quad e^B = \Delta A^{-1}(\exp(\Delta A)-I)\Delta B
   \]
   实现稳定时间积分。

5. **任务读出**：将输出SPD矩阵通过对数映射到切空间，再经softmax分类。

6. **全局卷积重新表述**（公式14）：
   递归可等价为卷积操作 \(y = x * \mathcal{K}\)，核 \(\mathcal{K}\) 通过 \( \hat{\mathcal{K}} = \mathcal{K}^\top\mathcal{K} + \epsilon I\) 保证SPD结构。

7. **SPD保持注意力（SPA）**（公式16-17）：
   在流形卷积骨干上引入自适应注意权重 \(\delta(\cdot)\)，通过指数映射与归一化确保输出仍为SPD，突出疾病相关区域并增强可解释性。

## 3. 实验设计：数据集、基准、对比方法

### 数据集
| 类型 | 数据集 | 任务/类别 | 样本量 | 脑区/关节数 |
|------|--------|-----------|--------|-------------|
| 脑连接组 | HCP-WM（工作记忆） | 8类任务事件 | 1081 subjects | 360 |
| | ADNI | 4类认知状态（CN-like/AD-like） | 250 | 116 |
| | OASIS | 2类（阿尔茨海默症 vs 健康） | 924 | 160 |
| | PPMI | 4类（帕金森进展） | 209 | 116 |
| | ABIDE | 2类（自闭症 vs 健康） | 1025 | 116 |
| 动作识别 | UTKinect-Action3D | 10类动作 | 199 | 20 joints |
| | Florence 3D Actions | 9类动作 | 215 | 15 joints |
| | HDM05 | 14类动作 | 686 | 31 joints |

### 基准与对比方法
- **空间模型**：GCN、GIN、GSN、Moment-GNN、GNN-AK、SPDNet、MLP；以及专用脑网络模型BrainGNN、BNT、ContrastPool、STAGIN、NeuroGraph。
- **序列模型**：1D-CNN、RNN、LSTM、MLP-Mixer、Transformer、Mamba（vanilla SSM）。
- 所有方法按作者先前工作[21]统一输入格式，确保公平比较。

### 评价指标
- 准确性（Acc）、精确率（Pre）、F1分数；10折交叉验证。

## 4. 资源与算力

- **硬件**：NVIDIA RTX 6000 Ada GPU（附录A.8明确提及）。
- **未明确说明**：GPU数量、训练总时长、分布式策略等细节未提供。
- **模型参数量与推理时间**：附表7给出了各模型在HCP-WM（N=360, T=39）上的参数量（M）和每样本推理时间（ms/item）。GeoDynamics参数量14.60M，推理时间2.51 ms/item，高于Mamba（0.33 ms）但低于SPDNet（27.05 ms）和NeuroGraph（39.79 ms），表明流形操作（对数映射需SVD）增加了计算开销，但整体可控。

## 5. 实验数量与充分性

- **实验组数**：共**5个脑数据集 + 3个动作数据集**的分类任务；此外还有：
  - 滑动窗口大小消融（表1，PPMI数据集）
  - 多类分类消融（表2，ADNI数据集）
  - 模型复杂度对比（表3，HCP-WM数据集，控制参数量）
  - 注意力图可视化（图4，各数据集脑区连接模式）
- **充分性**：对比方法全面（包含空间、序列、专用脑网络模型），采用10折交叉验证，报告误差（标准差），并给出配对t检验（p<0.05）；消融实验覆盖超参数、多类难例、模型容量。整体实验设计规范、公平、足够支撑结论。

## 6. 论文的主要结论与发现

1. **性能优势**：GeoDynamics在**所有脑数据集**上均达到最高准确率，显著优于最优基线（p<0.05）。在动作识别数据集上也保持竞争力。
2. **几何建模的必要性**：与SPDNet等流形模型相比，GeoDynamics额外融合了时序SSM，进一步提升了性能，说明同时考虑几何与动态的重要性。
3. **疾病特异性注意力模式**（图4）：
   - HCP-WM：默认模式网络（DMN）和中央执行网络。
   - AD：DMN和体感皮层。
   - PD：感觉运动区、额叶、DMN、小脑。
   - 自闭症：颞叶和视觉皮层。
   - 揭示了不同疾病共享和特异的脑网络受损模式。
4. **鲁棒性**：滑动窗口大小变化下性能稳定（表1），多类分类也明显优于基线（表2）。
5. **效率**：参数量与Mamba相当（表3），推理时间适中（2.51 ms）。

## 7. 优点

- **理论创新**：将SSM与黎曼几何深度融合，提出几何状态空间框架，同时捕捉时空信息，符合FC矩阵的天然流形结构。
- **几何一致性**：所有操作（平均、平移、卷积、注意力）均保持SPD结构，避免欧氏投影造成的变形。
- **计算效率**：相比传统流形模型（如SPDNet），通过卷积重构和Stein度量简化计算，显著提升效率。
- **可解释性**：SPD保持注意力模块可定位关键脑区和连接，提供生物可视化的疾病生物标志物。
- **跨域泛化**：在脑连接组和人体动作识别两类完全不同模态的数据上均表现优异，证明框架的通用性。

## 8. 不足与局限

- **计算复杂度**：矩阵指数和对数映射需要特征分解（SVD），当脑区数量大（如N=360）时，这部分计算较重，限制了向更大规模网络的扩展。
- **几何假设敏感**：加权Fréchet均值的唯一性和稳定性依赖输入SPD矩阵位于合适的测地球内；对噪声和病态数据（如秩亏）可能失效。
- **可解释性挑战**：尽管注意力图提供了可视化，但深层几何特征如何精确映射到临床认知仍有待进一步研究。
- **实验覆盖**：未在EEG/MEG等其他模态神经数据上验证；消融实验仅在PPMI一个数据集上做窗口大小消融，可能不够全面。
- **资源细节缺失**：未报告GPU数量、训练时长、能耗等，不利于复现和公平对比效率。
- **局限性陈述**（附录A.10）：作者明确指出了上述局限，并提出未来工作包括低秩近似、多模态扩展、更可解释模型。

（完）
