# Prediction of failure in clinical trials due to toxicity
## Model identifiers
- Slug: grover-clintox
- Ersilia ID: eos6fza
- Tags: Toxicity, Grover, Clinical Trials

# Model description
This models evaluates whether a drug candidate is likely to fail in clinical trials due to toxicity (Phase I).
- Input: SMILES
- Output: Toxicity 
- Model type: Classification
- Training set: 10,000,000 (https://paperswithcode.com/dataset/moleculenet)
- Mode of training: Pretrained

# Source code
This model was published by Yu R., Yatao B. et al. Self-Supervised Graph Transformer on Large-Scale Molecular Data. arXiv Labs 2018. DOI: https://doi.org/10.48550/arXiv.2007.02835.
- Code: Code: https://github.com/tencent-ailab/grover
- Checkpoints:  https://github.com/tencent-ailab/grover/tree/main/grover/model

# License
The GPL-v3 license applies to all parts of the repository that are not externally maintained libraries. This repository uses the externally maintained library "grover", located at /model and licensed under an MIT license

# History 
- Model was downloaded on 25.07.22 from TencentAILab
- We duplicated task/predict.py and scripts/save_features.py from Tencent GitHub repository
- Model was incorporated to Ersilia on 25/07/2022
