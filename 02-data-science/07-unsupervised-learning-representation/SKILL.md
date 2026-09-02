---
name: unsupervised-learning-representation
description: Reduce, segment, or detect anomalies without treating clusters as discovered truth — PCA, embeddings, clustering, and outlier detection. Use whenever the user asks for customer segments, PCA, clustering, embeddings, or anomaly detection without a label. Apply even if they want "natural groups in the data."
compatibility: Standard ML stacks.
metadata:
  author: Promptstation
  version: 1.0.0
  category: data-science
  course: 02-data-science
  section: 07-unsupervised-learning-representation
---

# Unsupervised Learning and Representation

## Mission

Unsupervised methods invent structure. Your job is to say whether that structure is useful for a named purpose, not whether it is "real." Clusters are tools. They are not tribes found in nature.

## When this skill governs

Use for segmentation, dimensionality reduction, embeddings, and unsupervised anomaly detection.

## Core output

Deliver a **Structure Note**:

1. Purpose (compress, segment, detect, embed)
2. Features and scaling
3. Method and hyperparameters
4. Stability checks (seeds, subsets, k)
5. Interpretation in original variables
6. How the output will be used
7. What not to claim

## Phase 1 — Purpose first

- **Compress:** PCA / factor-style reduction for downstream models or visualisation
- **Segment:** clusters as operational groups (treat differently)
- **Detect:** unusual points for review, not automatic guilt
- **Embed:** distances for retrieval or as features

If the purpose is "find insights," go back to EDA. Unsupervised learning is a poor substitute for a histogram and a question.

## Phase 2 — Clustering

k-means: spherical, similar scale, you pick k.  
Hierarchical: small n, dendrograms.  
Density (DBSCAN): irregular shapes, noise points.  
Mixture models: probabilistic assignment.

Rules:

- scale features that are not already comparable
- do not dump 200 collinear dummies in and pray
- k is a decision, not a truth; silhouette is a hint, not a verdict
- stability: rerun with different seeds and subsamples; unstable clusters are not a product
- always describe clusters in original units ("high recency, low monetary"), not "Cluster 3"

If a simple rule (e.g. RFM cutpoints) matches the clusters, prefer the rule.

## Phase 3 — Reduction and embeddings

PCA: linear, ordered components, good for continuous correlated features. Interpret loadings. Do not treat PC1 as a latent moral index.

Nonlinear embeddings (t-SNE, UMAP): visualisation only unless you have a retrieval task. Distances and densities are distorted. Never cluster on a t-SNE plot and call it analysis.

## Phase 4 — Anomaly detection

Unsupervised anomalies are points unlike the bulk. They may be fraud, errors, or legitimate tails.

Always send anomalies to a review rule. Score = priority for humans, not a conviction.

## Phase 5 — Research workflow

1. Name the use of the structure.
2. Choose features that are licit for that use (no leakage of future outcomes if segments will be used as treatments).
3. Fit; check stability.
4. Label in original variables.
5. Validate against the purpose (do segments differ on a held-out behaviour that was not used to cluster?).
6. Refuse ontological claims.

## Anti-patterns

- "The data revealed five customer types"
- Clustering raw mixed-scale data
- k chosen by a weak elbow and never questioned
- t-SNE as evidence
- Anomaly score as automatic sanction
- Using the target to cluster, then celebrating separation

## Decision heuristic

1. What will we do with this structure?
2. Would a simple rule suffice?
3. Are clusters stable?
4. Can I name them in original variables?
5. What claim am I not allowed to make?

## Validation gate

- Purpose named
- Scaling addressed
- Stability checked
- Clusters described in original units
- No "natural types" language
- Anomalies routed to review if they affect people

## Final principle

Unsupervised learning proposes a grouping. You owe a purpose, a stability check, and a description in the original variables — or you owe the reader nothing.
