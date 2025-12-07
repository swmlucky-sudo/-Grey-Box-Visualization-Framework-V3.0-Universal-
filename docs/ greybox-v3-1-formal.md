# Grey-Box V3.1 — Formal Edition  
### *Mathematical Interpretability Language for Transformer LLMs*

This document introduces the **formal symbolic system**, **metrics**, and **mathematical structures** used in Grey-Box analysis.

---

## 0. Symbolism Disclaimer

The formulas below are **not computational**.  
They serve as **formal structural markers** to describe semantic relationships, stability, and failure modes in LLMs.

---

## 1. Symbol Table

| Symbol | Meaning | Notes |
|--------|---------|-------|
| `T` | Token / Semantic Unit | Layer 1 |
| `h_t` | Hidden State Vector | Layer 3 |
| `D_s(T)` | Semantic Density | Layer 1 |
| `S_A` | Attention Sparsity | Layer 2 |
| `C_F(t)` | Flow Coherence | Layer 3 |
| `G_W` | Weight Sensitivity | Layer 4 |
| `V_L(h)` | Vector Variance | Layer 5 |
| `E_I` | Intervention Efficacy | Layer 6 |
| `Φ_S(x)` | Semantic Field Potential | Layer 7 |

---

## 2. Formal Layer Definitions

### **Layer 1 — Semantic Nodes**
D_s(T) = 1 / |Nε(T)|


### **Layer 2 — Attention Mapping**


S_A = 1 - H(A)


### **Layer 3 — Semantic Flow**


C_F(t) = cosine(h_t, h_(t+1))


### **Layer 4 — Weight Heatmap**


G_W = E[ || ∇_W L || ]


### **Layer 5 — Flow Velocity Field**


V_L(h) = Var(h_1 ... h_n)


### **Layer 6 — Intervention Ring**


E_I = || O' - O || / || I ||


### **Layer 7 — Semantic Field**


Φ_S(x) ∈ R


---

## 3. Formal Failure Modes

### **Attention Collapse**


S_A << 0.1 and C_F(t) ↓


### **Semantic Drift**


C_F(t) ↓ and ΔΦ_S(x) ≠ 0


### **Hallucination Attractor**


Φ_S(x) << 0 and H(P) ≈ 0


---

## 4. Inter-Layer Morphisms



N → A → F → W → V → ∇ → S


---

## Next:
👉 Proceed to **V3.1.1 Update** for interwoven dynamics and semantic mesh model.
