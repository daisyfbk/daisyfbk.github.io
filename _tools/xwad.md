---
tool: X-WAD
people:
  - RobertoDoriguzziCorin
  - MatteoBitussi
peopleOrder: surname
---

X-WAD (eXplainable Web Anomaly Detection) is a tool used to detect and explain security anomalies in web traffic using Transformer-based language models. Rather than functioning as a black-box model that only outputs an anomaly score, X-WAD provides fine-grained explainability by generating heatmap visualizations over request segments flagged as anomalous. This is achieved through token-level, logit-based surprisal mapping applied to a model trained in a semi-supervised manner on benign data. Two different types of models are supported: autoregressive models (using Causal Language Modeling) and predictive models (using Masked Language Modeling).

X-WAD enabled the discovery of sample mislabeling within a frequently used anomaly detection benchmark dataset. Such unseen contamination can introduce backdoor-like failures into trained models, potentially causing them to silently misclassify specific exploit vectors as normal requests.

X-WAD has been published as part of the following research paper:

`Matteo Bitussi and Doriguzzi-Corin, Roberto. "X-WAD: eXplainable Web Anomaly Detection" accepted at iAIMS 2026 (International Conference on Artificial Intelligence Models and Systems)`

You may find the preprint of the paper in the [arXiv repository](https://arxiv.org/abs/2608.27172).

X-WAD is available on [GitHub](https://github.com/mattebit/x-wad).
