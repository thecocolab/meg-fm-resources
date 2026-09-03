# MEG Foundation Model Resources

> Curated datasets and models for magnetoencephalography (MEG) foundation models.

Companion resource for the perspective paper **A Roadmap for MEG Foundation Models**. It collects the public material the paper surveys, kept up to date here as the field moves.

## Resources

| | |
| :-- | :-- |
| **[Datasets](datasets.md)** | 25 public MEG datasets for pretraining, transfer, and downstream evaluation — with hosting source, access conditions, cohort size, modalities, data volume, and paradigm for each. ≈3,200 participants; 13 openly available. |
| **[Models](models.md)** | 7 MEG and MEG-inclusive foundation models — direct MEG, clinical MEG, multi-modal, and precursors — with architecture, pretraining objective, tokenization, and evaluation for each. |

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

## Contributing

Contributions are welcome. To add a dataset, open a pull request against [datasets.md](datasets.md) following the existing entry format (participants, source, access, modalities, scale/size, task/paradigm, key strength, best FM use case) and add a matching row to its at-a-glance table. To add a model, do the same in [models.md](models.md) (model type, modalities, data scale, architecture, pretraining objective, tokenization, downstream evaluation, key contribution). Prefer entries with a stable, citable landing page.
