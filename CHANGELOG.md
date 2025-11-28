📘 CHANGELOG.md

Grey-Box Visualization Framework — Version History

[3.0.0] — 2025-11-XX
Major Release：Grey-Box Visualization Framework V3.0（Universal Edition）

This is the first complete, model-agnostic, 7-layer formalization of the Grey-Box framework.

✨ Added
1. Seventh Layer — Semantic Field（NEW）

Introduced the concept of a high-dimensional meaning landscape.

Field properties include:

semantic attractor basins

drift tendencies

regional stability / instability

potential gradients across meaning clusters

Provides a global, system-level view of how LLM meaning converges.

2. Cross-Layer Dynamics（NEW）

Defined feedback interactions between all layers:

nodes ↔ attention

attention ↔ flow

flow ↔ weight

weight ↔ field

field ↔ intervention

Establishes the first “multi-loop reasoning engine” description for LLMs.

3. Reasoning Pipeline Visualization

Token → embeddings → semantic nodes

Attention routing → flow → field

Field collapse → output distribution

Enables dynamic, step-by-step tracing of inference paths.

4. Universal LLM Compatibility

Framework generalized to apply to all Transformer LLMs:

GPT 系列

Gemini 系列

Claude

Llama

任何 Encoder-Decoder 與 Decoder-only 架構

Removes model-specific assumptions.

🔧 Changed
1. Six-Layer V2 Expanded to Seven-Layer V3

Added an entire new reasoning layer (Semantic Field).

Reinterpreted older layers to fit dynamic flow relations.

2. Terminology Standardization

Unified naming for nodes, flows, velocity fields, and intervention layers.

Clarified conceptual boundaries between saliency vs semantic flow.

3. Framework Reorganized for Clarity

Clear separation between:

local reasoning behaviors（Layers 1–5）

external control（Layer 6）

global semantic topology（Layer 7）

🧹 Removed

No features removed in this version.

V3 is an additive, backward-compatible expansion from V2.

📚 Notes

This Universal Edition contains only model-agnostic reasoning structures.

Framework extensions (e.g., persona, multi-agent, symbolic overlays) are not included here.

A “Specialized Edition” may be created for system-specific cognitive overlays（e.g., narrative models、multi-persona frameworks）.

[2.x.x] — Pre-V3 Internal Drafts
(Not formally published)

Implemented the original six-layer grey-box model：

Semantic Nodes

Attention Mapping

Semantic Flow

Weight Heatmap

Flow Velocity Field

Intervention Ring

Focused on the interpretability of Transformer attention and token-level reasoning.

Served as the conceptual foundation for V3.

[1.x.x] — Prototype Phase（Unpublished）

Personal research notes.

Experimental visualization concepts.

Not included in public documentation.

📌 Versioning Policy

Grey-Box Framework follows semantic versioning（SemVer）:

MAJOR.MINOR.PATCH


MAJOR：New layers, new reasoning structures

MINOR：New diagrams, new visualization tools

PATCH：Terminology clean-up / small corrections

📎 End of CHANGELOG

（This file will grow as additional releases are published.）
