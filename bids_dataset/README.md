# Creativity in Vitro – EEG Dataset

This dataset contains EEG recordings collected across three sessions from a single participant (Lina Lopes) using OpenBCI hardware. The recordings explore how auditory stimuli — both musical and spoken — relate to imagination and mental state in the context of an artistic-scientific research project.

## Overview

- Subject: Lina Lopes (`sub-lina`)
- Total Sessions: 3 (`ses-01`, `ses-02`, `ses-03`)
- Device:
  - Sessions 1 & 2: OpenBCI Cyton + Daisy (14 active gel-based channels) at 125 Hz
  - Session 3: OpenBCI Cyton (8 active gel-based channels) at 250 Hz
- Electrode Layout: 10-20 system
- Recording Environment: Eyes closed, relaxed body posture

## Sessions

### Session 1 – `task-visualize`
Participants listened to a musical loop composed of one melodic phrase followed by six lyrical phrases, repeated three times. The instruction was to keep eyes closed and generate vivid mental images for each lyrical phrase.

### Session 2 – `task-sing`
Same musical structure as Session 1. This time, the instruction was to internally sing along with the lyrical phrases, imagining the act of singing without vocalizing.

### Session 3 – `task-sunimagery`
Participants listened to a structured sequence of verbal instructions alternating between “Imagine the sun on your face” and “Relax”, repeated over 30 cycles. The goal was to engage in alternating visual imagery and mental rest.

## File Organization

- `sub-lina/`: EEG data organized by session and run
- `stimuli/`: Auditory stimuli used in each task (`.wav`)
- `sourcedata/`: Original raw OpenBCI `.csv` and `.txt` files
- `derivatives/`: Filtered, ICA-cleaned, and QA-assessed files
- `task-*.json`: Task-level descriptions for each session
- `*_events.tsv`: Timestamped annotations of stimuli
- `*_channels.tsv` and `*_impedance.tsv`: Optional metadata for each session

## How to Use

Each run includes:
- EEG recording in `.fif` format
- Sidecar metadata (`*_eeg.json`)
- Event annotations (`*_events.tsv`)
- Optional: channel descriptions and impedance data

The audio stimuli used are available in `stimuli/`, and each run is annotated with consistent event timing for repeatability.

## License

This dataset is distributed under the **Creative Commons CC-BY 4.0** license.

## Citation

Please cite as:
**Creativity in Vitro – EEG Dataset (2025)**
Lina Lopes
Zenodo DOI: `10.5281/zenodo.xxxxx`

## Acknowledgements

Data collected and structured using OpenBCI hardware and MNE-Python.
Supported by Cloudwalk and the Creativity in Vitro research initiative.
