<div align="center">

# hERG Pharmacophore Modeling using MOE

### A MOE-based computational drug-discovery workflow for pharmacophore modeling, virtual screening, and hERG liability interpretation

<br>

![MOE](https://img.shields.io/badge/Tool-MOE-blue?style=for-the-badge)
![Cheminformatics](https://img.shields.io/badge/Domain-Cheminformatics-green?style=for-the-badge)
![Drug Discovery](https://img.shields.io/badge/Focus-Drug%20Discovery-orange?style=for-the-badge)
![Pharmacophore](https://img.shields.io/badge/Method-Pharmacophore%20Modeling-purple?style=for-the-badge)
![License](https://img.shields.io/badge/License-CC0-lightgrey?style=for-the-badge)

<br>

<a href="#project-overview">Project Overview</a> • <a href="#workflow-summary">Workflow</a> • <a href="#key-results">Key Results</a> • <a href="#repository-structure">Repository</a> • <a href="#author">Author</a>

</div>

---

## Project Overview

This repository presents a structured **MOE-based pharmacophore modeling workflow** for evaluating potential **hERG inhibitor liability** using small-molecule conformer databases, pharmacophore feature selection, virtual screening, and model-performance interpretation.

The project is designed as a clean **computational drug-discovery portfolio example**, showing how pharmacophore models can be constructed, screened, inspected, and evaluated inside **Molecular Operating Environment (MOE)**.

---

## Why This Project Matters

The **hERG potassium channel** is an important safety-related target in drug discovery because unintended hERG inhibition can be associated with cardiotoxicity risk. Early computational screening can help identify compounds with possible hERG-related activity patterns before expensive downstream experimental testing.

This project demonstrates a practical cheminformatics workflow for:

* Building a pharmacophore model in MOE
* Screening conformer databases
* Inspecting pharmacophore-matched hits
* Summarizing model performance using confusion-matrix metrics
* Organizing MOE outputs into a reproducible portfolio-style repository

---

## Workflow Summary

```mermaid
flowchart LR
    A[Small Molecule Dataset] --> B[Conformer Database Preparation]
    B --> C[Pharmacophore Feature Selection]
    C --> D[MOE Pharmacophore Model]
    D --> E[Virtual Screening]
    E --> F[Hit Inspection]
    F --> G[Model Evaluation]
```

---

## Main Tasks

The workflow includes the following major steps:

| Step                          | Description                                                          |
| ----------------------------- | -------------------------------------------------------------------- |
| Dataset preparation           | Small molecules were prepared for conformer generation and screening |
| Conformer database generation | MOE conformer databases were generated for pharmacophore searching   |
| Feature selection             | Pharmacophore features were selected and inspected                   |
| Pharmacophore modeling        | A final hERG-focused pharmacophore model was constructed             |
| Virtual screening             | Compounds were screened against the selected model                   |
| Hit inspection                | Matched hits were visually inspected inside MOE                      |
| Model evaluation              | Confusion-matrix-based performance metrics were summarized           |

---

## Visual Results

### Selected Pharmacophore Model Features

> Add your main pharmacophore model image here.

```markdown
![Pharmacophore Model Features](results/figures/pharmacophore_model_features.png)
```

![Pharmacophore Model Features](results/figures/pharmacophore_model_features.png)

---

### Packed Conformation Hits

```markdown
![Packed Conformation Hits](results/figures/packed_conformation_hits.jpg)
```

![Packed Conformation Hits](results/figures/packed_conformation_hits.jpg)

---

### Screening Hits

```markdown
![Screening Hits](results/figures/screening_hits.jpg)
```

![Screening Hits](results/figures/screening_hits.jpg)

---

## Selected Pharmacophore Features

The selected pharmacophore model contains three key features:

| Feature | Type                   | Radius |
| ------- | ---------------------- | -----: |
| F1      | Donor/Acceptor feature |    1.1 |
| F2      | Hydrophobic feature    |    1.3 |
| F3      | Acceptor feature       |    1.0 |

These features represent the spatial and chemical interaction pattern used by the model to identify compounds with potential hERG-related activity.

---

## Key Results

The recorded model evaluation summary contains the following confusion-matrix values:

| Metric Component | Count |
| ---------------- | ----: |
| True Positives   |     6 |
| True Negatives   |     6 |
| False Positives  |     0 |
| False Negatives  |     3 |

### Accuracy Calculation

```text
Accuracy = (TP + TN) / (TP + TN + FP + FN)

Accuracy = (6 + 6) / (6 + 6 + 0 + 3)

Accuracy = 12 / 15

Accuracy = 80%
```

### Model Summary

| Metric                           | Value |
| -------------------------------- | ----: |
| Total evaluated compounds        |    15 |
| Correctly classified compounds   |    12 |
| Incorrectly classified compounds |     3 |
| Accuracy                         |   80% |

---

## Key Outputs

| Output                                             | Description                                              |
| -------------------------------------------------- | -------------------------------------------------------- |
| `models/hERG_pharmacophore_model.ph4`              | Final MOE pharmacophore model file                       |
| `models/pharmacophore_features.ph4que`             | Pharmacophore feature/query definition file              |
| `moe_databases/*.mdb`                              | MOE molecular and conformer database files               |
| `results/figures/pharmacophore_model_features.png` | Visual representation of selected pharmacophore features |
| `results/figures/packed_conformation_hits.jpg`     | Hit inspection from packed conformers                    |
| `results/figures/screening_hits.jpg`               | Screening output visualization                           |
| `results/tables/model_evaluation_summary.txt`      | Model evaluation summary                                 |

---

## Repository Structure

```text
.
├── models/
│   ├── hERG_pharmacophore_model.ph4
│   └── pharmacophore_features.ph4que
│
├── moe_databases/
│   ├── conf_log.mdb
│   ├── conf_out.mdb
│   ├── conf_unk.mdb
│   ├── dbname_conf.mdb
│   ├── dbnamescreen_conf.mdb
│   ├── mdr_pharmacophore.mdb
│   ├── packed.mdb
│   ├── ph4_out.mdb
│   ├── ph4_out2.mdb
│   └── screening.mdb
│
├── results/
│   ├── figures/
│   │   ├── pharmacophore_model_features.png
│   │   ├── packed_conformation_hits.jpg
│   │   └── screening_hits.jpg
│   └── tables/
│       └── model_evaluation_summary.txt
│
├── docs/
│   ├── methodology.md
│   ├── moe_workflow_notes.md
│   └── limitations.md
│
├── README.md
├── LICENSE
└── .gitignore
```

---

## Tools and Methods

| Category                    | Tools / Methods                                |
| --------------------------- | ---------------------------------------------- |
| Molecular modeling software | MOE, Molecular Operating Environment           |
| Core method                 | Pharmacophore modeling                         |
| Screening strategy          | Conformer database screening                   |
| Analysis type               | hERG liability interpretation                  |
| Output type                 | MOE models, MOE databases, figures, tables     |
| Repository purpose          | Computational drug-discovery portfolio project |

---

## How to Use This Repository

Some files in this repository are MOE-generated files and require **Molecular Operating Environment (MOE)** to open, inspect, or reproduce the workflow.

Recommended review order:

1. Open the `docs/` folder to understand the methodology and workflow notes.
2. Inspect the final pharmacophore model in `models/`.
3. Review MOE database outputs in `moe_databases/`.
4. Check visual outputs in `results/figures/`.
5. Review the model evaluation summary in `results/tables/`.

---

## Limitations

This project is intended as a computational workflow demonstration and portfolio example. The results should not be interpreted as experimental validation of hERG inhibition.

Important limitations include:

* The workflow depends on the quality and size of the input compound dataset.
* Pharmacophore screening provides pattern-based predictions, not direct biological confirmation.
* MOE-generated files require licensed MOE software for full inspection.
* Experimental validation would be required before drawing strong conclusions about hERG activity or cardiotoxicity risk.

---

## Future Improvements

Possible improvements for future versions include:

* Add a larger and more diverse compound dataset
* Compare multiple pharmacophore hypotheses
* Add ROC-AUC, sensitivity, specificity, precision, and F1-score
* Include external validation compounds
* Compare MOE pharmacophore screening with machine-learning-based hERG prediction
* Add animated workflow GIFs or short demo videos
* Add a downloadable PDF report for portfolio presentation

---

## Author

**Hazrat Maghaz**
Bioinformatician | Computational Biologist | AI Drug Discovery Enthusiast

| Platform | Link                                                 |
| -------- | ---------------------------------------------------- |
| Website  | https://hazratmaghaz.tech                            |
| GitHub   | https://github.com/HazratMaghaz                      |
| LinkedIn | https://www.linkedin.com/in/hazrat-maghaz-6967b9374/ |

---

## License

This repository is available under the license included in the `LICENSE` file.

---

<div align="center">

### If this repository helped you understand pharmacophore modeling, feel free to star the project.

![GitHub stars](https://img.shields.io/github/stars/HazratMaghaz/Pharmacophore-Modeling-hERG-Inhibitors-MOE?style=social)
![GitHub forks](https://img.shields.io/github/forks/HazratMaghaz/Pharmacophore-Modeling-hERG-Inhibitors-MOE?style=social)

</div>
