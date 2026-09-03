# MEG Datasets for Foundation-Model Development

> A curated list of magnetoencephalography (MEG) datasets for building and evaluating foundation models.

Companion dataset catalogue for the perspective paper **A Roadmap for MEG Foundation Models**. The list covers large-cohort, multimodal, naturalistic, clinical, and task-oriented MEG datasets that may support foundation-model **pretraining**, **transfer**, or **downstream evaluation**. For every dataset you get the hosting source, access conditions, cohort size, modalities, data volume, paradigm, its distinguishing strength, and the foundation-model use case it fits best.

## A Roadmap for MEG Foundation Models

Philipp Thölke<sup>1,2</sup>, Hamza Abdelhedi<sup>1,2,3</sup>, Yorguin Mantilla-Ramos<sup>1,2,3</sup>, Fouad Lbakali<sup>1,2,4</sup>, Oumayma Gharbi<sup>3,5</sup>, Catherine Duclos<sup>6,7,8</sup>, Annalisa Pascarella<sup>9</sup>, Vanessa Hadid<sup>2,10</sup>, Oiwi Parker Jones<sup>11,12</sup>, Karim Jerbi<sup>1,2,3,13</sup>

<details>
<summary><b>Affiliations</b></summary>

1. Cognitive and Computational Neuroscience Laboratory (CoCo Lab), Université de Montréal, Montréal, QC, Canada
2. Department of Psychology, Université de Montréal, Montréal, QC, Canada
3. Mila – Quebec Artificial Intelligence Institute, Montréal, QC, Canada
4. IMT Atlantique, Brest, F-29238, France
5. IVADO, Université de Montréal, Montréal, QC, Canada
6. Center for Advanced Research in Sleep Medicine, Hôpital du Sacré-Cœur de Montréal, Santé Québec Nord-de-l’Île-de-Montréal – Universitaire, Montréal, QC, Canada
7. Department of Anesthesiology and Pain Medicine, Faculty of Medicine, Université de Montréal, Montréal, QC, Canada
8. Department of Neuroscience, Faculty of Medicine, Université de Montréal, Montréal, QC, Canada
9. Institute for Applied Mathematics “Mauro Picone”, National Research Council (CNR), Rome, Italy
10. McGill University Health Centre, Montréal, QC, Canada
11. Oxford Centre for Integrative Neuroimaging (OxCIN), University of Oxford, Oxford, United Kingdom
12. Department of Engineering Science, University of Oxford, Oxford, United Kingdom
13. UNIQUE Center, Quebec Neuro-AI Research Center, Montréal, QC, Canada

</details>

### Abstract

Foundation models are beginning to reshape brain-signal analysis by moving the field beyond task-specific decoding pipelines toward reusable models pretrained on broad neural datasets. Magnetoencephalography (MEG) is a compelling but still underdeveloped target for this shift: it captures human cortical dynamics at millisecond resolution while offering stronger spatial interpretability than EEG, making it especially valuable for source-resolved studies of perception, language, cognition, and clinical brain function. Yet MEG foundation models remain at an early stage, with only a small number of MEG-specific and MEG-inclusive multi-modal models, modest pretraining corpora, and emerging but still limited benchmarks. This perspective lays down the basic concepts needed to understand MEG foundation models and provides a didactic overview of the field’s key design choices, including tokenization, sensor- versus source-space representations, sensor-geometry encoding, backbone architectures, self-supervised objectives, and pretraining data. We then offer a roadmap for future development, organized around native MEG pretraining, adaptation of EEG foundation models, transfer from generic time-series models, and multi-modal integration with EEG, fMRI, MRI, behaviour, and stimulus features. We highlight the need for coordinated infrastructure, including diverse and reusable MEG datasets, rigorous evaluation across subjects, sites, tasks, and clinical settings, and responsible data-sharing practices that address consent, privacy, access, and governance.

**Keywords:** magnetoencephalography (MEG) · foundation models · self-supervised learning · brain decoding · human electrophysiology · neural representation learning · multi-modal neuroimaging

### Citation

> The paper is not yet published. The full citation and a BibTeX entry will be added here once it is out.

## At a glance

**25 datasets · ≈3,200 participants · 13 openly available**

| Dataset | Family | N | Access | Modalities | Scale / size |
| :-- | :-- | --: | :-- | :-- | :-- |
| [CamCAN](#camcan) | [Large cohort](#large-cohort) | 647 | 📝 Registration | MEG, processed sMRI | Large lifespan dataset |
| [OMEGA](#omega) | [Large cohort](#large-cohort) | 644 | 📝 Registration | MEG, T1 MRI | 150+ hours |
| [MEG UK](#meg-uk) | [Large cohort](#large-cohort) | 500 | 🔒 Restricted | MEG, MRI, psychometric data | Multi-site; >500 healthy individuals |
| [NatMEG](#natmeg) | [Large cohort](#large-cohort) | 130 | 📝 Registration | MEG | Medium |
| [NIMH Healthy Research Volunteers](#nimh-healthy-research-volunteer-dataset) | [Large cohort](#large-cohort) | 123 | ✅ Open | MEG, MRI | 663 GB |
| [MOUS](#mous) | [Multimodal](#multimodal) | 204 | 🔒 Restricted | MEG, fMRI | 1030 GB |
| [WAND](#wand) | [Multimodal](#multimodal) | 170 | ✅ Open | MEG, MRI, TMS | Medium |
| [HCP MEG](#hcp-meg) | [Multimodal](#multimodal) | 95 | 📝 Registration | MEG, MRI | Moderate; 300 GB |
| [Naturalistic music listening](#naturalistic-music-listening) | [Multimodal](#multimodal) | 35 | ✅ Open | MEG | 333 GB |
| [Wakeman and Henson](#wakeman-and-henson) | [Multimodal](#multimodal) | 19 | ✅ Open | sMRI, fMRI, MEG, EEG | Small–medium; 29 GB |
| [Simon task MEEG](#simon-task-meeg) | [Multimodal](#multimodal) | 9 | ✅ Open | MEG, EEG | 38 GB |
| [Sentence-level meaning](#sentence-level-meaning) | [Naturalistic](#naturalistic) | 35 | ✅ Open | MEG, MRI | 343 GB |
| [LibriBrain100](#libribrain100) | [Naturalistic](#naturalistic) | 33 | ✅ Open | MEG, audio, text | ~100 hours |
| [DECAF](#decaf) | [Naturalistic](#naturalistic) | 30 | ✉️ Request | MEG, NIR face video, hEOG, ECG, tEMG | 60 hours; 300 GB |
| [MEG-MASC](#meg-masc) | [Naturalistic](#naturalistic) | 27 | ✅ Open | MEG + audio/text | Small–medium |
| [10-hour within-participant narrative](#10-hour-within-participant-narrative) | [Naturalistic](#naturalistic) | 3 | 🔒 Restricted | MEG | 230 GB |
| [LibriBrain](#libribrain) | [Naturalistic](#naturalistic) | 1 | ✅ Open | MEG | 50 hours; 87 GB |
| [Oscillatory building blocks](#oscillatory-building-blocks) | [Task benchmark](#task-benchmark) | 33 | 🔒 Restricted | MEG | 452 GB |
| [BCI and mental imagery](#bci-and-mental-imagery) | [Task benchmark](#task-benchmark) | 17 | ✅ Open | MEG | Small; 49 GB |
| [Eye movement effects in MEG](#eye-movement-effects-in-meg) | [Task benchmark](#task-benchmark) | 16 | 🔒 Restricted | MEG | 127 GB |
| [THINGS-MEG](#things-meg) | [Task benchmark](#task-benchmark) | 4 | ✅ Open | MEG, T1 MRI | 377 GB |
| [BioFIND](#biofind) | [Clinical / perturb.](#clinical-and-perturbation) | 324 | 📝 Registration | MEG, T1 MRI, metadata | Medium–large |
| [Pharmacological MEG](#pharmacological-meg) | [Clinical / perturb.](#clinical-and-perturbation) | 68 | ✅ Open | MEG | Medium |
| [Auditory-to-motor entrainment in Parkinson's](#auditory-to-motor-entrainment-in-parkinsons-disease) | [Clinical / perturb.](#clinical-and-perturbation) | 30 | 🔒 Restricted | MEG | 174 GB |
| [Left motor cortex and phonological discrimination](#left-motor-cortex-and-phonological-discrimination) | [Specialized](#specialized) | 32 | ✅ Open | MEG | Not specified |

## The datasets

Full records for all 25 datasets, grouped by family and ordered by cohort size.

### Large cohort

Broad, standardized recordings across many participants — the backbone for native MEG pretraining and normative modeling.

#### CamCAN

**Cambridge Centre for Ageing and Neuroscience** — [opendata.mrc-cbu.cam.ac.uk](https://opendata.mrc-cbu.cam.ac.uk/projects/camcan/)

- **Participants:** 647
- **Source:** MRC CBU · **Access:** 📝 Registration needed
- **Modalities:** MEG, processed sMRI
- **Scale / size:** Large lifespan dataset
- **Task / paradigm:** Rest, sensorimotor and passive tasks
- **Key strength:** Lifespan variability (18–88 yrs)
- **Best FM use case:** Native pretraining; normative representations; cross-subject transfer. Core dataset for MEG-GPT.

#### OMEGA

**Open MEG Archives** — [mcgill.ca/bic/neuroinformatics/omega](https://www.mcgill.ca/bic/neuroinformatics/omega)

- **Participants:** 644
- **Source:** McGill BIC · **Access:** 📝 Registration needed
- **Modalities:** MEG, T1 MRI
- **Scale / size:** 150+ hours
- **Task / paradigm:** Resting state
- **Key strength:** Large, standardized, growing repository
- **Best FM use case:** Native pretraining; normative representations; cross-subject transfer. Used in scaling MEG token models.

#### MEG UK

[meguk.ac.uk](https://meguk.ac.uk/)

- **Participants:** 500
- **Source:** UK MEG Partnership / Cardiff · **Access:** 🔒 Restricted (consortium access)
- **Modalities:** MEG, MRI, psychometric data
- **Scale / size:** Multi-site; more than 500 healthy individuals
- **Task / paradigm:** Rest; sensory-motor and cognitive tasks
- **Key strength:** Cross-site recordings from multiple MEG systems
- **Best FM use case:** Native pretraining; normative representations; cross-subject transfer.

#### NatMEG

**NatMEG (Parkinson's dataset), Swedish National Facility** — [search.kg.ebrains.eu](https://search.kg.ebrains.eu/instances/d55146e8-fc86-44dd-95db-7191fdca7f30)

- **Participants:** 130
- **Source:** EBRAINS · **Access:** 📝 Registration needed
- **Modalities:** MEG
- **Scale / size:** Medium
- **Task / paradigm:** Resting + tasks
- **Key strength:** Neurodegenerative trajectories
- **Best FM use case:** Native pretraining; normative representations; cross-subject transfer. Useful for longitudinal FM extensions.

#### NIMH Healthy Research Volunteer Dataset

[openneuro.org/datasets/ds005752](https://openneuro.org/datasets/ds005752/versions/2.1.0)

- **Participants:** 123
- **Source:** OpenNeuro · **Access:** ✅ Open
- **Modalities:** MEG, MRI
- **Scale / size:** 663 GB
- **Task / paradigm:** Rest; Hariri Hammer; Sternberg; somatosensory; Go/No-Go; naturalistic viewing; oddball
- **Key strength:** Deep clinical, psychometric, cognitive, MRI, and MEG phenotyping
- **Best FM use case:** Native pretraining; normative representations; cross-subject transfer.

### Multimodal

MEG recorded alongside fMRI, EEG, structural MRI, or brain stimulation — for cross-modal alignment and method validation.

#### MOUS

**Mother of Unification Studies** — [data.ru.nl](https://data.ru.nl/collections/di/dccn/DSC_3011020.09_236)

- **Participants:** 204
- **Source:** Radboud Universiteit · **Access:** 🔒 Restricted
- **Modalities:** MEG, fMRI
- **Scale / size:** 1030 GB
- **Task / paradigm:** Rest, language task
- **Key strength:** Strong cross-modal training resource
- **Best FM use case:** Multimodal alignment; EEG/MEG/fMRI transfer; validation benchmark. Used for generalization in MEG token models.

#### WAND

**Welsh Advanced Neuroimaging Database** — [git.cardiff.ac.uk/cubric/wand](https://git.cardiff.ac.uk/cubric/wand)

- **Participants:** 170
- **Source:** CUBRIC, Cardiff University · **Access:** ✅ Open
- **Modalities:** MEG, MRI, TMS
- **Scale / size:** Medium
- **Task / paradigm:** Mixed tasks
- **Key strength:** Multimodal + intervention
- **Best FM use case:** Multimodal alignment; EEG/MEG/fMRI transfer; validation benchmark. Useful for causal modeling.

#### HCP MEG

**Human Connectome Project MEG** — [humanconnectome.org](https://humanconnectome.org/study/hcp-young-adult/data-releases)

- **Participants:** 95
- **Source:** ConnectomeDB · **Access:** 📝 Registration needed
- **Modalities:** MEG, MRI
- **Scale / size:** Moderate; 300 GB
- **Task / paradigm:** Rest, multiple tasks
- **Key strength:** High-quality multimodal integration
- **Best FM use case:** Multimodal alignment; EEG/MEG/fMRI transfer; validation benchmark. Gold-standard multimodal alignment.

#### Naturalistic music listening

**Tracking predictions in naturalistic music listening using MEG and computational models of music** — [data.ru.nl](https://data.ru.nl/collections/di/dccn/DSC_3018045.02_116)

- **Participants:** 35
- **Source:** Radboud Universiteit · **Access:** ✅ Open
- **Modalities:** MEG
- **Scale / size:** 333 GB
- **Task / paradigm:** Naturalistic Western classical music listening
- **Key strength:** Note-level melodic surprise and uncertainty from computational music models
- **Best FM use case:** Multimodal alignment; EEG/MEG/fMRI transfer; validation benchmark.

#### Wakeman and Henson

**Wakeman & Henson dataset** — [openneuro.org/datasets/ds000117](https://openneuro.org/datasets/ds000117/versions/1.1.0)

- **Participants:** 19
- **Source:** OpenNeuro · **Access:** ✅ Open
- **Modalities:** sMRI, fMRI, MEG, EEG
- **Scale / size:** Small–medium; 29 GB
- **Task / paradigm:** Face perception task
- **Key strength:** Multimodal benchmarking dataset
- **Best FM use case:** Multimodal alignment; EEG/MEG/fMRI transfer; validation benchmark. Widely used for method validation.

#### Simon task MEEG

**Simon task MEEG data** — [data.ru.nl](https://data.ru.nl/collections/di/dcn/DSC_62002071_01_114)

- **Participants:** 9
- **Source:** Radboud Universiteit · **Access:** ✅ Open
- **Modalities:** MEG, EEG
- **Scale / size:** 38 GB
- **Task / paradigm:** Simon response-conflict task
- **Key strength:** Simultaneous MEG+EEG with high sensor count for response-conflict source separation
- **Best FM use case:** Multimodal alignment; EEG/MEG/fMRI transfer; validation benchmark.

### Naturalistic

Continuous, ecologically valid stimulation with rich temporal annotations — for language/audio/video-aligned training and long-context modeling.

#### Sentence-level meaning

**Constructing sentence-level meaning: an MEG study of naturalistic language comprehension** — [data.ru.nl](https://data.ru.nl/collections/di/dccn/DSC_3027007.01_206)

- **Participants:** 35
- **Source:** Radboud Universiteit · **Access:** ✅ Open
- **Modalities:** MEG, MRI
- **Scale / size:** 343 GB
- **Task / paradigm:** Naturalistic story listening
- **Key strength:** Story-listening data spanning multiple levels of natural linguistic representation
- **Best FM use case:** Language/audio/video-aligned fine-tuning; long-context temporal modeling.

#### LibriBrain100

[pnpl/LibriBrain](https://huggingface.co/datasets/pnpl/LibriBrain) + [pnpl/LibriBrain2](https://huggingface.co/datasets/pnpl/LibriBrain2)

- **Participants:** 33
- **Source:** HuggingFace · **Access:** ✅ Open
- **Modalities:** MEG, audio, text
- **Scale / size:** ~100 hours
- **Task / paradigm:** Naturalistic continuous speech listening
- **Key strength:** Deep within-subject sampling plus a cross-subject cohort
- **Best FM use case:** Word-classification benchmark; cross-subject evaluation.

*LibriBrain100 is the union of two HuggingFace repositories: [LibriBrain](#libribrain) (the single deeply-sampled participant, ~50 hours) plus `pnpl/LibriBrain2` (the additional cross-subject cohort). Both are needed to assemble the full ~100-hour, 33-participant dataset.*

#### DECAF

**DECAF (Movie watching dataset)** — [decaf-dataset.github.io](https://decaf-dataset.github.io/)

- **Participants:** 30
- **Source:** MHUG / University of Trento · **Access:** ✉️ Request-based
- **Modalities:** MEG, NIR face video, hEOG, ECG, tEMG
- **Scale / size:** 60 hours; 300 GB
- **Task / paradigm:** Naturalistic movie and music-video viewing
- **Key strength:** Naturalistic cognition/perception
- **Best FM use case:** Language/audio/video-aligned fine-tuning; long-context temporal modeling. Useful for temporal predictive modeling.

#### MEG-MASC

**MEG-MASC (Natural Speech dataset)** — [osf.io/ag3kj](https://osf.io/ag3kj/overview)

- **Participants:** 27
- **Source:** OSF · **Access:** ✅ Open
- **Modalities:** MEG + audio/text
- **Scale / size:** Small–medium
- **Task / paradigm:** Naturalistic language
- **Key strength:** High-quality temporal annotations
- **Best FM use case:** Language/audio/video-aligned fine-tuning; long-context temporal modeling. Ideal for language-aligned BFMs.

#### 10-hour within-participant narrative

**A 10-hour within-participant MEG narrative dataset** — [data.ru.nl](https://data.ru.nl/collections/di/dccn/DSC_3011085.05_995)

- **Participants:** 3
- **Source:** Radboud Universiteit · **Access:** 🔒 Restricted
- **Modalities:** MEG
- **Scale / size:** 230 GB
- **Task / paradigm:** English audiobook listening (Sherlock Holmes) across ten sessions
- **Key strength:** Deep repeated-measures narrative data with word and phoneme timing
- **Best FM use case:** Language/audio/video-aligned fine-tuning; long-context temporal modeling. Ten one-hour sessions.

#### LibriBrain

[huggingface.co/datasets/pnpl/LibriBrain/tree/main](https://huggingface.co/datasets/pnpl/LibriBrain/tree/main)

- **Participants:** 1
- **Source:** HuggingFace · **Access:** ✅ Open
- **Modalities:** MEG
- **Scale / size:** 50 hours; 87 GB
- **Task / paradigm:** Naturalistic auditory listening
- **Key strength:** Deep within-subject sampling with high-quality temporal annotations
- **Best FM use case:** Language/audio-aligned fine-tuning; long-context temporal modeling; potential for representation learning.

*This repository is also one half of [LibriBrain100](#libribrain100), which combines it with `pnpl/LibriBrain2` to reach 33 participants.*

### Task benchmark

Controlled paradigms with well-defined labels — the natural targets for decoding, few-shot adaptation, and task transfer.

#### Oscillatory building blocks

**Oscillatory building blocks underlying perceptual decision making** — [data.ru.nl](https://data.ru.nl/collections/di/dccn/DSC_3015079.01_677)

- **Participants:** 33
- **Source:** Radboud Universiteit · **Access:** 🔒 Restricted
- **Modalities:** MEG
- **Scale / size:** 452 GB
- **Task / paradigm:** Visual match-to-sample task matching orientation or spatial frequency
- **Key strength:** Pre-/retro-cue design probing orientation and spatial-frequency decisions
- **Best FM use case:** Downstream decoding; few-shot adaptation; task-transfer benchmark.

#### BCI and mental imagery

**BCI / mental imagery MEG datasets** — [springernature.figshare.com](https://springernature.figshare.com/collections/A_magnetoencephalography_dataset_for_motor_and_cognitive_imagery_BCI/5101544)

- **Participants:** 17
- **Source:** Springer Nature · **Access:** ✅ Open
- **Modalities:** MEG
- **Scale / size:** Small; 49 GB
- **Task / paradigm:** Imagery tasks
- **Key strength:** High SNR, task-specific
- **Best FM use case:** Downstream decoding; few-shot adaptation; task-transfer benchmark. Useful for decoding benchmarks.

#### Eye movement effects in MEG

[data.ru.nl](https://data.ru.nl/collections/di/dcc/DSC_2018.00111_468)

- **Participants:** 16
- **Source:** Radboud Universiteit · **Access:** 🔒 Restricted
- **Modalities:** MEG
- **Scale / size:** 127 GB
- **Task / paradigm:** Working-memory match-to-sample task with cued attention
- **Key strength:** Direct characterization of eye-movement confounds in MEG decoding
- **Best FM use case:** Downstream decoding; few-shot adaptation; task-transfer benchmark.

#### THINGS-MEG

[openneuro.org/datasets/ds004212](https://openneuro.org/datasets/ds004212/versions/3.0.0)

- **Participants:** 4
- **Source:** OpenNeuro · **Access:** ✅ Open
- **Modalities:** MEG, T1 MRI
- **Scale / size:** 377 GB
- **Task / paradigm:** Rapid visual object viewing with oddball detection
- **Key strength:** Broad object sampling across 1,854 concepts and 12 sessions
- **Best FM use case:** Downstream decoding; few-shot adaptation; task-transfer benchmark.

### Clinical and perturbation

Disease cohorts and pharmacologically induced states — for clinical fine-tuning and robustness to altered brain dynamics.

#### BioFIND

**BioFIND (Dementia)** — [portal.dementiasplatform.uk](https://portal.dementiasplatform.uk)

- **Participants:** 324
- **Source:** DPUK · **Access:** 📝 Registration needed
- **Modalities:** MEG, T1 MRI, metadata
- **Scale / size:** Medium–large
- **Task / paradigm:** Resting state
- **Key strength:** Disease-focused representation learning
- **Best FM use case:** Clinical fine-tuning; disease/altered-state robustness; potential for clinical FM.

#### Pharmacological MEG

**Pharmacological MEG datasets (tiagabine, perampanel, ketamine, and LSD)** — [dataverse.harvard.edu](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/9Q1SKM)

- **Participants:** 68
- **Source:** Harvard Dataverse · **Access:** ✅ Open
- **Modalities:** MEG
- **Scale / size:** Medium
- **Task / paradigm:** Rest, drug-induced states
- **Key strength:** Perturbation dynamics
- **Best FM use case:** Clinical fine-tuning; disease/altered-state robustness. Rare resource for causal/state modeling.

#### Auditory-to-motor entrainment in Parkinson's disease

**Impaired auditory-to-motor entrainment in Parkinson's disease** — [data.ru.nl](https://data.ru.nl/collections/di/dccn/DSC_3018009.04_857)

- **Participants:** 30
- **Source:** Radboud Universiteit · **Access:** 🔒 Restricted
- **Modalities:** MEG
- **Scale / size:** 174 GB
- **Task / paradigm:** Rhythmic auditory target detection with predictive tones and omissions
- **Key strength:** PD/control comparison of sensory versus motor entrainment
- **Best FM use case:** Clinical fine-tuning; disease/altered-state robustness.

### Specialized

Narrow-scope recordings that probe one cognitive mechanism in depth.

#### Left motor cortex and phonological discrimination

**Left Motor Cortex Contributes to Auditory Phonological Discrimination** — [borealisdata.ca](https://borealisdata.ca/dataset.xhtml?persistentId=doi:10.5683/SP3/WLOAC6)

- **Participants:** 32
- **Source:** University of Toronto · **Access:** ✅ Open
- **Modalities:** MEG
- **Scale / size:** Not specified
- **Task / paradigm:** Phonological discrimination of syllable pairs under three noise conditions
- **Key strength:** Speech-in-noise MEG probing motor-cortex contributions to phonological processing
- **Best FM use case:** Specialized fine-tuning or auxiliary evaluation; speech perception and production.

## Contributing

Contributions are welcome. Please open a pull request that adds a dataset entry following the existing format, keeping the same fields (participants, source, access, modalities, scale/size, task/paradigm, key strength, best FM use case) and adding a matching row to the [At a glance](#at-a-glance) table. Prefer datasets with a stable, citable landing page.

