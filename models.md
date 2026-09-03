# MEG Foundation Models

> The current landscape of MEG foundation models and MEG-inclusive multi-modal foundation models.

Part of **[meg-fm-resources](README.md)**, the companion resource for *A Roadmap for MEG Foundation Models*. See also the **[dataset list](datasets.md)**.

This list distinguishes **direct MEG** models, **clinical MEG** models, **multi-modal MEG-inclusive** foundation models, and **precursors** — earlier work that established the paradigm without being a foundation model in the full sense. For each entry you get the modalities, pretraining data scale, architecture, self-supervised objective, tokenization scheme, downstream evaluation, and the contribution that distinguishes it.

**7 models · 4 categories**

## At a glance

| Model | Type | Modalities | Pretraining data | Architecture |
| :-- | :-- | :-- | :-- | :-- |
| [MEG-GPT](#meg-gpt) | [Direct MEG FM](#direct-meg-foundation-models) | MEG (resting-state) | Cam-CAN (~612 subjects) | GPT-style Transformer |
| [Headache-MEG-FM](#headache-meg-fm) | [Clinical MEG FM](#clinical-meg-foundation-models) | MEG (multi-state) | ~416 participants (clinical + controls) | Deep neural network |
| [BrainOmni](#brainomni) | [Multi-modal FM](#multi-modal-meg-inclusive-foundation-models) | EEG + MEG | ~1,997 h EEG + 656 h MEG | Transformer-based |
| [Brain-OF](#brain-of) | [Multi-modal FM](#multi-modal-meg-inclusive-foundation-models) | fMRI + EEG + MEG | ~40 datasets (multi-source) | Unified multi-modal architecture |
| [Ferrante et al.](#ferrante-et-al) | [Hybrid FM](#multi-modal-meg-inclusive-foundation-models) | EEG + MEG + fMRI | Multiple datasets (vision tasks) | Representation alignment framework |
| [GPT2MEG](#gpt2meg) | [Precursor](#precursors) | MEG | Large MEG dataset (multi-subject) | GPT-2-style autoregressive model |
| [Jayalath et al.](#jayalath-et-al) | [Precursor](#precursors) | MEG | Cam-CAN (641 subjects, ~160 h) + MOUS (204) | Conv cortex encoder + LSTM |

## The models

Full records for all 7 models, grouped by type.

### Direct MEG foundation models

Models pretrained natively on MEG, targeting general-purpose representations rather than one task.

#### MEG-GPT

Citation key: `huang_meg-gpt_2026`

- **Model type:** Direct MEG FM
- **Modalities:** MEG (resting-state)
- **Data scale / datasets:** Cam-CAN (~612 subjects)
- **Architecture:** GPT-style Transformer
- **Pretraining objective:** Self-supervised autoregressive prediction
- **Tokenization / representation:** Region-level time-series tokenization
- **Downstream evaluation:** Cross-subject generalization, decoding
- **Key contribution:** First explicit general-purpose MEG foundation model

### Clinical MEG foundation models

Models pretrained on MEG with a clinical population and diagnostic endpoint in view.

#### Headache-MEG-FM

Citation key: `liao_pretrained_2026`

- **Model type:** Clinical MEG FM
- **Modalities:** MEG (multi-state)
- **Data scale / datasets:** ~416 participants (clinical + controls)
- **Architecture:** Deep neural network (details less standardized vs. GPT-style)
- **Pretraining objective:** Self-supervised + supervised fine-tuning
- **Tokenization / representation:** Signal-level / feature embeddings
- **Downstream evaluation:** Migraine/headache classification
- **Key contribution:** First clinically oriented MEG foundation model

### Multi-modal MEG-inclusive foundation models

Models that treat MEG as one modality among several, learning a shared representation across EEG, fMRI, or both.

#### BrainOmni

Citation key: `xiao_brainomni_2025`

- **Model type:** Multi-modal FM
- **Modalities:** EEG + MEG
- **Data scale / datasets:** ~1,997 h EEG + 656 h MEG
- **Architecture:** Transformer-based
- **Pretraining objective:** Self-supervised cross-modal learning
- **Tokenization / representation:** Shared latent space across modalities
- **Downstream evaluation:** Cross-dataset generalization, decoding
- **Key contribution:** First joint EEG–MEG foundation model

#### Brain-OF

Citation key: `guo_brain-_2026`

- **Model type:** Multi-modal FM
- **Modalities:** fMRI + EEG + MEG
- **Data scale / datasets:** ~40 datasets (multi-source)
- **Architecture:** Unified multi-modal architecture (transformer-like)
- **Pretraining objective:** Self-supervised multi-modal pretraining
- **Tokenization / representation:** Cross-modal latent representations
- **Downstream evaluation:** Encoding, decoding, modality conversion
- **Key contribution:** First tri-modal omnifunctional brain FM

#### Ferrante et al.

Citation key: `ferrante_towards_2026`

- **Model type:** Hybrid FM (alignment-focused)
- **Modalities:** EEG + MEG + fMRI
- **Data scale / datasets:** Multiple datasets (vision tasks)
- **Architecture:** Representation alignment framework
- **Pretraining objective:** Cross-modal alignment / shared embeddings
- **Tokenization / representation:** Latent representation learning
- **Downstream evaluation:** Decoding, encoding, modality translation
- **Key contribution:** Early foundation-model-style alignment approach

### Precursors

Earlier work that established the modelling paradigm without being a foundation model in the full sense.

#### GPT2MEG

Citation key: `csaky_gpt2meg_2026`

- **Model type:** Precursor
- **Modalities:** MEG
- **Data scale / datasets:** Large MEG dataset (multi-subject)
- **Architecture:** GPT-2-style autoregressive model
- **Pretraining objective:** Self-supervised autoregressive
- **Tokenization / representation:** Quantized MEG tokens
- **Downstream evaluation:** Generation, decoding
- **Key contribution:** Key precursor to the MEG-GPT paradigm

#### Jayalath et al.

Citation key: `jayalath_brains_2025`

- **Model type:** SSL pretext-task method for MEG speech decoding (precursor; not a transformer FM)
- **Modalities:** MEG
- **Data scale / datasets:** Cam-CAN (641 subjects, ~160 h); + MOUS (204 subjects) in aggregation test
- **Architecture:** Convolutional cortex encoder (SEANet-style) + LSTM; dataset-conditional layer, FiLM subject conditioning; frozen backbone + linear probe
- **Pretraining objective:** Self-supervised pretext prediction: band, phase-shift, amplitude-scale
- **Tokenization / representation:** Continuous multi-sensor windows (0.5 s) conv-encoded to embeddings; sensor-count-agnostic
- **Downstream evaluation:** Speech detection + voicing classification on Armeni (3 subj.) and Gwilliams MEG-MASC (27 subj.); cross-subject, cross-dataset, novel-subject generalization
- **Key contribution:** Neuroscience-inspired SSL tasks enabling first novel-subject and cross-dataset generalization in MEG speech decoding, with scaling-law evidence
