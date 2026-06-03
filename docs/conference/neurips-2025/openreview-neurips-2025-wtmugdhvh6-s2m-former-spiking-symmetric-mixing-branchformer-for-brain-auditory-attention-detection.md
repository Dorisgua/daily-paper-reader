---
title: "S$^2$M-Former: Spiking Symmetric Mixing Branchformer for Brain Auditory Attention Detection"
title_zh: "S2M-Former: 用于脑听觉注意检测的尖峰对称混合分支former"
authors: "Jiaqi Wang, Zhengyu Ma, Xiongri Shen, Chenlin Zhou, Leilei Zhao, Han Zhang, Yi Zhong, Siqi Cai, Zhenxi Song, Zhiguo Zhang"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=WtMuGdHvh6"
tags: ["query:eeg"]
score: 4.0
evidence: 基于EEG的听觉注意检测，使用尖峰神经网络
tldr: 该论文提出S2M-Former尖峰对称混合框架，利用空间和频率分支并行处理EEG特征，实现节能高效的听觉注意检测，在多个数据集上取得先进性能。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-wtmugdhvh6/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 661, \"height\": 321, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-wtmugdhvh6/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1444, \"height\": 1102, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-wtmugdhvh6/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 571, \"height\": 969, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-wtmugdhvh6/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1438, \"height\": 492, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-wtmugdhvh6/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 630, \"height\": 783, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-wtmugdhvh6/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1451, \"height\": 390, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-wtmugdhvh6/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 584, \"height\": 503, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-wtmugdhvh6/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 635, \"height\": 538, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-wtmugdhvh6/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 698, \"height\": 451, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-wtmugdhvh6/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1441, \"height\": 213, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-wtmugdhvh6/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1402, \"height\": 788, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-wtmugdhvh6/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1402, \"height\": 781, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-wtmugdhvh6/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1441, \"height\": 430, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-wtmugdhvh6/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 942, \"height\": 315, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-wtmugdhvh6/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 946, \"height\": 263, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-wtmugdhvh6/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1383, \"height\": 570, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-wtmugdhvh6/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1438, \"height\": 413, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-wtmugdhvh6/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1438, \"height\": 422, \"label\": \"Table\"}]"
motivation: 现有EEG听觉注意检测方法难以充分利用互补特征并满足能效约束。
method: 提出尖峰驱动对称架构，包含并行空间和频率分支，使用生物启发式token-通道混合器。
result: 在听觉注意检测任务上实现了高精度且低能耗。
conclusion: 为神经导向助听设备提供了高效的EEG解码方案。
---

## Abstract
Auditory attention detection (AAD) aims to decode listeners' focus in complex auditory environments from electroencephalography (EEG) recordings, which is crucial for developing neuro-steered hearing devices.  Despite recent advancements, EEG-based AAD remains hindered by the absence of synergistic frameworks that can fully leverage complementary EEG features under energy-efficiency constraints. We propose ***S$^2$M-Former***, a novel ***s***piking ***s***ymmetric ***m***ixing framework to address this limitation through two key innovations:  i)   Presenting a spike-driven symmetric architecture composed of parallel spatial and frequency branches with mirrored modular design, leveraging biologically plausible token-channel mixers to enhance complementary learning across branches; ii) Introducing lightweight 1D token sequences to replace conventional 3D operations, reducing parameters by 14.7$\times$. The brain-inspired spiking architecture further reduces power consumption, achieving a 5.8$\times$ energy reduction compared to recent ANN methods, while also surpassing existing SNN baselines in terms of parameter efficiency and performance. Comprehensive experiments on three AAD benchmarks (KUL, DTU and AV-GC-AAD) across three settings (within-trial, cross-trial and cross-subject) demonstrate that S$^2$M-Former achieves comparable state-of-the-art (SOTA) decoding accuracy, making it a promising low-power, high-performance solution for AAD tasks. Code is available at https://github.com/JackieWang9811/S2M-Former.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）

- **研究动机**：脑听觉注意力检测（Auditory Attention Detection, AAD）旨在从脑电图（EEG）信号中解码听者在嘈杂环境（鸡尾酒会效应）中关注的说话人，这对于开发神经驱动型助听器等脑机接口（BCI）应用至关重要。  
- **现有挑战**：当前基于EEG的AAD方法面临双重瓶颈：(1) 缺乏能同时利用空间和频率互补特征的高效协同框架；(2) 现有双分支网络（如DBPNet、M-DBPNet）采用简单拼接或求和进行特征融合，忽略分支间的互补学习；且计算开销大（如使用3D卷积），难以满足低功耗可穿戴设备的需求。  
- **整体含义**：本文提出一种新型尖峰驱动对称混合框架S²M-Former，在保持高精度的同时大幅降低参数和能耗，为神经形态低功耗AAD提供可行方案。

---

### 2. 论文提出的方法论：核心思想、关键技术细节

#### 核心思想
- 采用**尖峰对称混合架构**，包含并行的空间分支和频率分支，通过镜像模块设计实现分支间互补学习；  
- 以轻量级1D令牌序列替代传统3D操作，降低计算复杂度；  
- 全尖峰驱动（spike-driven）机制，利用Leaky Integrate-and-Fire (LIF) 和改进的**通道参数化LIF (CPLIF)** 神经元，实现稀疏、低功耗计算。

#### 关键技术细节
1. **特征提取**：
   - **空间分支**：使用公共空间模式（CSP）提取时空特征 E<sub>S</sub> ∈ R<sup>C×T</sup>；  
   - **频率分支**：提取差分熵（DE）特征并映射为5频带二维拓扑图 E<sub>F</sub> ∈ R<sup>5×H×W</sup>。
2. **分支编码器**：
   - **SBE（空间分支编码器）**：级联时间卷积（T Conv2d）和双路径空间卷积（SConv2d），捕捉时空依赖；  
   - **FBE（频率分支编码器）**：利用膨胀卷积（dilation=2）扩增感受野，逐步压缩通道维度，保留频率-空间模式。
3. **S²M模块**：
   - **SCSA（尖峰通道自注意力）**：通道式自注意力（复杂度从O(N²D)降至O(ND²)），分别建模电极间关系（空间分支）或频带间关系（频率分支）；  
   - **SMSC（尖峰多尺度可分离卷积）**：三个并行深度卷积（核大小1,3,5）提取多尺度局部模式，后接通道混洗增强跨尺度交互；  
   - **SGCM（尖峰门控通道混合器）**：拼接两分支特征后，通过门控机制计算通道注意力向量，调制关键值，实现自适应跨分支融合；  
   - **MPTM（膜电位感知令牌混合器）**：利用全局平均池化聚合各分支表征，按比例混合生成引导表示，通过残差调制与原始特征融合，最后拼接最大池化结果压缩令牌数。
4. **分类头**：融合后的D维嵌入经全连接层输出二分类预测。

#### 关键公式
- CPLIF膜电位更新：  
  H[t,c,n] = V[t−1,c,n] + (1/τ<sub>l</sub>[c]) (X[t,c,n] − (V[t−1,c,n] − V<sub>reset</sub>)) + β[c]  
  其中τ<sub>l</sub>、β为可学习通道向量。

---

### 3. 实验设计：数据集、基准、对比方法

- **数据集**：三个公开AAD基准：
  - KUL（16名受试者，听觉刺激，时长12.8小时）  
  - DTU（18名受试者，听觉刺激，时长15小时）  
  - AV-GC-AAD（11名受试者，视听刺激，时长14.7小时）
- **评估设置**：
  - Within-trial（单试次内划分训练/验证/测试）  
  - Cross-trial（随机划分试次，无重叠测试）  
  - Cross-subject（留一受试者交叉验证）
- **决策窗口**：0.1s、1s、2s（带50%重叠滑动窗口）。
- **对比方法**：
  - 单分支方法：SSF-CNN、MBSSFCC、DARNet  
  - 双分支方法：DBPNet、M-DBPNet  
  - 尖峰网络基线：QKFormer、Spike-driven Transformer、Spikformer（仅频率分支对比）
- **评价指标**：平均分类准确率±标准差。

---

### 4. 资源与算力

- **硬件**：单张NVIDIA GeForce RTX 4090 GPU。  
- **训练配置**：Adam优化器，学习率1e-3（KUL within-trial）/5e-4（其他），批次大小32（受试者依赖）/128（受试者独立），训练300轮，early stopping（25轮无改善）。  
- **时间步**：默认为4（TS=4），所有实验在此设置下进行。  
- **未明确说明**：单次训练具体时长（分钟/小时）及GPU数量（仅1张）。

---

### 5. 实验数量与充分性

- **实验数量**：  
  - 主表（Table 2、Table 3）：三个数据集 × 三种决策窗口 × 两种设置（within-trial、cross-trial）共18个条件，对比5种基线。  
  - 消融研究（Table 4、Table 8、Table 9）：包含ANN对照、CPLIF替换为LIF、移除SGCM+MPTM、单分支、与3种SNN骨干对比，涵盖DTU、KUL、AV-GC。  
  - 交叉受试者实验（Table 6）：KUL和DTU的LOSO验证。  
  - 参数/能耗对比（Table 5）。  
  - 额外的可视化分析（Figure 3–9）及时步/发放率分析（Figure 8）。
- **充分性与公平性**：  
  - 所有基线使用相同预处理流程和决策窗口；  
  - 多次重复（文中未明确重复次数，但报告了标准差）；  
  - 消融实验设计完整，验证了尖峰驱动、CPLIF、互补融合模块的必要性；  
  - 跨数据集、跨设置评估，覆盖受试者内/间泛化。总体充分且客观。

---

### 6. 论文的主要结论与发现

1. **性能领先**：S²M-Former在18个条件中11个取得最佳准确率，尤其在Cross-trial下表现突出（DTU 2s: 76.74%, AV-GC 2s: 70.64%），且仅用0.06M参数。  
2. **效率优势**：相比DBPNet参数减少14.7×（0.06M vs 0.88M），理论能耗降低5.8×；相比ANN版（SM-Former）FLOPs减少53.9%；SOPs与单分支SNN相当。  
3. **互补学习有效**：移除SGCM+MPTM导致精度下降，验证了跨分支互补融合的必要性；CPLIF优于标准LIF。  
4. **尖峰驱动有益**：S²M-Former优于其ANN对应体（SM-Former），说明尖峰稀疏性提升了表征能力和泛化性。  
5. **鲁棒泛化**：在Cross-subject（LOSO）设置下，KUL和DTU均取得最高准确率，表明跨受试者泛化能力强。

---

### 7. 优点：方法或实验设计上的亮点

- **生物学合理性**：采用LIF/CPLIF尖峰神经元模拟生物神经动力学，稀疏发放降低能耗。  
- **对称双分支设计**：空间与频率分支结构镜像，通过SGCM+MPTM模块实现可学习的互补融合，而非简单拼接。  
- **轻量化**：用1D令牌替代3D卷积，参数仅0.06M；所有模块共享固定参数，不随窗口长度变化（对比M-DBPNet需调整尺寸）。  
- **能效分析完整**：不仅报告参数和FLOPs，还基于45nm硬件计算理论能耗（MAC vs AC），并分析发放率。  
- **实验全面**：涵盖三种评估范式、三个数据集、多种窗口、消融/对比/泛化实验，可视化丰富。

---

### 8. 不足与局限

- **时间动态受损**：CSP和DE特征提取预处理破坏了原始EEG的时序动态，无法充分建模时间依赖性。作者承认这是未来工作方向。  
- **边缘性能不稳定**：Cross-trial下某些受试者准确率低于机会水平（50%），标准偏差较大（尤其KUL和AV-GC），反映零样本泛化挑战。  
- **硬件部署未验证**：当前仅报告理论能耗，未在神经形态芯片上实际部署验证，需算法-硬件协同设计研究。  
- **消融实验的统计显著性未报告**：未提供置信区间或显著性检验。  
- **对AV-GC数据集**：条件4（不一致移动目标噪声）作为测试域，模型在0.1s短窗口下精度有限（74.42%），长区间优势更明显。

---

（完）
