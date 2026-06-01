---
title: Identifying Neural Dynamics Using Interventional State Space Models
title_zh: 使用干预状态空间模型识别神经动力学
authors: "Amin Nejatbakhsh, Yixin Wang"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=n7qKt6gjl9"
tags: ["query:eeg-latent"]
score: 5.0
evidence: 用于潜在神经动力学的干预状态空间模型
tldr: 该论文提出干预状态空间模型(iSSM)，能够预测神经回路在未知扰动下的响应，通过低维潜变量动力学实现因果解释。尽管实验基于神经记录，其潜空间建模框架可直接用于EEG信号中的潜特征提取和因果分析，为EEG潜空间表示提供新方法。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-n7qkt6gjl9/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1571, \"height\": 687, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-n7qkt6gjl9/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1753, \"height\": 672, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-n7qkt6gjl9/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 844, \"height\": 704, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-n7qkt6gjl9/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1573, \"height\": 779, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-n7qkt6gjl9/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1568, \"height\": 752, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-n7qkt6gjl9/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1757, \"height\": 667, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-n7qkt6gjl9/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1663, \"height\": 242, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-n7qkt6gjl9/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1843, \"height\": 388, \"label\": \"Table\"}]"
motivation: 传统状态空间模型仅捕捉统计关联，无法进行因果预测。
method: 结合因果动态系统理论，在状态空间模型中引入干预变量，学习因果潜动力学。
result: 在合成和实际神经数据上成功预测了干预下的神经响应。
conclusion: 干预状态空间模型为神经潜动力学提供了因果建模工具，可推广至EEG分析。
---

## Abstract
Neural circuits produce signals that are complex and nonlinear. To facilitate the understanding of neural dynamics, a popular approach is to fit state space models (SSM) to the data and analyze the dynamics of the low-dimensional latent variables. Despite the power of SSM to explain the dynamics of neural circuits, these models have been shown to merely capture statistical associations in the data and cannot be causally interpreted. Therefore, an important research problem is to build models that can predict neural dynamics under causal manipulations. Here, we propose interventional state-space models (iSSM), a class of causal models that can predict neural responses to novel perturbations. We draw on recent advances in causal dynamical systems and present theoretical results for the identifiability of iSSM. In simulations of the motor cortex, we show that iSSM can recover the true latents and the underlying dynamics. In addition, we illustrate two applications of iSSM in biological datasets. First, we applied iSSM to a dataset of calcium recordings from ALM neurons in mice during photostimulation. Second, we applied iSSM to a dataset of electrophysiological recordings from macaque dlPFC during micro-stimulation. In both cases, we show that iSSM outperforms SSM and results in identifiable parameters. The code is available at https://github.com/amin-nejat/issm.

---

## 论文详细总结（自动生成）

# 论文总结：使用干预状态空间模型识别神经动力学

## 1. 核心问题与整体含义

- **研究动机**：神经回路产生复杂非线性信号，传统状态空间模型（SSM）虽能捕捉低维潜变量动力学，但仅反映统计关联，无法进行因果解释。在神经科学中，理解因果机制需要预测干预（如光遗传、电刺激）下的神经响应，而现有模型缺乏这一能力。
- **整体含义**：提出干预状态空间模型（iSSM），通过将干预显式建模为潜变量动力学的结构方程，实现对干预数据的因果建模。iSSM能够从观测和干预数据中识别潜变量、动力学矩阵和混合函数，从而泛化到未见干预，为神经科学中的因果假设检验提供新工具。

## 2. 方法论

- **核心思想**：基于因果推断框架，将干预建模为改变结构方程。假设干预直接作用于潜变量，并切断被干预潜变量与其父节点的连接。在动力学方程中，当干预非零时，被干预潜变量的更新仅依赖于干预项和噪声，忽略来自其他潜变量的动力学影响。
- **关键技术细节**：
  - **模型定义**：
    - 潜变量动力学：`x_{t+1} = 1{Bu_t = 0} ⊗ A x_t + B u_t + ϵ_t`，其中`1{Bu_t = 0}`为逐元素指示向量，`A`为动力学矩阵，`B`为干预效应矩阵（施加稀疏Laplace先验），`ϵ_t`为高斯噪声。
    - 观测模型：`y_t ~ P(y_t | f_θ(x_t))`，`f_θ`为非线性混合函数（如ReLU网络）。
  - ****识别性理论**：
    - 假设观测模型满足有界完备性（bounded completeness）、混合函数为分段线性连续单射、动力学满足忠实性（无干预时无额外独立关系），则iSSM可被块识别（block identifiable）——通过单个干预可将被干预潜变量与未被干预潜变量分离，且可泛化到只作用于已分离潜变量的新干预。
    - 在足够多样干预（满足无序对条件）下，可实现全局识别（可逆对角缩放+置换）。
  - **推理方法**：采用变分推断，使用LSTM作为识别网络，并在变分均值处直接应用干预结构（`μ_t`替换为`1{Bu_t=0} ⊗ μ_t + B u_t`），使干预信息一致地传递到后验近似。

## 3. 实验设计

- **数据集/场景**：
  1. **合成数据**：两种运动皮层模型——旋转动力学（RD）和动态吸引子（DA），生成低维潜变量+非线性观测；以及高维投影版本（通过随机正交矩阵C投影到更高维）。
  2. **小鼠数据集**：前外侧运动皮层（ALM）钙成像，含179个神经元、77次试验，8个光刺激通道，记录短时记忆任务中延迟期光刺激的神经活动。
  3. **猕猴数据集**：dlPFC电生理记录（96通道电极阵列），6个数据集（3个仅观测，3个含微刺激干预），每个干预会话刺激两个电极。
- **Benchmark**：与标准SSM（观测模型，不含干预结构）对比。
- **比较方法**：SSM vs iSSM，比较两种模型在观测和干预下的重构精度、潜变量识别能力、B矩阵的一致性（不同随机初始化下的稳定性）。
- **评估指标**：重构相关系数（观测和潜变量）、一致性得分（B矩阵跨初始化的欧氏距离）。

## 4. 资源与算力

- 论文未明确说明使用的GPU型号、数量或训练时长。
- 仅提及使用Adam优化器，学习率0.001~0.01，迭代1000次，LSTM隐藏单元数10，未报告具体硬件配置。

## 5. 实验数量与充分性

- **实验组数**：包含合成数据（2种模型，多个维度设置）、小鼠数据（超参数搜索后比较）、猕猴数据（6个数据集，不同潜伏维度）。消融实验：比较不同潜伏维度、B稀疏度的影响；SSM vs iSSM的多次随机初始化（3~10次）以评估一致性。
- **充分性**：合成数据上验证了识别性（潜变量和动力学矩阵恢复），真实数据上展示了重构精度提升和参数一致性提高。实验覆盖了不同物种（小鼠、猕猴）和记录类型（钙成像、电生理）。但缺乏与更多基线方法（如LDS、非线性ICA、其他因果表示学习方法）的对比；未在更大规模数据或更多干预类型上测试泛化能力。

## 6. 主要结论与发现

- iSSM能够从干预数据中识别潜变量和底层动力学（合成数据中潜变量相关系数接近1，动力学矩阵恢复良好），而标准SSM无法做到。
- 在真实数据上，iSSM的重构精度（训练和测试）优于SSM，且B矩阵在不同初始化下更一致（一致性得分更低），表明参数识别性更好。
- iSSM学习到的潜变量轨迹能区分行为正确/错误试次（小鼠数据），并在刺激期间显示明显的状态偏移（猕猴数据），具有生物意义。
- iSSM可泛化到未见干预（理论保证+合成数据验证）。

## 7. 优点

- **理论贡献**：提供了干预下状态空间模型识别性的充分条件，将因果表示学习扩展到动态系统，特别针对潜变量受干预直接影响的场景。
- **方法创新**：将干预显式融入变分推断的均值更新中，确保了干预图结构在后验中的一致性。
- **实验验证**：在合成和两个真实世界神经数据集上验证了方法有效性，覆盖不同物种和记录模态。
- **实用性**：模型能够预测新干预下的观测分布，对神经科学中的因果假设检验和闭环刺激设计有潜在价值。

## 8. 不足与局限

- **动力学线性假设**：当前模型假设潜动力学为线性，虽然理论上线性+非线性发射可近似任意动力学，但真实神经动力学可能包含强非线性，缺乏非线性动力学的明确建模和识别理论。
- **干预与潜变量对齐**：假设干预直接影响潜变量，但实际中干预作用于神经元，需通过B矩阵映射到潜变量。这种对齐需要先验或额外推断，可能不成立。
- **推理近似**：采用变分推断，可能引入近似误差；LSTM作为识别网络可能不是最优，且计算开销随序列长度增加。
- **实验覆盖**：缺乏与更多现有方法（如PI-VAE、iVAE、其他动态因果模型）的系统比较；仅在少数数据集上测试，未在大量不同任务或脑区验证泛化性。
- **可扩展性**：未讨论高维潜变量或大规模神经群体时的计算和识别挑战；稀疏B假设可能要求足够的干预覆盖才能实现完整识别。

（完）
