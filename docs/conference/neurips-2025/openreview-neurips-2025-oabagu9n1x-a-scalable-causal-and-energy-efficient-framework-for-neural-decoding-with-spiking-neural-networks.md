---
title: "A Scalable, Causal, and Energy Efficient Framework for Neural Decoding with Spiking Neural Networks"
title_zh: 用于神经解码的可扩展、因果且节能的脉冲神经网络框架
authors: "Georgios Mentzelopoulos, Ioannis Asmanis, Konrad Kording, Eva L Dyer, Kostas Daniilidis, Flavia Vitale"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=oAbaGU9N1X"
tags: ["query:eeg"]
score: 8.0
evidence: 用于脑机接口神经解码的脉冲神经网络框架
tldr: 本文针对脑机接口中神经解码的计算效率问题，提出一种基于脉冲神经网络的可扩展、因果且节能的框架。该框架在保持高性能的同时显著降低能耗，适用于资源受限的实时BCI系统。方法虽不局限于EEG，但其因果性和低功耗特性直接服务于EEG BCI的应用需求。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-oabagu9n1x/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1382, \"height\": 602, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-oabagu9n1x/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1440, \"height\": 672, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-oabagu9n1x/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 756, \"height\": 307, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-oabagu9n1x/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1429, \"height\": 302, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-oabagu9n1x/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1443, \"height\": 316, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-oabagu9n1x/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 661, \"height\": 667, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-oabagu9n1x/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 813, \"height\": 422, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-oabagu9n1x/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1447, \"height\": 633, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-oabagu9n1x/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1439, \"height\": 312, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-oabagu9n1x/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1425, \"height\": 1207, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-oabagu9n1x/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1407, \"height\": 329, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-oabagu9n1x/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 853, \"height\": 343, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-oabagu9n1x/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1322, \"height\": 149, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-oabagu9n1x/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 858, \"height\": 316, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-oabagu9n1x/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 585, \"height\": 208, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-oabagu9n1x/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 793, \"height\": 208, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-oabagu9n1x/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 916, \"height\": 277, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-oabagu9n1x/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 899, \"height\": 275, \"label\": \"Table\"}]"
motivation: 现有神经解码器在实时性和能效上存在瓶颈，亟需适应资源受限BCI系统的方案。
method: 设计因果脉冲神经网络，通过时间编码和事件驱动实现低功耗在线解码。
result: 在多个神经数据集上达到竞争性能，能耗较人工神经网络降低数个数量级。
conclusion: SNN为BCI神经解码提供了有前途的节能、可扩展方案。
---

## Abstract
Brain-computer interfaces (BCIs) promise to enable vital functions, such as speech and prosthetic control, for individuals with neuromotor impairments. Central to their success are neural decoders, models that map neural activity to intended behavior. Current learning-based decoding approaches fall into two classes: simple, causal models that lack generalization, or complex, non-causal models that generalize and scale offline but struggle in real-time settings. Both face a common challenge, their reliance on power-hungry artificial neural network backbones, which makes integration into real-world, resource-limited systems difficult. Spiking neural networks (SNNs) offer a promising alternative. Because they operate causally (i.e. only on present and past inputs) these models are suitable for real-time use, and their low energy demands make them ideal for battery-constrained environments. To this end, we introduce **Spikachu: a scalable, causal, and energy-efficient neural decoding framework based on SNNs**. Our approach processes binned spikes directly by projecting them into a shared latent space, where spiking modules, adapted to the timing of the input, extract relevant features; these latent representations are then integrated and decoded to generate behavioral predictions. We evaluate our approach on 113 recording sessions from 6 non-human primates, totaling 43 hours of recordings. Our method outperforms causal baselines when trained on single sessions using between 2.26× and 418.81× less energy. Furthermore, we demonstrate that scaling up training to multiple sessions and subjects improves performance and enables few-shot transfer to unseen sessions, subjects, and tasks. Overall, Spikachu introduces a scalable, online-compatible neural decoding framework based on SNNs, whose performance is competitive relative to state-of-the-art models while consuming orders of magnitude less energy.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）

- **研究动机**：脑机接口（BCI）依靠神经解码器将神经活动映射为意图行为，但现有解码方法面临两难：简单的因果模型缺乏泛化能力，复杂的非因果模型虽能离线扩展却难以实时部署。两类方法都依赖高能耗的人工神经网络（ANN）骨干，难以集成到资源受限的植入式或边缘设备中。
- **研究目标**：提出一种同时满足**因果性（实时在线）**、**可扩展（跨会话、跨被试）** 和**高能效**的神经解码框架，以适用于电池约束的植入式BCI系统。脉冲神经网络（SNN）因其内在因果性和低能耗成为理想替代方案。

---

## 2. 方法论：核心思想、关键技术细节

### 核心思想
- 构建基于SNN的端到端框架 **Spikachu**：将离散的尖峰脉冲（binned spikes）投影到共享潜空间，通过多尺度并行SNN模块提取时序特征，再经脉冲自注意力捕获长程依赖，最后通过膜电位观测层输出连续的连续行为变量（如光标速度）。

### 关键技术细节
1. **单元令牌化与共享潜空间投影**：
   - 每个神经元单元（unit）被赋予一个可学习的32维嵌入向量。
   - 利用Perceiver编码器（交叉注意力）将变长输入序列投影为固定长度的潜变量（128维），再线性映射为128维的“虚拟单元”——该层权重跨会话、跨被试共享，实现对齐。

2. **多尺度脉冲特征提取**：
   - 将潜变量输入3个并行的脉冲MLP（各4层，输出256维），每个MLP的LIF神经元具有**可学习的衰减常数τ**（初始值分别为1.11、1.46、434.79），从而在不同时间尺度上捕获神经动态。

3. **脉冲自注意力（Spiking Self-Attention, SSA）**：
   - 采用Zhou等[55]提出的SSA机制，使用二进制尖峰进行Q、K、V投影，无softmax，计算效率更高。8头注意力，输入投影到512维。

4. **膜电位观测层**：
   - 使用从不发放脉冲的LIF神经元，直接输出膜电位值（连续），再通过线性层得到最终的2维速度预测（vx, vy）。

5. **整体训练**：
   - 损失函数为MSE（中心外任务中给运动阶段赋予5倍权重）。
   - 使用LAMB优化器，权重衰减1e-4，学习率2e-3，余弦退火。
   - 使用单元丢弃（unit dropout）数据增强，确保最小保留30个单元。

---

## 3. 实验设计

### 数据集
- **主数据集**：Perich et al. [36] 的公开数据集，包含4只NHP（猴C/J/M/T）共111个会话，CO和RT任务。另有2只NHP的2个会话来自Neural Latents Benchmark [37]（MC-RTT、MC-Maze）。**总计6只NHP、113个会话、43小时记录、超过1.1亿个尖峰、2000万个行为时点。**

### 基准方法与评估指标
- **对比方法**：MLP、GRU、LSTM、POYO（非因果）、POYO-causal（添加因果掩码）。
- **评估指标**：R²（解码性能）和每次推理能耗（μJ，基于FLOPs换算）。
- **评估协议**：CO和MC-Maze仅评估运动阶段，RT评估全部运动段；预测结果经20步移动平均平滑。

### 实验设置
- 单次训练：70%训练、10%验证、20%测试。
- 单会话模型训练1000轮，多会话模型训练400轮。
- 计算能耗时使用Horowitz[89]的MAC/AC能量常数（4.6 pJ / 0.9 pJ），并考虑SNN的尖峰稀疏性。

---

## 4. 资源与算力

- **GPU型号**：训练使用L40s、L40、A40、RTX 3090、A6000、2080 Ti、A10等NVIDIA GPU。
- **显存要求**：单会话模型<11GB；多会话模型使用48GB的A40。
- **训练时长**：单会话模型通常<1小时（少数2080 Ti上约5小时）；多会话模型（含Spikachu-mp）<48小时。
- **框架**：PyTorch + SpikingJelly（SNN组件）。

---

## 5. 实验数量与充分性

### 主要实验组（共约10组以上对比）
1. **单会话性能比较**（99个会话，CO和RT任务）——对比MLP/GRU/LSTM/POYO/POYO-causal。
2. **多会话预训练（Spikachu-mp）**：在99个会话上训练，再微调到单会话，评估性能与能效提升。
3. **跨被试迁移**：将Spikachu-mp迁移到猴T的12个未见会话（6 CO + 6 RT）。
4. **缩放律实验**：用20/49/75/99个会话预训练，再微调到**已见过会话、未见会话、未见被试**三种条件。
5. **跨任务/跨设置迁移**：迁移到MC-RTT和MC-Maze（不同动物、不同记录设备、不同任务）。
6. **消融实验**：逐个移除Multi-Scale I、SSA、Multi-Scale II等模块；以及将SNN替换为ANN（保持连接性）验证脉冲机制的作用。
7. **嵌入空间分析**：LDA/SVM分析单元嵌入在动物和任务上的可分性。
8. **FLOPs与内存访问分析**（附录F.5）。

### 充分性评价
- **充分且公平**：所有对比方法使用相同的训练/测试划分、平滑策略和能耗计算方法。多个独立会话提供了统计误差线（SEM）。
- **偏差风险**：数据集集中于运动皮层的猴实验，未覆盖人类或癫痫病灶等场景。SNN能耗估计基于FLOPs而非实际硬件测量。

---

## 6. 主要结论与发现

1. **单会话性能**：Spikachu在所有**因果模型**中取得最优R²（CO: 0.84, RT: 0.68），能耗比最接近的GRU低2.26倍，比POYO低418.81倍。
2. **多会话预训练**：Spikachu-mp（99会话）微调后R²提升至CO: 0.88, RT: 0.69，同时能耗进一步降低约2%。
3. **跨被试迁移**：从Spikachu-mp迁移到猴T，R²提升（CO: 0.76→0.78, RT: 0.66→0.68），能耗降低3.6%~3.7%，收敛速度加快3-4倍。
4. **缩放律**：预训练数据量越大，性能提升和能耗节省越显著。
5. **跨任务迁移**：迁移到MC-RTT和MC-Maze虽性能未显著提升，但收敛速度加快2.3~2.7倍，能耗降低2%~3%。
6. **消融证实**：LIF神经元的脉冲动力学是关键，单独连接不能解释性能；多尺度SNN模块贡献最大；SSA在扩展训练时体现重要。

---

## 7. 优点

- **首次将SNN与Transformer结合用于多会话、多被试的神经解码**，实现因果性、可扩展与能效的三重统一。
- **创新的“谱调器”（Harmonizer）**：通过可学习嵌入和交叉注意力对齐异构数据，可即插即用到任意现有模型（附录展示与LSTM/GRU/MLP结合仍有提升）。
- **多尺度脉冲模块**：可学习衰减常数使网络自动适应不同时间尺度的神经动态。
- **膜电位观测层**优雅地输出连续变量，避免传统SNN无法直接回归的问题。
- **实验全面**：覆盖多个物种、任务、跨被试/跨任务迁移、缩放律、消融、嵌入分析，验证了方法的鲁棒性。
- **能耗优势显著**：不仅FLOPs更低，内存访问也最少，适合真实植入场景。

---

## 8. 不足与局限

1. **能耗估算基于FLOPs**：未在实际神经形态芯片（如Loihi 2）上部署验证，真实能耗可能因硬件差异有偏差。
2. **仍依赖少量ANN组件**：Harmonizer（占参数量<15%但能耗占比高）不是全脉冲的，作者指出可用全脉冲注意力改进。
3. **数据集限制**：仅限运动皮层的猴数据，未评估在人类、其他脑区（如语言区）或非运动任务上的表现。
4. **跨任务迁移性能未显著提升**：在MC-RTT/MC-Maze上仅取得收敛加速，R²未优于从头训练，说明表示迁移在差异较大的设置下有上限。
5. **未进行在线实验**：虽然设计为因果，但实际在线验证（如实时闭环控制）尚未进行。
6. **模型规模固定**：为保持能效，多会话训练时未增加模型大小，可能限制了表示能力（对比POYO等使用更多参数）。
7. **训练细节中未报告随机种子及消融实验的统计显著性检验**（如t检验），仅报告均值±SEM。

（完）
