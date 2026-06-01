---
title: Flow-field inference from neural data using deep recurrent networks
title_zh: 利用深度循环网络从神经数据推断流场
authors: "Timothy Doyeon Kim, Thomas Zhihao Luo, Tankut Can, Kamesh Krishnamurthy, Jonathan W. Pillow, Carlos D Brody"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=ZLC4B9oQWX"
tags: ["query:eeg"]
score: 4.0
evidence: 深度循环网络用于神经群体动力学推断
tldr: 该论文提出FINDR方法，利用深度循环网络无监督地从神经脉冲序列推断低维非线性随机流场，捕捉个体神经元异质响应。该方法可应用于EEG信号处理，用于提取EEG中复杂的时序动态特征，支持EEG信号重建和分析。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-zlc4b9oqwx/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1587, \"height\": 927, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zlc4b9oqwx/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1546, \"height\": 1258, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zlc4b9oqwx/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1498, \"height\": 1123, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zlc4b9oqwx/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1770, \"height\": 775, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zlc4b9oqwx/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1061, \"height\": 438, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zlc4b9oqwx/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1720, \"height\": 848, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zlc4b9oqwx/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 768, \"height\": 417, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zlc4b9oqwx/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1788, \"height\": 1299, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zlc4b9oqwx/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1425, \"height\": 1669, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zlc4b9oqwx/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1420, \"height\": 792, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zlc4b9oqwx/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1466, \"height\": 805, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zlc4b9oqwx/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1794, \"height\": 283, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zlc4b9oqwx/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1714, \"height\": 960, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zlc4b9oqwx/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1711, \"height\": 327, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zlc4b9oqwx/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1190, \"height\": 546, \"label\": \"Figure\"}]"
motivation: 神经群体动力学估计困难，现有方法局限。
method: 设计无监督深度循环网络，学习低维流场并分离任务相关和无关活动。
result: 在老鼠前额叶数据上媲美现有方法，并成功分离任务相关活动。
conclusion: FINDR为神经数据分析提供了有效的动力学推断工具，可拓展至EEG。
---

## Abstract
Neural computations underlying processes such as decision-making, working memory, and motor control are thought to emerge from neural population dynamics. But estimating these dynamics remains a significant challenge. Here we introduce Flow-field Inference from Neural Data using deep Recurrent networks (FINDR), an unsupervised deep learning method for inferring low-dimensional, nonlinear, stochastic dynamics underlying neural population activity. Using spike train data from frontal brain regions of rats performing an auditory decision-making task, we demonstrate that FINDR performs competitively with existing methods in capturing the heterogeneous responses of individual neurons. When trained to disentangle task-relevant and irrelevant activity, FINDR uncovers interpretable low-dimensional dynamics. These dynamics can be visualized as flow fields and attractors, enabling direct tests of attractor-based theories of neural computation. We suggest FINDR as a powerful method for revealing the low-dimensional task-relevant dynamics of neural populations and their associated computations.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）
- **问题背景**：神经科学认为，决策、工作记忆、运动控制等认知功能源自神经群体的低维动力学。但如何从记录到的神经脉冲序列中准确推断这些动力学仍是一个重大挑战。
- **现有方法局限**：已有方法对动力学做了强假设（如自洽、线性、分段线性、确定性、高维等），导致难以学习某些复杂非线性随机系统，且多数方法未明确区分任务相关与任务无关成分。
- **本文贡献**：提出 **FINDR**（Flow-field Inference from Neural Data using deep Recurrent networks），一个无监督深度学习方法，能够从脉冲序列推断低维、非线性、随机动力学，并可视化流场和吸引子，直接检验基于吸引子的神经计算理论。

### 2. 论文提出的方法论
- **核心思想**：将神经群体动力学建模为隐状态的低维随机微分方程（SDE），并通过顺序变分自编码器（sequential VAE）框架同时完成隐轨迹推理和流场学习。
- **关键技术细节**：
  - **观测模型**：低维隐变量 \(z_t \in \mathbb{R}^L\) 通过线性映射加 softplus 输出各神经元的发放率 \(\lambda_t = \text{softplus}(C z_t + d_t)\)，其中 \(d_t\) 为任务无关时变偏置。
  - **动力学模型（先验）**：采用门控 MLP 参数化的漂移函数 \(\mu(z, u)\)：
    \[
    z_t = z_{t-1} + \frac{\Delta t}{\tau} \mu(z_{t-1}, u_t) + \sqrt{\frac{\Delta t}{\tau}} \xi_t,\quad \xi_t \sim \mathcal{N}(0, \Sigma)
    \]
    其中 \(\mu(z, u) = \sigma(G(z, u)) \odot [-z + F(z, u)]\)，\(F\) 和 \(G\) 均为 MLP，通过门控机制提高表达能力和可训练性。
  - **变分后验（编码器）**：使用双向 GRU 处理整个序列 \([u_t; y_t]\) 得到 \(e_t\)，然后用类似门控 SDE 的形式（\(\tilde{F}, \tilde{G}\)）估计后验轨迹。
  - **训练目标**：最小化损失 \(\tilde{\mathcal{L}} = \sum_t [-\log p(y_t|z_t, d_t) + \beta D_{\text{KL}}]\), 其中 \(\beta=2\) 以强调动力学推断。
  - **后处理可识别性**：对加载矩阵 \(C\) 进行 SVD 并旋转隐空间，使距离与角度在逆 softplus 率空间和隐空间等价，保证可识别性（至多相差正交变换）。

### 3. 实验设计
- **合成数据实验**：
  - 基于 \(n\)-bit flip-flop 任务生成不同几何的连续吸引子（圆盘、矩形、三维棱柱），模拟 500 个泊松发放神经元，600 训练 + 200 验证 + 200 测试试次。
  - 训练 FINDR 假设不同隐维度 \(L=1,\dots,6\)，评估归一化对数似然和 PCA 解释方差。
- **真实数据实验**：
  - **数据集**：大鼠背内侧前额叶皮层（dmFC）和内侧前额叶皮层（mPFC）的 464 个神经元（其中 67 个选择相关神经元）在听觉决策任务中的脉冲序列（448 试次）。任务：听左右随机点击声，转向点击多的一侧。
  - **预处理**：按 10ms 分箱，对齐刺激起始，提供左右点击数作为外部输入 \(u\)。
  - **评价指标**：5 折交叉验证下的（1）归一化对数似然差（co-smoothing）、（2）证据条件化 PSTH \(R^2\)。
  - **对比方法**：SLDS、rSLDS、autoLFADS、GPFA，以及 CEBRA（仅用于流形可视化对比）。
- **额外分析**：跨折叠一致性检验（Pearson \(|r|\)）、消融实验（移除任务无关偏置）、不同随机种子和次优超参的稳定性。

### 4. 资源与算力
- **文中未明确说明 GPU 型号、数量或训练时长**。仅在致谢中提及使用了普林斯顿大学的高性能计算集群（HPC）。附录 A.1.5 提到训练 3000 个 epoch，使用 mini-batch 梯度下降和 warm restart 学习率调度，但未给出具体硬件信息。

### 5. 实验数量与充分性
- **实验数量**：涵盖合成数据上的多个几何（圆盘、矩形、三维棱柱）和维度测试；真实数据上多 latent 维度（\(L=1,\dots,6\)）与 5 个对比方法全面比较；跨折叠一致性分析（5 折）；消融实验（是否学习任务无关成分）；不同随机种子和次优超参验证；额外与 autoLFADS 和 CEBRA 的对比。
- **充分性与公平性**：
  - 采用标准交叉验证和公认评估指标（co-smoothing, PSTH \(R^2\)）。
  - 对每个对比方法进行了超参搜索（如 SLDS/rSLDS 的状态数、autoLFADS 的超参），并按最优结果比较。
  - 消融实验揭示了任务无关成分的重要性。
  - **不足**：真实数据仅使用了一个任务（大鼠听觉决策）的一个脑区数据集，覆盖面有限；未在多个独立数据集或不同物种/任务上验证泛化性。

### 6. 论文的主要结论与发现
- FINDR 在合成数据上能准确恢复已知的连续吸引子结构（圆盘、矩形、三维棱柱），并正确推断隐维度。
- 在真实大鼠前额叶数据上，FINDR 在低维（\(L \le 3\)）时 held-out 对数似然和 PSTH \(R^2\) 显著优于 SLDS、rSLDS、autoLFADS、GPFA；在较高维度时性能相当。
- FINDR 发现的 2 维动力学流场在 5 折交叉验证中高度一致，并稳定出现两个慢点（slow points），分别对应左/右选择偏好，支持吸引子理论。
- 相比 autoLFADS，FINDR 的隐空间不仅拓扑一致，而且几何（距离）保持一致性，有利于解释。
- 明确分离任务无关偏置 \(d_t\) 对获得一致、可解释的动力学至关重要。

### 7. 优点
- **动力学灵活性**：使用门控 MLP 作为漂移函数，能表达高度非线性随机系统，优于线性或分段线性假设。
- **可控可解释**：通过区分任务相关（低维隐状态）与任务无关（时变偏置）活动，所得动力学更易关联行为，并能直接可视化流场和吸引子。
- **低维高效**：仅用 2-3 个隐维度即可充分描述数据，比 autoLFADS（常需 20+ 因子）更简洁。
- **跨折叠几何一致性**：相比 autoLFADS 和 CEBRA，FINDR 不仅拓扑稳定，几何性质（距离）也保持，有利于定量分析与比较。
- **通用扩展性**：框架适用于多种神经计算场景（如运动控制、视觉等），且支持 SDE 噪声建模来自我步长变化。

### 8. 不足与局限
- **数据需求**：作为深度学习方法，需要大量同时记录的神经元和重复试次；若神经元数或试次数不足，性能可能下降。
- **未提供不确定性**：文中指出未来可结合高斯过程等方法量化流场推断的不确定性。
- **可变试次长度**：当前 FINDR 假设所有试次等长，不支持可变长度（部分对比方法有此限制）。
- **一致性无理论保证**：虽实验上跨折叠一致，但论文承认尚未从理论上证明，新数据集上需再验证。
- **真实数据验证单一**：仅在一个大鼠决策数据集上展示，未在多物种、多任务（如运动皮层、视觉皮层）上测试，泛化性待检验。
- **计算开销**：训练需要 BPTT 和调参（学习率、隐藏单元数等），尽管未具体报告时间，但 deep VAE 训练通常较慢。

（完）
