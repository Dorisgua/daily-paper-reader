---
title: "EvoBrain: Dynamic Multi-Channel EEG Graph Modeling for Time-Evolving Brain Networks"
title_zh: EvoBrain：用于时变脑网络的动态多通道EEG图建模
authors: "Rikuto Kotoge, Zheng Chen, Tasuku Kimura, Yasuko Matsubara, Takufumi Yanagisawa, Haruhiko Kishima, Yasushi Sakurai"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=XmV7KRABBl"
tags: ["query:eeg"]
score: 4.0
evidence: 动态多通道EEG图建模用于癫痫检测，属于EEG信号处理范畴
tldr: 现有动态图神经网络在EEG癫痫检测中难以捕获脑连接随时间演化的特性。本文提出EvoBrain，通过构建时变图结构并联合建模时空特征，动态反映癫痫进展中的脑网络变化。实验表明该方法在癫痫检测任务上性能提升，揭示了动态脑网络建模的重要性。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-xmv7krabbl/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1424, \"height\": 789, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xmv7krabbl/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 678, \"height\": 344, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xmv7krabbl/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 663, \"height\": 480, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xmv7krabbl/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1426, \"height\": 405, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xmv7krabbl/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1349, \"height\": 387, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xmv7krabbl/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1420, \"height\": 718, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xmv7krabbl/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1445, \"height\": 328, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-xmv7krabbl/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1141, \"height\": 764, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-xmv7krabbl/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1450, \"height\": 449, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xmv7krabbl/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1456, \"height\": 137, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xmv7krabbl/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1451, \"height\": 299, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-xmv7krabbl/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 852, \"height\": 302, \"label\": \"Table\"}]"
motivation: 现有动态GNN使用静态图，无法反映癫痫进展中的脑连接演化。
method: 提出时变图结构联合时空建模的动态图神经网络。
result: 在癫痫检测任务上取得更优性能，验证了动态建模的有效性。
conclusion: EvoBrain为理解脑状态动态变化提供了新的建模工具。
---

## Abstract
Dynamic GNNs, which integrate temporal and spatial features in Electroencephalography (EEG) data, have shown great potential in automating seizure detection.
However, fully capturing the underlying dynamics necessary to represent brain states, such as seizure and non-seizure, remains a non-trivial task and presents two fundamental challenges.
First, most existing dynamic GNN methods are built on temporally fixed static graphs, which fail to reflect the evolving nature of brain connectivity during seizure progression. 
Second, current efforts to jointly model temporal signals and graph structures and, more importantly, their interactions remain nascent, often resulting in inconsistent performance.
To address these challenges, we present the first theoretical analysis of these two problems, demonstrating the effectiveness and necessity of explicit dynamic modeling and time-then-graph dynamic GNN method.
Building on these insights, we propose EvoBrain, a novel seizure detection model that integrates a two-stream Mamba architecture with a GCN enhanced by Laplacian Positional Encoding, following neurological insights.
Moreover, EvoBrain incorporates explicitly dynamic graph structures, allowing both nodes and edges to evolve over time.
Our contributions include 
(a) a theoretical analysis proving the expressivity advantage of explicit dynamic modeling and time-then-graph over other approaches, 
(b) a novel and efficient model that significantly improves AUROC by 23\% and F1 score by 30\%, compared with the dynamic GNN baseline, and 
(c) broad evaluation of our method on the challenging early seizure prediction task.

---

## 论文详细总结（自动生成）

### 论文《EvoBrain: Dynamic Multi-Channel EEG Graph Modeling for Time-Evolving Brain Networks》详细中文总结

#### 1. 核心问题与整体含义（研究动机和背景）
- **研究动机**：癫痫发作本质上是脑网络动态紊乱，异常连接常作为发作标志。现有动态图神经网络（GNN）在自动癫痫检测中虽有潜力，但普遍存在两个根本挑战：
  - 大多方法采用**时不变静态图**，无法捕捉发作进程中脑连接随时间的演化；
  - 现有方法对**时间信号与图结构的联合建模以及二者交互**的探索不足，导致性能不稳定。
- **整体含义**：本文旨在通过理论分析和模型设计，证明**显式动态图建模**和**“时间-然后-图”（time-then-graph）架构**在表达脑网络动态方面的优势，并以此为基础提出高效、准确的癫痫检测与预测模型。

#### 2. 方法论：核心思想、关键技术细节
- **核心思想**：基于两个理论定理，EvoBrain采用**显式动态图结构**（每个时间片独立构建图）和**“时间-然后-图”处理流程**（先建模节点/边的时间演化，再对聚合后的静态图进行空间建模）。
- **关键技术细节**：
  1. **显式动态图构建**：
     - 对每个EEG快照（short-time segment），计算通道间归一化互相关的绝对值作为边权重，保留top-τ最高相关的邻居。
     - 得到时序加权有向图序列 `G = {A_{:,:,t}, X_{:,t}}`。
  2. **时序建模——双流Mamba**：
     - 分别用独立Mamba处理**节点特征**和**边特征**的时序序列。
     - Mamba作为选择性状态空间模型，通过输入依赖的参数实现类似神经调节的遗忘与更新机制，捕捉短/长期记忆。
  3. **空间建模——GCN + Laplacian Positional Encoding (LapPE)**：
     - 利用LapPE注入节点空间特异性（反映脑区功能定位），解决GNN对图自同构节点无法区分的局限。
     - 对聚合后的静态图应用多层GCN，最终通过最大池化和全连接层输出分类结果。
  4. **输入预处理**：对原始EEG信号执行短时傅里叶变换（STFT），取非负频率的对数振幅，并进行z归一化。
- **公式与算法流程（文字说明）**：
  - 快照级图构建：`a_{i,j,t} = |cross-corr(x_{i,:,t}, x_{j,:,t})|`（若v_j为v_i的top-τ邻居，否则0）。
  - Mamba更新（公式5）：`h_t = (1 - Δ_t·D) h_{t-1} + Δ_t·B_t x_t`，其中Δ_t等由输入决定。
  - 空间建模：`h^{(l+1)}_i = σ(D^{-1/2} A' D^{-1/2} h^{(l)}_j Θ^{(l)})`，其中A'由边特征经投影和softplus生成。
  - 分类：`Z = max-pool(H^{(L)}), logits = FC(Z), prob = softmax(logits)`。

#### 3. 实验设计
- **数据集与场景**：
  - **TUSZ v1.5.2**：最大公开癫痫EEG数据库，5,612个记录，3,050次标注发作，19通道。用于**发作检测**（区分发作与非发作）和**早期预测**（区分发作前1分钟与正常状态）。
  - **CHB-MIT**：844小时22通道头皮EEG，22名患者，163次发作。仅用于发作检测的辅助验证。
- **Benchmark**：对比方法涵盖传统机器学习（SVM、随机森林）、深度学习时序模型（LSTM、CNN-LSTM）、EEG基础模型（BIOT、LaBraM、EEGPT）以及四种动态GNN方法（EvolveGCN、DCRNN、GRAPHS4MER、GRU-GCN）。
- **评价指标**：AUROC和F1分数，所有结果基于5次不同随机种子运行的平均值。

#### 4. 资源与算力
- **计算设备**：NVIDIA A6000 GPU + Xeon Gold 6258R CPU。
- **训练配置**：Adam优化器，100个epoch，初始学习率1e-4，无dropout。
- **模型参数量**：EvoBrain约11.5万可训练参数（主模型约18.3万），远小于基础模型LaBraM（580万）和EEGPT（5122万）。
- **效率优势**：训练时间比DCRNN快**17倍**，推理时间快**14倍**（文献图4）。
- **说明**：文中未给出单个实验的精确时间或总GPU小时数，但提供了相对效率数据。

#### 5. 实验数量与充分性
- **实验组数**：
  - 主表（表1）：4个子任务（检测/预测 × 12s/60s窗口），每组带标准差。
  - 消融实验（图5）：架构对比、输入特征（频域 vs 原始）、LapPE、GNN层（GCN vs GIN vs 无GNN）、RNN层（Mamba vs GRU）影响。
  - 额外分析：动态/静态图对比（图3）、ROC曲线（图2）、计算效率（图4）、临床案例（图6）。
- **充分性评价**：实验覆盖了不同任务、不同时间窗口、两个独立数据集，并与多种传统/深度/基础模型公平比较；消融研究逐一验证了关键设计选择；理论分析与实验一致。整体设计较为充分、客观，但未在更多任务（如情绪识别）上验证泛化性，且预测任务依赖于固定的1分钟预发作定义。

#### 6. 主要结论与发现
- **理论结论**：
  - 显式动态图建模（时变邻接矩阵）严格表达性强于隐式静态图建模（Theorem 1）。
  - 在1-WL GNN框架下，时间-然后-图架构严格表达性强于时间-并-图，后者又强于图-然后-时间架构（Theorem 2）。
- **实验发现**：
  - EvoBrain在TUSZ发作检测任务中，AUROC比动态GNN基线EvolveGCN提升**23%**（0.670→0.865），F1提升**30%**（0.340→0.483），且优于所有对比方法（包括部分基础模型）。
  - 在早期预测任务上，EvoBrain同样取得最优（AUROC 13.8%提升）。
  - 动态图结构在所有动态GNN方法中均带来性能提升（图3），证明其必要性。
  - Mamba在长序列（60s）上优于GRU。

#### 7. 优点
- **理论贡献**：首次从图同构角度分析动态EEG时空建模的表达性，提供形式化定理和证明，为设计选择提供依据。
- **方法创新**：结合显式动态图、双流Mamba、LapPE，实现高效且符合神经科学观察的建模（临床案例显示正常、发作前、局部发作、全面发作的图结构差异符合认知）。
- **性能与效率兼顾**：在参数量远小于基础模型的情况下取得竞争甚至更优结果，且计算速度快（17×训练加速）。
- **任务拓展**：不仅检测发作，还成功应用于更具挑战的早期预测（提前1分钟），具有临床意义。

#### 8. 不足与局限
- **实验覆盖**：仅验证了癫痫检测/预测任务，未在其他EEG任务（如情绪识别、运动想象）上测试泛化性。
- **预测任务定义**：预发作窗口固定为1分钟，实际癫痫预发作期临床定义不明确，可能影响方法的普适性。
- **基线比较**：在预测任务上，EvoBrain虽优于其他GNN，但稍逊于大型预训练模型LaBraM（因参数量少），且未充分讨论与Cai et al. (2023)等最近工作的对比（后者虽提及但未在表1中出现）。
- **潜在偏差与风险**：
  - 模型可能对特定人口统计或医院数据产生偏差，导致泛化到不同群体时性能下降。
  - 系统故障或误判（尤其预测任务）可能引起误报，导致患者不必要的焦虑或不当干预。
- **临床实用性**：虽然案例可视化了癫痫扩散模式，但未提供正式的量化评估（如病灶定位准确率），尚需更严格的临床验证。

（完）
