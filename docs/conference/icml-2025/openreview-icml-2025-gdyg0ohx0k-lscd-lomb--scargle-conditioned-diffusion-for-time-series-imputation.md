---
title: "LSCD: Lomb--Scargle Conditioned Diffusion for Time series Imputation"
title_zh: "LSCD: 基于Lomb-Scargle条件扩散的时间序列插补"
authors: "Elizabeth Fons, Alejandro Sztrajman, Yousef El-Laham, Luciana Ferrer, Svitlana Vyetrenko, Manuela Veloso"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=GdYg0Ohx0k"
tags: ["query:eeg-latent"]
score: 7.0
evidence: 扩散模型用于时间序列缺失数据插补，直接适用于EEG通道重建
tldr: 时间序列中缺失或不规则采样数据是常见难题。现有频域方法依赖均匀采样，需预插值导致频谱失真。本文提出LSCD，引入可微Lomb-Scargle层计算不规则采样信号的功率谱，并以此条件训练扩散模型用于插补。实验证明该方法在合成和真实基准上优于纯时域方法，可直接迁移至EEG缺失通道补全任务。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-gdyg0ohx0k/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 858, \"height\": 322, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-gdyg0ohx0k/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1768, \"height\": 621, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-gdyg0ohx0k/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 858, \"height\": 228, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-gdyg0ohx0k/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1776, \"height\": 709, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-gdyg0ohx0k/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1775, \"height\": 747, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-gdyg0ohx0k/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1815, \"height\": 1542, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-gdyg0ohx0k/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1779, \"height\": 769, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-gdyg0ohx0k/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1778, \"height\": 769, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-gdyg0ohx0k/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1778, \"height\": 772, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-gdyg0ohx0k/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1776, \"height\": 770, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-gdyg0ohx0k/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1777, \"height\": 773, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-gdyg0ohx0k/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1778, \"height\": 775, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-gdyg0ohx0k/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1777, \"height\": 773, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-gdyg0ohx0k/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1780, \"height\": 775, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-gdyg0ohx0k/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1781, \"height\": 809, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-gdyg0ohx0k/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1778, \"height\": 812, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-gdyg0ohx0k/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1781, \"height\": 833, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-gdyg0ohx0k/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1780, \"height\": 828, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-gdyg0ohx0k/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1753, \"height\": 601, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-gdyg0ohx0k/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1752, \"height\": 604, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-gdyg0ohx0k/fig-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 1752, \"height\": 604, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-gdyg0ohx0k/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1754, \"height\": 1049, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-gdyg0ohx0k/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1754, \"height\": 496, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-gdyg0ohx0k/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1226, \"height\": 252, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-gdyg0ohx0k/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 976, \"height\": 194, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-gdyg0ohx0k/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 961, \"height\": 194, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-gdyg0ohx0k/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1757, \"height\": 200, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-gdyg0ohx0k/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1679, \"height\": 289, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-gdyg0ohx0k/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1500, \"height\": 465, \"label\": \"Table\"}]"
motivation: 时间序列缺失数据插补中频域方法受均匀采样假设限制。
method: 提出Lomb-Scargle条件扩散模型，结合可微分频谱计算与分数匹配。
result: 在合成和真实数据上恢复缺失值更准确。
conclusion: LSCD为不规则采样时间序列插补提供了新方案，适用于EEG通道补全。
---

## Abstract
Time series with missing or irregularly sampled data are a persistent challenge in machine learning. Many methods operate on the frequency-domain, relying on the Fast Fourier Transform (FFT) which assumes uniform sampling, therefore requiring prior interpolation that can distort the spectra. To address this limitation, we introduce a differentiable Lomb--Scargle layer that enables a reliable computation of the power spectrum of irregularly sampled data.
We integrate this layer into a novel score-based diffusion model (LSCD) for time series imputation conditioned on the entire signal spectrum. 
Experiments on synthetic and real-world benchmarks demonstrate that our method recovers missing data more accurately than purely time-domain baselines, while simultaneously producing consistent frequency estimates. Crucially, our method can be easily integrated into learning frameworks, enabling broader adoption of spectral guidance in machine learning approaches involving incomplete or irregular data.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）

时间序列数据普遍存在缺失观测或不规则采样的问题，这给机器学习任务（如插补、预测）带来了挑战。现有频域方法（如基于FFT的TimesNet）依赖均匀采样的假设，因此必须对缺失值进行插值或补零预处理，这会导致频谱失真，尤其在高缺失率下更严重。相比之下，Lomb–Scargle周期图可以直接从不均匀采样数据中估计功率谱，无需插值，但此前在机器学习领域应用较少。本文提出Lomb–Scargle Conditioned Diffusion（LSCD），将可微分的Lomb–Scargle层集成到分数扩散模型中，以整个信号的频谱作为条件进行时间序列插补，旨在同时提升时域恢复精度和频域一致性。

### 2. 论文提出的方法论：核心思想、关键技术细节、公式或算法流程

- **核心思想**：构建一个在时域操作的扩散模型，但以Lomb–Scargle周期图（经FAP滤波、对数变换和归一化）作为额外条件输入，从而在去噪过程中引入频域信息；同时引入频谱一致性损失，强制最终插补结果与观测数据的频谱对齐。
- **关键技术**：
  - **可微Lomb–Scargle层**：给定观测时间点集合 \(s_i\) 和对应的值 \(x_{s_i}\)，按标准公式计算功率 \(P(\omega)\)，再通过假警报概率（FAP）过滤并加权。实现为PyTorch模块，支持批处理和掩码。
  - **频谱编码器 \(E_{\text{spec}}\)**：由两个多头自注意力层组成，分别沿频率维和特征维编码，输出潜在表示 \(z_S\)，在每个去噪步骤中与其它条件（观测值等）拼接。
  - **条件扩散框架**：
    - 前向过程：对目标部分 \(x^{\text{ta}}_0\) 逐步加噪，\(x^{\text{ta}}_t = \sqrt{\alpha_t} x^{\text{ta}}_{t-1} + \sqrt{1-\alpha_t}\epsilon_t\)。
    - 反向（去噪）过程：网络 \(\epsilon_\theta(x^{\text{ta}}_t, t \mid x^{\text{co}}_0, \text{LS}(x^{\text{co}}_0))\) 预测噪声，训练损失为 \(\mathcal{L}(\theta) = \mathbb{E}[\|\epsilon - \epsilon_\theta\|^2]\)。
  - **频谱一致性损失**：在训练后期微调阶段，利用完整的重构信号 \(\hat{x}_0\)（观测部分+插补部分）计算其Lomb–Scargle谱，与观测谱做MSE损失：\(\mathcal{L}_{\text{SCons}} = \|\text{LS}(x^{\text{co}}_0) - \text{LS}(\hat{x}^{\text{co}}_0)\|_2^2\)。
- **算法流程**：两阶段训练。第一阶段使用标准扩散损失优化；第二阶段加入频谱一致性损失微调，使最终输出保留观测数据的频谱特征。

### 3. 实验设计：使用了哪些数据集/场景，它的 benchmark 是什么，对比了哪些方法

- **数据集**：
  - **合成正弦波数据集**（Sines）：2000样本，5个通道，100时间步，每个通道由不同数量、频率和幅度的正弦波组成。初始已有10%随机缺失，再施加三种缺失机制（MCAR、序列缺失、块缺失），每种机制设10%/50%/90%目标缺失率（块缺失实际率因重叠而不同）。
  - **PhysioNet**：ICU患者生理测量数据，4000条记录，35个特征，48个时间步，自然约80%缺失。进一步随机选择10%/50%/90%观测值作为测试目标。
  - **PM2.5空气质量**（北京36站点）：5633样本，36个时间步，自然约13%缺失，仅评估10%缺失率下的插补。
- **基准方法**包括：**Mean**（均值插补）、**Lerp**（线性插值）、**BRITS**、**GP-VAE**、**US-GAN**、**TimesNet**、**CSDI**、**SAITS**、**ModernTCN**。
- **评估指标**：时域 MAE、RMSE（仅对人工移除的观测值计算）；频域 S-MAE（两个归一化功率谱的绝对差，仅用观测点计算谱）。
- **实验场景**：合成数据集3×3=9种缺失组合；PhysioNet 3种缺失率；PM2.5 1种缺失率；消融实验逐步移除三个组件（LS条件、频谱编码器、频谱一致性损失），共4种变体 × 4种场景。总计约13+组核心对比实验，外加多组可视化（频谱分布、PSD差异、值分布）。

### 4. 资源与算力

论文在附录C中说明了计算平台，但未详细列出训练总时长或GPU数量。具体信息如下：
- **硬件**：AWS g5.2xlarge 实例，CPU为AMD EPYC 7R32，GPU为Nvidia A10G 24 GB（推测为单卡）。
- **训练时间**（每epoch）：CSDI在PhysioNet上约10.30秒，PM2.5上约14.82秒；LSCD分别约11.18秒（+8.5%）和16.23秒（+9.5%）。
- **推理时间**（每batch，batch size=16）：CSDI在PhysioNet上约88.19秒，PM2.5上约69.36秒；LSCD分别约99.18秒（+13.3%）和78.58秒（+12.5%）。
- **总训练时间增加**：若计入频谱一致性损失微调阶段（需运行完整推理管线），两个数据集的总训练时间分别增加约43%和45%。
- 论文未明确说明训练总epoch数、总耗时或具体使用的多GPU设置，仅提供了相对时间开销。

### 5. 实验数量与充分性

- **实验数量**：在合成数据上覆盖9种缺失方案，真实数据覆盖4种缺失率（PhysioNet 3种、PM2.5 1种），对比了9种基线，并进行了完整的消融研究（4个变体×4个场景）和多组可视化。实验总量较为丰富。
- **充分性**：
  - 合成数据的设计合理，能控制频率真值，便于评估频谱恢复。
  - 真实数据涵盖两个领域（医疗、环境），且PhysioNet测试了三种缺失比例，展示了算法从低到高缺失率的鲁棒性。
  - 消融实验直接验证了每个组件的贡献。
  - 但存在一定不足：PM2.5只测试了10%缺失率，未包含50%/90%等更极端的设置；缺失机制仅测试MCAR、序列缺失、块缺失，未覆盖MAR、MNAR等非随机缺失模式；基准方法中缺少近期连续时间模型（如Latent ODE、Neural Flows、MADS）的比较。
- **公平性**：所有实验使用相同的数据划分和随机种子，指标计算严格遵守仅对目标值评估的规则，时域和频域指标分离，且频谱指标仅基于观测点计算。对比方法均采用各自官方或常用的超参数，整体公平性较好。

### 6. 论文的主要结论与发现

1. LSCD在所有测试场景下时域MAE/RMSE优于或持平于最强的基线CSDI，并在S-MAE上显著更低，说明频谱恢复更准确。
2. 在高达90%缺失率下，LSCD仍保持性能优势，尤其在频谱一致性方面。
3. 消融实验表明，移除Lomb–Scargle条件、频谱编码器或频谱一致性损失均会导致性能下降，其中去除LS条件的影响最大，证实了频谱条件的核心作用。
4. 可视化（如主导频率分布、PSD差异图）显示LSCD能更好地保留数据的频率结构，而其他方法（如TimesNet、SAITS）会出现频谱偏差或更大方差。
5. 提出的可微Lomb–Scargle层可以有效集成到学习框架中，且额外计算开销可控（训练+10-15%，含微调+43-45%）。

### 7. 优点：方法或实验设计上的亮点

- **方法创新**：首次将Lomb–Scargle周期图以可微分形式嵌入扩散模型条件，避免了FFT对均匀采样的强制要求，直接从稀疏观测中提取可靠频谱。
- **双重频谱利用**：一方面将编码后的频谱作为扩散条件引导生成，另一方面通过频谱一致性损失在后训练阶段强制对齐，有效兼顾时域精度与频域保真。
- **实现开放**：提供了完整的可微Lomb–Scargle PyTorch代码，降低了后续应用门槛。
- **实验设计亮点**：合成数据使用已知频率的波形，便于直接量化频谱恢复质量；在PhysioNet上测试三个缺失等级（10%/50%/90%）展示了鲁棒性；消融实验逐步剥离组件，验证了各自贡献。

### 8. 不足与局限

- **实验覆盖局限**：只讨论了MCAR、序列缺失、块缺失三种模式，未评估MAR或MNAR场景；PM2.5仅测了10%缺失率，未在高缺失率下验证；未与连续时间模型（如Latent ODE、Neural Flows、GRU-ODE-Bayes）对比，而这些方法在处理不规则采样时具有理论优势。
- **潜在偏差风险**：Lomb–Scargle基于正弦拟合假设，虽然作为条件可能不引入偏差，但频谱一致性损失会偏离分数匹配最优解，可能产生有偏的生成（论文本身也承认这一点）。
- **应用限制**：当前LSCD基于固定网格运行，不能直接处理完全不规则的时间点（需事先知道插值时间）；而连续时间方法在训练和推理时均能自然地适应不规则采样。
- **计算开销**：虽然相对增加不大，但加上微调阶段后总训练时间增加约45%；推理阶段比CSDI慢约13%，对于实时应用可能需要注意。
- **资源说明不足**：未提供总训练时间（小时数）、多GPU并行情况、超参数搜索细节等，影响复现性。

（完）
