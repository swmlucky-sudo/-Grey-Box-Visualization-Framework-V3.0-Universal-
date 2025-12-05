📘 Grey-Box Visualization Framework V3.1 — Formal Edition (Unified Version)
A Structured Interpretability Language for Transformer-based LLMs
2025 Updated Edition with Section 8 Integration
0. Mathematical Symbolism Disclaimer

The mathematical notation used in Grey-Box V3.1 (e.g.,
Φ_S(x), C_F(t), V_L(h), S_A, E_I) is not intended for numerical computation.
These symbols serve as formal structural markers that describe conceptual relationships among semantic phenomena inside Transformer-based language models.

They do not imply:

access to internal weights,

numerical measurability,

or executable mathematical operations.

Their purpose is to:

Provide a consistent theoretical language for describing semantic structures.

Enable formal reasoning about stability, turbulence, alignment, and attractor behavior.

Communicate interpretability findings without reliance on proprietary internals.

Thus, the notation constitutes a formal descriptive language, not a computational model.

1. Notation Table（符號表）
Symbol	Meaning	Notes
T	Token / semantic unit	基本語義節點
hₜ	Hidden-state vector at time t	Transformer 隱藏狀態
D_s(T)	Semantic Density	Layer 1 Metric
S_A	Attention Sparsity	Layer 2 Metric
C_F(t)	Flow Coherence	Layer 3 Metric
G_W	Weight Sensitivity	Layer 4 Metric
V_L(h)	Vector Variance	Layer 5 Metric
E_I	Intervention Efficacy	Layer 6 Metric
Φ_S(x)	Semantic Field Potential	Layer 7 Metric
H(P)	Output entropy	幻覺吸引子判定用
2. Layers 1–7 (Formal Definitions)
Layer 1 — Semantic Nodes

Atomic semantic units emerging from token embeddings.

Formal Definition
A semantic node N is a region in embedding space E with local density:

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


Interpretability Use:

High D_s(T) in words like 「靈魂」「自由」 means high turbulence risk.

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

Low entropy → highly concentrated attention → collapse risk

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

C_F → 0 → semantic drift

C_F → –1 → contradiction

Layer 4 — Weight Heatmap

Amplification of contextual importance.

Metric: Weight Sensitivity

𝐺
𝑊
=
𝐸
[
∣
∣
∇
𝑊
𝐿
∣
∣
]
G
W
	​

=E[∣∣∇
W
	​

L∣∣]

High G_W → concept being amplified → value distortion risk

Layer 5 — Flow Velocity Field

Semantic motion intensity.

Metric: Vector Variance

𝑉
𝐿
(
ℎ
)
=
𝑉
𝑎
𝑟
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

High → turbulence

Low → stable attractor basin

Layer 6 — Intervention Ring

All internal or external modification points.

Metric: Intervention Efficacy

𝐸
𝐼
=
∣
∣
𝑂
′
−
𝑂
∣
∣
∣
∣
𝐼
∣
∣
E
I
	​

=
∣∣I∣∣
∣∣O
′
−O∣∣
	​


Shows how strongly a minimal intervention I affects output O.

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

Low Φ_S → attractor basin

High Φ_S → escape region

3. Formalized Failure Modes (Layer 12)
(1) Attention Collapse

Conditions

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

Symptoms

Over-amplification of one token

Logical breakdown

(2) Semantic Drift

Conditions

𝐶
𝐹
(
𝑡
)
↓
,
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

(t)↓,ΔΦ
S
	​

(x)

=0

Symptoms

Answer gradually diverges from topic

Moves toward unintended attractor

(3) Hallucination Attractors

Conditions

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

Symptoms

Unwarranted high-certainty output

Self-correction failure

4. Inter-Layer Morphisms（跨層態射）

Grey-Box’s conceptual mapping:

𝑁
→
𝐴
→
𝐹
→
𝑊
→
𝑉
→
∇
→
𝑆
N→A→F→W→V→∇→S

Interpretation：

Semantic nodes → attention determines relevance

Attention → shapes semantic flow

Flow → determines stability

Stability → determines semantic positioning in Φ_S

This structure is didactic, not temporal.

5. Final Notes

Grey-Box V3.1 turns interpretability intuition into a structured formal language.
Mathematical expressions define relationships, not numerical computations.
The design remains model-agnostic and architecture-compatible.

6. Appendix — Example Phrase-Level Interpretation

(可留空，供未來加入)

7. Appendix — Glossary of Semantic Structures

(可留空，供未來加入)

8. Linear Morphisms vs. Interwoven Layer Interactions
新增於 2025 版 V3.1（重要過渡章節）

While V3.1 presents the morphism chain

𝑁
→
𝐴
→
𝐹
→
𝑊
→
𝑉
→
∇
→
𝑆
N→A→F→W→V→∇→S

to clarify structural dependency, this chain should not be interpreted as a strict temporal order.

8.1 Linear Morphism View（線性態射觀點）

Useful for：

Teaching the conceptual build-up of meaning

Explaining how semantic layers depend on each other

Interpreting one static moment of reasoning

It answers：

「在此刻，語義是如何被構成並穩定的？」

8.2 Interwoven Interaction View（交錯層互動觀點）

This view reflects actual Transformer behavior：

(1) Intra-layer Parallelism

Within a single timestep, Layer 1–5 behaviors occur in parallel, not sequentially.

(2) Cross-Layer Dynamics

Higher-level turbulence (Layer 5) can inform diagnostic insight about
attention stability (Layer 2).
This is analysis feedback, not architectural feedback.

(3) Semantic Field as a Dynamic Landscape

Layer 7 is not a final output but an ongoing potential field shaping the path τ of reasoning.

8.3 Why This Matters

V3.1 uses a static structural view

V3.2 will introduce dynamic trajectories τ(t) and semantic events

This section bridges the conceptual transition

8.4 Summary

Grey-Box is not a pipeline. It is a semantic mesh.
V3.1 views the mesh statically;
V3.2 views the mesh in motion.
