---
title: Flow Matching for Few-Trial Neural Adaptation with Stable Latent Dynamics
title_zh: 用于少试次神经适应且具有稳定潜动力学的流匹配方法
authors: "Puli Wang, Yu Qi, Yueming Wang, Gang Pan"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=nKJEAQ6JCY"
tags: ["query:eeg"]
score: 8.0
evidence: 基于流的分布对齐用于脑机接口中少试次神经适应
tldr: 本文针对脑机接口（BCI）跨天神经信号非平稳性导致性能下降的问题，提出基于流匹配的分布对齐框架（FDA），通过稳定潜空间动力学实现少试次下的高效神经适应。实验表明，该方法在少量校准试次下显著提升了跨天解码性能，为实际BCI部署提供了可行方案。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-nkjeaq6jcy/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 690, \"height\": 645, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nkjeaq6jcy/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1747, \"height\": 474, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nkjeaq6jcy/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 723, \"height\": 503, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nkjeaq6jcy/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 731, \"height\": 637, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nkjeaq6jcy/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1774, \"height\": 639, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nkjeaq6jcy/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1772, \"height\": 803, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nkjeaq6jcy/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1764, \"height\": 379, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nkjeaq6jcy/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1762, \"height\": 902, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nkjeaq6jcy/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1072, \"height\": 400, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nkjeaq6jcy/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1413, \"height\": 461, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nkjeaq6jcy/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1409, \"height\": 474, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nkjeaq6jcy/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1781, \"height\": 547, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nkjeaq6jcy/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1765, \"height\": 722, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-nkjeaq6jcy/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1757, \"height\": 613, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 862, \"height\": 751, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1761, \"height\": 757, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 845, \"height\": 237, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 841, \"height\": 127, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 851, \"height\": 263, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 719, \"height\": 134, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 580, \"height\": 209, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 927, \"height\": 207, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 928, \"height\": 208, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1749, \"height\": 520, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1762, \"height\": 181, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 991, \"height\": 164, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1591, \"height\": 168, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 579, \"height\": 161, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1753, \"height\": 219, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1129, \"height\": 164, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 512, \"height\": 128, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1310, \"height\": 233, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1747, \"height\": 192, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1750, \"height\": 193, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 905, \"height\": 165, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 905, \"height\": 165, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 924, \"height\": 165, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-nkjeaq6jcy/table-024.webp\", \"caption\": \"\", \"page\": 0, \"index\": 24, \"width\": 999, \"height\": 202, \"label\": \"Table\"}]"
motivation: 解决BCI跨天神经信号非平稳性，现有对齐方法在少试次时不稳定。
method: 提出流匹配分布对齐（FDA），利用潜空间流匹配实现跨天分布对齐。
result: 在少试次下实现稳定高效的神经适应，优于现有对齐方法。
conclusion: FDA提升了BCI实际部署中的鲁棒性和实用性。
---

## Abstract
The primary goal of brain-computer interfaces (BCIs) is to establish a direct linkage between neural activities and behavioral actions via neural decoders. Due to the nonstationary property of neural signals, BCIs trained on one day usually obtain degraded performance on other days, hindering the user experience. Existing studies attempted to address this problem by aligning neural signals across different days. However, these neural adaptation methods may exhibit  instability and poor performance when only a few trials are available for alignment, limiting their practicality in real-world BCI deployment. To achieve efficient and stable neural adaptation with few trials, we propose Flow-Based Distribution Alignment (FDA), a novel framework that utilizes flow matching to learn flexible neural representations with stable latent dynamics, thereby facilitating source-free domain alignment through likelihood maximization. The latent dynamics of FDA framework is theoretically proven to be stable using Lyapunov exponents, allowing for robust adaptation. Further experiments across multiple motor cortex datasets demonstrate the superior performance of FDA, achieving reliable results with fewer than five trials. Our FDA approach offers a novel and efficient solution for few-trial neural data adaptation, offering significant potential for improving the long-term viability of real-world BCI applications.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：脑机接口（BCI）解码器因神经信号的非平稳性（行为变异、生理变化、电极退化等），跨天使用时性能大幅下降。现有神经适应方法（如NoMAD、Cycle-GAN、ERDiff）在仅有少量试次（如小于5个试次）可用于校准时，表现不稳定甚至负迁移，限制了实际BCI的长期部署。
- **整体含义**：本文旨在设计一种能够在极少校准试次下实现高效、稳定跨天神经适应的框架，以提高BCI在实际应用中的鲁棒性和可用性。

### 2. 论文提出的方法论：核心思想、关键技术细节

- **核心思想**：提出Flow-Based Distribution Alignment（FDA），利用条件流匹配（Conditional Flow Matching）学习灵活的神经表示，并保证潜动力学稳定性，从而通过似然最大化实现源无关的域对齐。
- **两阶段框架**：
  - **预训练阶段**（监督学习）：
    - 使用Transformer（`fα`）从原始神经信号（短时窗口）中提取条件特征`c`。
    - 构建从标准高斯噪声`z(0)`到目标神经表示`z(1)`的连续归一化流，`z(1)`由行为标签线性映射得到：`z(1) = ηy`。
    - 流路径采用线性插值：`z(τ) = (1-τ)z(0) + τz(1)`，对应的速度场`u = z(1)-z(0)`。
    - 用MLP（带残差连接、Lipschitz连续激活函数）参数化向量场`vθ`，通过条件流匹配损失`Lcfm`训练。
    - 理论证明：该潜动力学是稳定的（Lyapunov指数非正），因为MLP残差结构中的尺度系数被约束在(0,1)，且激活函数的Lipschitz连续性确保状态偏差呈几何级数衰减（Theorem 3.1）。
  - **微调阶段**（无监督适应）：
    - 固定流网络`vθ`，仅微调特征提取器`fα`。
    - 两种对齐策略：
      - **FDA-MMD**：最小化源域和目标域`z(1)`分布之间的最大均值差异（MMD），需要源数据。
      - **FDA-MLA**（源无关）：通过直接最大化目标域的对数似然（利用变量变化公式或Hutchinson迹估计器）实现对齐，无需源样本。
- **算法流程**（Algorithm 1）：输入源域DS和目标域DT，先预训练`fα`和`vθ`（n_pre-train=3500 epochs），然后在固定`vθ`的情况下微调`fα`（n_fine-tune=25 epochs），根据所选对齐策略更新`α`。

### 3. 实验设计：数据集、场景、对比方法

- **数据集**：三个来自非人灵长类初级运动皮层（M1）的细胞外神经记录：
  - CO-C（猴子C中心外出任务）
  - CO-M（猴子M中心外出任务）
  - RT-M（猴子M随机目标任务）
- **场景设置**：选取一天作为源域DS（约200个试次），其他天数作为目标域DT，无标签。目标试次数通过比例r控制，主要考察极低比例：r=0.02（≤5个试次），也测试了0.03、0.04、0.06。
- **对比方法**：
  - LSTM（无对齐基线）
  - CEBRA（无对齐的潜变量工具）
  - ERDiff（基于扩散模型和VAE的潜动力学对齐）
  - NoMAD（基于LFADS和KL散度的对齐）
  - Cycle-GAN（全维信号空间的对齐）
- **评估指标**：R²得分（解码二维光标速度的拟合优度）。
- **统计设置**：每个源域预训练使用5个随机种子，每个目标域试次选择进行25次随机采样，结果取均值和标准差。

### 4. 资源与算力

- 论文明确提到：训练硬件为NVIDIA GeForce RTX 3080 Ti（12GB），单卡。
- 给出训练时间对比：FDA预训练约99秒，微调约2.3秒；总参数量0.03M；推理时间约4ms。
- 未说明使用的GPU数量（推测单卡）、未提及多卡并行或其他GPU型号对比。

### 5. 实验数量与充分性

- **实验数量**：
  - 三个数据集，每个数据集约10个目标天，共约30个目标会话。
  - 目标比例r从0.02到0.06的多种设置；另外对r=0.1~0.6也有补充分析。
  - 消融实验：对比不同对齐策略（FDA-t, FDA-g, FDA-c）、不同流路径（VP, GVP）、不同特征提取器（MLP、时序注意力）、稳定性变体（去除激活函数或尺度系数）、附加重建损失（FDA-re）。
  - 额外实验：零样本性能、最大Lyapunov指数（MLE）计算、模拟数据（Lorenz吸引子）恢复潜变量、超参数敏感性（窗口大小、潜维度、采样步数）、试次多样性分析等。
- **充分性与公平性**：实验覆盖了主要场景，对比方法与原文设置保持一致；随机种子和多次采样降低了偶然性；消融实验验证了各组件的必要性；稳定性理论得到MLE计算的佐证。但部分基线（NoMAD、Cycle-GAN）在少试次下性能极差，与原文报道的高试次结果形成对比，体现了方法在极低数据量下的差异。

### 6. 论文的主要结论与发现

- FDA在少试次（<5个试次）条件下显著优于所有对比方法，R²提升约15%以上（如CO-M数据集平均45.59% vs NoMAD约20%、Cycle-GAN约15%）。
- 潜动力学的稳定性（非正Lyapunov指数）被理论和实验验证，且是提升少试次鲁棒性的关键。
- FDA-MLA（源无关）性能略低于FDA-MMD，但仍优于大多数基线，适合隐私敏感场景。
- 消融表明：流匹配框架、Lipschitz连续激活函数和尺度系数约束对稳定性至关重要；非线性流路径（VP/GVP）和简单特征提取器（MLP）会降低性能。
- 当目标试次增加至约60（r≈0.3）时，Cycle-GAN和NoMAD性能与FDA接近，但FDA在极低试次下优势明显。

### 7. 优点：方法与实验设计的亮点

- **方法创新**：首次将流匹配引入BCI神经适应，避免了以往方法对潜变量分布的先验假设（如高斯），适应更灵活的分布。
- **理论保证**：严格证明了潜动力学的稳定性，提供了可解释性和可靠性。
- **实用高效**：微调仅需2~3秒，推理4ms，满足实时BCI要求。
- **源无关选项**：FDA-MLA无需源数据，保护隐私，便于实际部署。
- **实验设计细致**：广泛覆盖多数据集、多目标天数、多比例，消融充分，并加入了模拟数据验证。

### 8. 不足与局限

- **实验覆盖局限**：所有实验均来自同一主体，且神经元群体有较高重叠；跨主体、跨任务、神经元子集不重叠的场景未验证。
- **异常表现**：在CO-C数据集上，FDA在某些目标天（如Day10）性能接近于零，说明对不同动物的泛化存在差异；FDA-MLA在CO-M Day8出现NLL异常升高现象。
- **基线的旧版本**：NoMAD实现基于公开的lfads-torch，可能与原文版本有差异；ERDiff使用最新release，但少试次下存在梯度爆炸导致提前停止。
- **与大规模预训练模型对比有限**：仅附录中与NDT-2做了零样本对比，未充分展示FDA在与自监督预训练结合时的潜力。
- **临床数据缺失**：仅使用非人灵长类数据，人类临床数据验证尚待未来研究。
- **高试次场景优势减弱**：当目标试次增加至60以上时，FDA与Cycle-GAN/NoMAD性能接近，说明FDA的优势集中在极端少试次场景。

（完）
