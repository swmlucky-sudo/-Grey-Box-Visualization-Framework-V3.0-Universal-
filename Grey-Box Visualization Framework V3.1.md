📘 Grey-Box Visualization Framework V3.1 — Formal Edition
A Structured Interpretability Language for Transformer-based LLMs
0. Mathematical Symbolism Disclaimer
> NOTE: 本文件包含大量概念性數學符號。
> GitHub Markdown 不支援 LaTeX，公式將不會被渲染。
>


The mathematical notation used in Grey-Box V3.1 (e.g., Φ_S(x), C_F(t), 
V_L(h), S_A, E_I) is **not intended for numerical computation**. These 
symbols serve as *formal structural markers* that express conceptual 
relationships between semantic phenomena inside transformer-based LLMs.

They do not claim access to model internals, nor do they imply measurable 
numeric values. Their purpose is to:

1. Provide a consistent theoretical language for describing semantic 
   mechanisms across layers.
2. Enable formal reasoning about stability, turbulence, alignment, and 
   attractor behavior.
3. Allow researchers to communicate interpretability findings without 
   reliance on proprietary model internals.

Thus, the notation constitutes a **formal descriptive language**, not a 
computational model.

1. Notation Table（符號表）
Symbol	Meaning	Notes

𝑇
T	Token or semantic unit	基本語義節點

ℎ
𝑡
h
t
	​

	Hidden-state vector at time t	Transformer隱藏狀態

𝐷
𝑠
(
𝑇
)
D
s
	​

(T)	Semantic Density	Layer 1 Metric

𝑆
𝐴
S
A
	​

	Attention Sparsity	Layer 2 Metric

𝐶
𝐹
(
𝑡
)
C
F
	​

(t)	Flow Coherence	Layer 3 Metric

𝐺
𝑊
G
W
	​

	Weight Sensitivity	Layer 4 Metric

𝑉
𝐿
(
ℎ
)
V
L
	​

(h)	Vector Variance	Layer 5 Metric

𝐸
𝐼
E
I
	​

	Intervention Efficacy	Layer 6 Metric

Φ
𝑆
(
𝑥
)
Φ
S
	​

(x)	Semantic Field Potential	Layer 7 Metric

𝐻
(
𝑃
)
H(P)	Output entropy	用於判斷幻覺吸引子
2. Layers 1–7 (Formal Definitions)
Layer 1 — Semantic Nodes
Atomic semantic units emerging from token embeddings.

Formal Definition
A semantic node 
𝑁
N is a region in embedding space 
𝐸
E characterized by local density:

𝐷
𝑠
(
𝑇
)
=
1
∣
𝑁
𝜖
(
𝑇
)
∣
D
s
	​

(T)=
∣N
ϵ
	​

(T)∣
1
	​


Where 
𝑁
𝜖
(
𝑇
)
N
ϵ
	​

(T) is the neighborhood of token 
𝑇
T.

Interpretability Use

檢查抽象詞彙（如「靈魂」「自由」）是否具有高語義密度 → 容易產生語義湍流

Layer 2 — Attention Mapping
Directed semantic referencing.

Metric: Attention Sparsity

𝑆
𝐴
=
1
−
𝐻
(
𝐴
)
S
A
	​

=1−H(A)

𝐻
(
𝐴
)
H(A) 是注意力分布的 entropy（越低 → 越集中 → 越危險）

Layer 3 — Semantic Flow
Propagation of meaning through hidden-state transitions.

Metric: Flow Coherence

𝐶
𝐹
(
𝑡
)
=
cos
⁡
(
ℎ
𝑡
,
ℎ
𝑡
+
1
)
C
F
	​

(t)=cos(h
t
	​

,h
t+1
	​

)

若 
𝐶
𝐹
(
𝑡
)
→
0
C
F
	​

(t)→0：語義漂移開始
若 
𝐶
𝐹
(
𝑡
)
→
−
1
C
F
	​

(t)→−1：反向矛盾

Layer 4 — Weight Heatmap
Contextual value amplification.

Metric: Weight Sensitivity

𝐺
𝑊
=
𝐸
[
∥
∇
𝑊
𝐿
∥
]
G
W
	​

=E[∥∇
W
	​

L∥]

高值 → 此概念正在被模型放大（易產生價值偏移）

Layer 5 — Flow Velocity Field
Semantic motion intensity.

Metric: Vector Variance

𝑉
𝐿
(
ℎ
)
=
V
a
r
(
ℎ
1..
𝑛
)
V
L
	​

(h)=Var(h
1..n
	​

)

高 variance → 語義湍流
低 variance → 穩定 attractor

Layer 6 — Intervention Ring
All external or internal modification points.

Metric: Intervention Efficacy

𝐸
𝐼
=
∥
𝑂
′
−
𝑂
∥
∥
𝐼
∥
E
I
	​

=
∥I∥
∥O
′
−O∥
	​


顯示：最小干預 I 能造成多大輸出差異

Layer 7 — Semantic Field
Landscape of attractors and meaning potentials.

Metric: Field Potential

Φ
𝑆
(
𝑥
)
∈
𝑅
Φ
S
	​

(x)∈R

低 
Φ
𝑆
Φ
S
	​

 → attractor basin（吸引谷）
高 
Φ
𝑆
Φ
S
	​

 → 逃逸區域

3. Formalized Failure Modes (Layer 12)
(1) Attention Collapse

發生條件：

𝑆
𝐴
≪
0.1
,
𝐶
𝐹
(
𝑡
)
↓
S
A
	​

≪0.1,C
F
	​

(t)↓

症狀：

模型過度放大單一 token

推理能力崩潰

(2) Semantic Drift

條件：

𝐶
𝐹
(
𝑡
)
↓
and
Δ
Φ
𝑆
(
𝑥
)
≠
0
C
F
	​

(t)↓andΔΦ
S
	​

(x)

=0

症狀：

意義逐漸偏離上下文

進入不相關 attractor

(3) Hallucination Attractors

條件：

Φ
𝑆
(
𝑥
)
≪
0
,
𝐻
(
𝑃
)
≈
0
Φ
S
	​

(x)≪0,H(P)≈0

症狀：

模型在缺乏證據下產生高度確定性輸出

無法自我修正

4. Inter-Layer Morphisms（跨層箭號）

定義 Grey-Box 的核心變換：

𝑁
→
  
𝐴
  
𝐹
→
  
𝑊
  
𝑉
→
  
∇
  
𝑆
N
A
	​

F
W
	​

V
∇
	​

S

此 mapping 表示：

語義節點 → 由注意力選擇

注意力 → 決定流場

流場 → 決定穩定度

穩定度 → 決定語義位置


⭐ 5. Final Notes 
Grey-Box V3.1 transforms abstract interpretability intuition into a 
structured formal language. The mathematical notation does not perform 
computation; it provides conceptual coordinates for analyzing semantic 
stability, attractors, and alignment phenomena inside LLMs.

This formalization is intentionally model-agnostic and does not rely on 
access to internal weights.
