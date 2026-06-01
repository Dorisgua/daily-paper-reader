---
title: A Generalist Intracortical Motor Decoder
title_zh: 通用皮层内运动解码器
authors: "Joel Ye, Fabio Rizzoglio, Xuan Ma, Adam Smoulder, Hongwei Mao, Gary H Blumenthal, William Hockeimer, Nicolas Guazzelli Kunigk, Dalton D. Moore, Patrick J. Marino, Raeed H. Chowdhury, J. Patrick Mayo, Aaron Batista, Steven Chase, Michael L Boninger, Charles M. Greenspon, Andrew B. Schwartz, Nicholas G. Hatsopoulos, Lee E. Miller, Kristofer Bouchard, Jennifer L Collinger, Leila Wehbe, Robert Gaunt"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=utXSSdD9mt"
tags: ["query:eeg"]
score: 4.0
evidence: 神经解码与运动脑机接口
tldr: 本文构建了一个通用皮层内运动解码器，在2000小时的神经集群锋电位数据上预训练自回归Transformer。该模型在8个下游运动解码任务上均提升了性能，并能泛化到多种神经分布偏移。尽管数据模态为皮层内记录，其方法和结论对脑机接口领域的通用解码架构具有重要启示。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-utxssdd9mt/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1385, \"height\": 589, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-utxssdd9mt/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1454, \"height\": 649, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-utxssdd9mt/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1447, \"height\": 917, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-utxssdd9mt/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1441, \"height\": 678, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-utxssdd9mt/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1448, \"height\": 571, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-utxssdd9mt/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1453, \"height\": 385, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-utxssdd9mt/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 580, \"height\": 592, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-utxssdd9mt/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1448, \"height\": 682, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-utxssdd9mt/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1450, \"height\": 468, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-utxssdd9mt/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1022, \"height\": 1014, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-utxssdd9mt/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1442, \"height\": 1541, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-utxssdd9mt/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1442, \"height\": 479, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-utxssdd9mt/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 994, \"height\": 573, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-utxssdd9mt/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1452, \"height\": 573, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-utxssdd9mt/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 657, \"height\": 617, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-utxssdd9mt/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1427, \"height\": 596, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-utxssdd9mt/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1445, \"height\": 366, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-utxssdd9mt/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1312, \"height\": 684, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-utxssdd9mt/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1435, \"height\": 506, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-utxssdd9mt/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1286, \"height\": 259, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-utxssdd9mt/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 924, \"height\": 338, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-utxssdd9mt/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1433, \"height\": 2113, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-utxssdd9mt/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1134, \"height\": 219, \"label\": \"Table\"}]"
motivation: 现有运动解码器通常限制问题复杂度，未能利用大规模数据提升泛化能力。
method: 在2000小时神经锋电位数据上预训练自回归Transformer，结合多种运动协变量。
result: 在8个下游运动解码任务上表现优异，可泛化至多种神经分布偏移。
conclusion: 大规模预训练是提升神经解码泛化能力的有效途径。
---

## Abstract
Mapping the relationship between neural activity and motor behavior is a central aim of sensorimotor neuroscience and neurotechnology. While most progress to this end has relied on restricting complexity, the advent of foundation models instead proposes integrating a breadth of data as an alternate avenue for broadly advancing downstream modeling. We quantify this premise for motor decoding from intracortical microelectrode data, pretraining an autoregressive Transformer on 2000 hours of neural population spiking activity paired with diverse motor covariates from over 30 monkeys and humans. The resulting model is broadly useful, benefiting decoding on 8 downstream decoding tasks and generalizing to a variety of neural distribution shifts. However, we also highlight that scaling autoregressive Transformers seems unlikely to resolve limitations stemming from sensor variability and output stereotypy in neural datasets.

---

## 论文详细总结（自动生成）

# 论文详细中文总结

## 1. 核心问题与整体含义（研究动机和背景）

- **核心问题**：运动解码（从皮层内微电极记录的神经群体锋电位活动解码运动行为）通常依赖于限制问题复杂度的策略（如单被试、单任务）。本文探索基础模型范式——通过整合大量多样化的神经-行为配对数据来进行预训练，是否能够在广泛的下游解码任务上带来普遍性提升。
- **背景**：脑机接口（BCI）领域数据快速增长，但跨数据集存在巨大异质性（电极差异、神经元群体差异、行为差异）。预训练可能利用共享结构提升样本效率，但传感器差异和行为刻板性可能构成根本限制。此前有NDT2等模型展示了跨session/跨subject的迁移学习，但规模较小。本文旨在量化大规模预训练的实际益处和局限。

## 2. 方法论

- **核心思想**：训练一个自回归Transformer（NDT3），在大量“神经锋电位序列 + 行为时间序列”配对数据上进行下一个token预测，然后在下游任务上微调所有参数以进行连续运动解码。
- **关键技术细节**：
  - **数据tokenization**：
    - 神经数据：每20ms窗口内的锋电位计数，按32个通道“patch”成一个token（例如96通道→3个神经token/时间步）。
    - 行为数据：每个行为维度（如速度、肌电、力）直接作为一个token（低维）。
    - 额外token：阶段标记（BCI控制 vs. 程序控制）和回报标记（基于未来任务完成度），仅预训练使用，推理时擦除。
  - **模型架构**：线性读入层（将输入映射到嵌入）→因果Transformer（RoPE位置编码，闪速注意力2）→线性读出层（预测下一时间步的所有token）。
  - **训练目标**：行为变量均方误差（MSE）+ 神经锋电位计数交叉熵损失 + 回报交叉熵损失。
  - **预训练与微调**：
    - 预训练：数据不标注间断，截成2秒片段，丢弃无活动或行为不变的片段。总约3百万片段，1750小时（作者近似为2000小时）。
    - 微调：保持所有预训练目标，更新所有参数，使用较小学习率。
    - 行为协变量在训练中对部分时间步进行mask（“协变量dropout”），防止模型仅依赖自回归行为输入而忽略神经输入。
- **推理**：输入仅包含神经token和行为维度的零mask，模型自回归生成行为预测（因果顺序保证控制实时性）。

## 3. 实验设计

- **使用的数据集 / 场景**：
  - 预训练数据：>30只猴子和人类，2000小时，来自多个实验室的皮层内微电极阵列数据。包括：运动学（肢体速度）、肌电（EMG）、力信号、BCI闭环控制数据等。
  - 下游评估：8个独立数据集（4个人类+4个猴子），覆盖不同上肢运动任务（2D光标控制、抓握力、自行触达、临界稳定任务、双手光标控制等）。所有下游猴子和部分人类数据在预训练中严格保留（除2khr模型有少量重叠但证明无优势）。
  - 额外泛化测试：不同脑区（S1、FEF/MT）、时间偏移、姿势偏移、弹簧负载偏移、实验结构（断续 vs. 连续）等。
- **基准方法**：
  - Wiener Filter（WF）：传统线性解码器，使用多时间步历史与岭回归。
  - NDT2：基于Transformer的MAE预训练模型，当前FALCON基准领先者。比较从头训练和使用公开预训练权重（100h人类数据）的版本。
- **评估方式**：
  - 多数据库微调：每个下游数据集合并多个session的微调数据（联合训练），避免逐个session训练。对每个任务在多种下游数据量比例（25%、50%、100%）上评估。
  - 指标：行为预测R²（方差加权平均），每个设置运行3个随机种子，网格搜索3个学习率。
  - 统计检验：FDR校正的配对t检验比较模型间差异。

## 4. 资源与算力

- **预训练计算**：
  - 45M参数模型（200小时数据）：约480 A100-GPU小时。
  - 350M参数模型（2000小时数据）：约20,000 A100-GPU小时。
- **硬件**：NVIDIA A100 (40GB) GPU，使用数据并行训练。
- **推理延迟**：在NVIDIA 4090上，45M模型平均4ms，350M模型平均9ms，满足20ms实时要求。
- 部分计算资源来自NERSC（Perlmutter集群）和匹兹堡大学H2P集群。

## 5. 实验数量与充分性

- **主要实验数量**：
  - 8个下游解码任务 × 3-4种下游数据比例 × 多种预训练配置（不同数据规模/模型大小）= 约31个评估设置。
  - 每个设置3个随机种子，共约2000个微调模型。
  - 泛化分析：输入敏感性（通道打乱、半token偏移、token打乱）、角度外推（3 hold-in vs 5 hold-out）、多种真实分布偏移（时间、姿势、负载）、不同脑区。
  - 消融实验：协变量dropout、BCI conditioning tokens、神经重建目标、MSE vs 分类、patch大小等。
- **充分性与客观性**：
  - 使用统计显著性检验，而非仅平均值比较。
  - 所有模型（深度网络）使用相同的超参数搜索空间，避免对NDT3过度调整。
  - Wiener Filter超参数也经交叉验证。
  - 但局限性：超参数搜索范围有限（仅3个学习率），可能未充分优化NDT2（其性能低于预期）。未与更多近期模型（如POYO、NDT-MTM）全面比较（文中解释了原因）。实验覆盖了多种类型但缺乏严格控制的多subject多task数据集来精确区分数据集质量的影响。

## 6. 主要结论与发现

- **大规模预训练的收益**：
  - 在多达31个下游设置上，联合增大数据规模和模型大小能带来总体性能提升。350M/2khr模型显著优于其他配置（除350M/200hr模型外）。
  - 收益主要集中在下游数据量 < 1.5小时的场景；超过此阈值，线性和深度模型差异消失，预训练增益饱和。
- **输入顺序敏感性限制跨subject迁移**：
  - 预训练模型在跨session数据上表现良好，但在跨subject数据上无额外收益（超出预训练已提供的基线），说明预训练已经吸收了所有可迁移的跨subject结构。
  - 通道打乱或半token偏移（保持邻接但破坏token内通道结构）极大地削弱了跨session迁移，表明NDT3对输入维度顺序的依赖。
- **无法泛化到未见过的角度（输出刻板性）**：
  - 在中心-外任务中，即使预训练模型也无法预测从未见过的角度，其输出被限制在训练角度之间（吸引子行为），而经过PCA-LDA的线性解码器能成功外推。
  - 这表明模型学到了行为刻板性，而非潜在的神经活动低维结构。
- **真实分布偏移下的泛化**：
  - 在时间、姿势、负载等自然偏移下，预训练带来的收益在分布内和分布外保持正相关。
  - 预训练降低了对实验trial结构的依赖（连续训练下试次化调优的模型退化更温和）。
  - 在运动皮层外（S1、眼动区）也显示了非平凡增益，表明模型学到一定的通用神经先验。

## 7. 优点

- **规模空前**：预训练数据量（2000小时）和模型大小（350M参数）远超此前皮层内锋电位研究（通常<200h, <10M），是向基础模型迈进的重要尝试。
- **通用架构**：仅依靠自回归Transformer和简单线性读入/读出层，无需任务特定组件（如不同解码头），便于扩展到新任务。
- **广泛评估**：在8个不同任务、多种下游数据量、多种分布偏移下系统评估，并提供统计显著性检验，结论较为可靠。
- **开放透明**：代码和预训练权重公开发布，支持复现和后续研究。
- **明确局限性分析**：主动指出输入顺序敏感性和输出刻板性，为未来基础模型设置了具体基准挑战。

## 8. 不足与局限

- **收益饱和过早**：1.5小时下游数据后预训练无明显增益，限制了其在实际BCI部署中的优势（因为临床用户往往可以收集更多数据）。作者认为这可能源于数据异质性的根本限制。
- **存在严重泛化失败**：对输入通道顺序敏感（打乱后迁移失效），不能泛化到未训练的角度（输出吸引子），这两点对于稳健的BCI控制至关重要。
- **实验设计的局限**：
  - 未与POYO、NDT-MTM等最新Transformer解码器进行详细对比（仅简单复现POYO表现不佳），且NDT2基线性能可能因有限超参数搜索低于其最佳水平。
  - 缺乏对多种神经特征（如局部场电位、bandpower）和元特征（每日嵌入）的探索。
  - 下游数据集主体是受限的实验范式（试次化、短时重复动作），自然行为数据不足。
  - 部分人类评估数据集包含在2khr预训练中（但作者证明未带来优势），但仍存在泄露风险。
- **计算成本高**：350M模型需要20K A100-hours，限制了多数实验室的复现能力。
- **过拟合实验结构**：模型仍然倾向于利用试次边界等实验伪影，尽管预训练缓解了这一问题，但未完全解决。
- **隐私与安全**：预训练模型可能隐含训练数据信息，脑机接口数据敏感，需注意隐私保护。

（完）
