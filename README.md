# Toxicity at clinical trial stage

Separates drugs that reached FDA approval from those eliminated during clinical trials because of toxicity, using ClinTox, a MoleculeNet set of 1,478 compounds. The two outcomes are returned as independent probabilities rather than as a single verdict. A graph transformer pretrained on 10 million unlabelled molecules was fine-tuned on the pairing, with three fine-tuned folds averaged. The failed drugs are few and their failures span many mechanisms, so a high toxicity score signals resemblance to known failures rather than a specific liability.

This model was incorporated on 2022-07-13.Last packaged on 2026-05-20.

## Information
### Identifiers
- **Ersilia Identifier:** `eos6fza`
- **Slug:** `grover-clintox`

### Domain
- **Task:** `Annotation`
- **Subtask:** `Activity prediction`
- **Biomedical Area:** `ADMET`
- **Target Organism:** `Homo sapiens`
- **Tags:** `Toxicity`, `Chemical graph model`, `Side effects`

### Input
- **Input:** `Compound`
- **Input Dimension:** `1`

### Output
- **Output Dimension:** `2`
- **Output Consistency:** `Fixed`
- **Interpretation:** Probability of FDA approval and probability of clinical trial failure through toxicity.

Below are the **Output Columns** of the model:
| Name | Type | Direction | Description |
|------|------|-----------|-------------|
| fda_approved | float | high | Probability that the drug is FDA approved |
| ct_tox | float | high | Probability that the drug has clinical toxicity |


### Source and Deployment
- **Source:** `Local`
- **Source Type:** `External`
- **DockerHub**: [https://hub.docker.com/r/ersiliaos/eos6fza](https://hub.docker.com/r/ersiliaos/eos6fza)
- **Docker Architecture:** `AMD64`, `ARM64`
- **S3 Storage**: [https://ersilia-models-zipped.s3.eu-central-1.amazonaws.com/eos6fza.zip](https://ersilia-models-zipped.s3.eu-central-1.amazonaws.com/eos6fza.zip)

### Resource Consumption
- **Model Size (Mb):** `1310`
- **Environment Size (Mb):** `2547`
- **Image Size (Mb):** `6502.53`

**Computational Performance (seconds):**
- 10 inputs: `29.82`
- 100 inputs: `52.06`
- 10000 inputs: `-1`

### References
- **Source Code**: [https://github.com/tencent-ailab/grover](https://github.com/tencent-ailab/grover)
- **Publication**: [https://doi.org/10.48550/arXiv.2007.02835](https://doi.org/10.48550/arXiv.2007.02835)
- **Publication Type:** `Preprint`
- **Publication Year:** `2020`
- **Ersilia Contributor:** [Amna-28](https://github.com/Amna-28)

### License
This package is licensed under a [GPL-3.0](https://github.com/ersilia-os/ersilia/blob/master/LICENSE) license. The model contained within this package is licensed under a [MIT](LICENSE) license.

**Notice**: Ersilia grants access to models _as is_, directly from the original authors, please refer to the original code repository and/or publication if you use the model in your research.


## Use
To use this model locally, you need to have the [Ersilia CLI](https://github.com/ersilia-os/ersilia) installed.
The model can be **fetched** using the following command:
```bash
# fetch model from the Ersilia Model Hub
ersilia fetch eos6fza
```
Then, you can **serve**, **run** and **close** the model as follows:
```bash
# serve the model
ersilia serve eos6fza
# generate an example file
ersilia example -n 3 -f my_input.csv
# run the model
ersilia run -i my_input.csv -o my_output.csv
# close the model
ersilia close
```

## About Ersilia
The [Ersilia Open Source Initiative](https://ersilia.io) is a tech non-profit organization fueling sustainable research in the Global South.
Please [cite](https://github.com/ersilia-os/ersilia/blob/master/CITATION.cff) the Ersilia Model Hub if you've found this model to be useful. Always [let us know](https://github.com/ersilia-os/ersilia/issues) if you experience any issues while trying to run it.
If you want to contribute to our mission, consider [donating](https://www.ersilia.io/donate) to Ersilia!
