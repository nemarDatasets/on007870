[![DOI](https://img.shields.io/badge/DOI-10.82901%2Fnemar.on007870-blue)](https://doi.org/10.82901/nemar.on007870)

# Appleseed MEG Dataset (BIDS)

This dataset contains the Appleseed MEG data in Brain Imaging Data Structure (BIDS) standard formnat. It includes MEG recordings from 12 participants listening to continuous narrative speech, plus an empty-room recording, along with stimulus files and derivative outputs. 

## Dataset summary

- Dataset type: raw
- BIDS version: 1.7.0
- Subjects: sub-01 through sub-12, plus sub-emptyroom
- Modality: MEG
- Stimuli: audio, gammatone feature pickles, and Praat TextGrid annotations
- Derivatives: Freesurfer outputs, MNE-related files, predictor objects, and processing scripts

## Citation

Please cite:

Brodbeck, Christian, Shohini Bhattasali, Aura AL Cruz Heredia, Philip Resnik, Jonathan Z Simon, and Ellen Lau (2022). Parallel processing in speech perception with local and global representations of linguistic context. eLife, 11, e72056. https://doi.org/10.7554/elife.72056

## Abstract

Speech processing is highly incremental. It is widely accepted that human listeners continuously use the linguistic context to anticipate upcoming concepts, words, and phonemes. However, previous evidence supports two seemingly contradictory models of how a predictive context is integrated with the bottom-up sensory input: Classic psycholinguistic paradigms suggest a two-stage process, in which acoustic input initially leads to local, context-independent representations, which are then quickly integrated with contextual constraints. This contrasts with the view that the brain constructs a single coherent, unified interpretation of the input, which fully integrates available information across representational hierarchies, and thus uses contextual constraints to modulate even the earliest sensory representations. To distinguish these hypotheses, we tested magnetoencephalography responses to continuous narrative speech for signatures of local and unified predictive models. Results provide evidence that listeners employ both types of models in parallel. Two local context models uniquely predict some part of early neural responses, one based on sublexical phoneme sequences, and one based on the phonemes in the current word alone; at the same time, even early responses to phonemes also reflect a unified model that incorporates sentence-level constraints to predict upcoming phonemes. Neural source localization places the anatomical origins of the different predictive models in nonidentical parts of the superior temporal lobes bilaterally, with the right hemisphere showing a relative preference for more local models. These results suggest that speech processing recruits both local and unified predictive models in parallel, reconciling previous disparate findings. Parallel models might make the perceptual system more robust, facilitate processing of unexpected inputs, and serve a function in language acquisition

## Directory structure

The repository currently contains the following top-level content:

```text
BIDS/
├── README.md
├── dataset_description.json
├── participants.tsv
├── participants.json
├── stimuli/
│   ├── *-gammatone.pickle
│   └── *.TextGrid
├── sub-01/
│   └── meg/
├── sub-02/
│   └── meg/
├── ...
├── sub-12/
│   └── meg/
├── sub-emptyroom/
└── derivatives/
    ├── freesurfer/
    ├── mne/
    ├── predictors/
    └── scripts/
```

Each subject folder contains a MEG data directory with BIDS-compliant files such as:

- channel descriptions
- event files
- metadata JSON files
- MEG FIF files
- a scans.tsv file

## Notes

- Subjects sub-04 and sub-05 heard stimulus 11b instead of stimulus 11.
- MRI data are not subject-specific anatomical scans; they are derived from the fsaverage template using subject-specific scaling parameters.
- Original audio files are copyrighted and cannot be shared.

## Data access and use

MEG data are stored in FIFF format and can be opened with MNE-Python. The BIDS metadata files describe the recording structure, events, channels, and task definitions for each subject.


## Correspondance

Please contact Dr. Christian Brodbeck at brodbecc@mcmaster.ca for any further details or questions.
