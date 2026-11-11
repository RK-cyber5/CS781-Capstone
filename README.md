# CS781 Capstone Competition — IIT Kanpur

## Student information

- **Name:** Mutaka Rohith Kumar
- **Roll Number:** 240671
- **Institute:** IIT Kanpur
- **Email:** rohithk24@iitk.ac.in

## Overview

This repository contains the implementation artifacts and final report for the CS781 Capstone Competition. The supplied materials are organized by competition phase; notebooks are preserved as submitted source artifacts.

## Repository structure

- `code/` contains the phase-specific notebooks and status documentation.
- `code/phase1/` through `code/phase7/` contain the materials for their respective phases.
- `report/` contains the final capstone report.

## Phase-wise implementation

| Phase | Status | Implementation |
| --- | --- | --- |
| Phase 1 | Submitted | Architecture-A legal-language-model pipeline with official-data audit, leakage-safe holdout, resumable training, checkpoint selection, and submission generation. |
| Phase 2 | Not submitted | No verified competition implementation is included; see `code/phase2/STATUS.md`. |
| Phase 3 | Not submitted | No verified competition implementation is included; see `code/phase3/STATUS.md`. |
| Phase 4 | Submitted | CJPE workflow based on the Phase-1 Architecture-A checkpoint, with full-epoch data training, development evaluation, adapter tuning, and resumable checkpoints. The supplied documentation records three completed submissions against a six-submission target. |
| Phase 5 | Submitted | Legal Statute Identification multi-label workflow using Phase-1 model checkpoints, including adapters, LoRMA, partial/layer-wise fine-tuning, BitFit, full fine-tuning, and knowledge-distillation experiment support. |
| Phase 6 | Submitted | Architecture-C / E7 rank-16 LoRA decoding workflow that selects among deterministic repetition-controlled decoding configurations without retraining. |
| Phase 7 | Submitted | Architecture-A long-run legal retrieval experiment using full fine-tuning, learned retrieval projection, hard negatives, and resumable training. |

## Installation and execution

The project is distributed as notebooks rather than a standalone Python package. Open the relevant notebook in a competition-compatible Kaggle environment and run cells in order.

- Each phase may require its official dataset and the exact tokenizer and checkpoint named in its notebook.
- Phases 1, 4, 5, 6, and 7 require GPU resources for their documented workflows.
- Phase 4 requires the Phase-1 Architecture-A checkpoint and matching `LEGAL_40K` tokenizer.
- Phase 5 requires compatible Phase-1 checkpoints and the exact `LEGAL_40K` tokenizer; missing or incompatible architectures are reported rather than treated as complete.
- Phase 6 requires the Phase-1 Architecture-C / DMLC-150 checkpoint, exact `LEGAL_40K` tokenizer, and the E7 rank-16 LoRA adapter. It also documents enabling Kaggle Internet to load the official Phase-6 dataset.
- Phase 7 requires the documented Phase-1 Architecture-A checkpoint and official Phase-7 data. Its multi-session restart procedure is documented in the notebook.

The supplied notebooks do not guarantee availability of datasets, checkpoints, external services, or sufficient compute. See [`code/README.md`](code/README.md) and each notebook for phase-specific setup, paths, and restart instructions.

## Report

[CS781 capstone report](report/CS781-CP-Rohith-Kumar-240671-report.pdf)

## Reproducibility

Where the required official data, checkpoints, environment configuration, and compute resources are available, reproduce a phase by opening its notebook, attaching the required inputs, and executing it in order. The notebooks document their expected artifacts, checkpoint handling, and submission packaging. Phase 2 and Phase 3 intentionally remain documented as having no verified competition implementation.
