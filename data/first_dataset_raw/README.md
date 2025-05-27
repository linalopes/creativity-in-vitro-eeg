# EEG Dataset – OpenBCI Raw Recordings (Cyton + Daisy, 14 Channels)

## Overview

This dataset contains raw EEG data recorded using the OpenBCI Cyton board with the Daisy extension (14 channels total). The recordings were made as part of the project **Creativity in vitro**, which investigates how brain activity responds to lyrical and semantic patterns in music.

Lina, the participant listened to 20 repeated loops of 3 of the first six phrases of the song *Aquarela* by Toquinho. These 20 sessions were recorded consecutively in one continuous session, without restarting the OpenBCI GUI.

---

## Files

All 20 recording sessions were captured in a single streaming session using the OpenBCI GUI, which generated one continuous file for the entire sequence. This resulted in one `.csv` file and 20 `.txt` log file containing all recordings sequentially.

These 20 sessions are distinguishable via timestamp gaps in the file and were later segmented programmatically.

### 1. `BrainFlow-RAW-*.csv`
- Continuous EEG data for all 20 loops (recorded without restarting the GUI)
- **Format:** tab-separated values
- **Main columns:**
  - Column 0: Timestamp (Unix format, in seconds)
  - Columns 1–16: EEG signals from channels 1–16 (in microvolts)
  - Additional columns include accelerometer and system values (dropped in preprocessing)

### 2. `OpenBCI-RAW-*.txt`
- Backup text log of the same 20 recording session
- Includes:
  - Sample index
  - EEG values per channel
  - Formatted timestamps
  - Epoch timestamp (Unix time)
  - Marker channel (0 - since no custom triggers were added)
- Useful for verifying timing or reconstructing session conditions in the OpenBCI GUI.

---

## Hardware Setup

- **Board:** OpenBCI Cyton + Daisy
- **Channels:** 14 EEG channels used (out of 16 available); channels 9 and 10 were intentionally left unconnected for spatial consistency with the 10–20 system layout.
- **Sampling rate:** ~125 Hz
- **Reference (SRB):** Connected to right mastoid
- **Ground (BIAS):** Connected to left mastoid
- **Electrodes:** 10–20 system with gel electrodes

> Note: The headplot in the OpenBCI GUI does not display Fz and Pz positions (used in channels 13 and 14), but these positions are included in this dataset.
---

## Channel Mapping

| Channel Index | Connector | 10–20 Position | Brain Region        |
|---------------|-----------|----------------|---------------------|
| 0             | N1P       | Fp1            | Frontal (left)      |
| 1             | N2P       | Fp2            | Frontal (right)     |
| 2             | N3P       | C3             | Central (left)      |
| 3             | N4P       | C4             | Central (right)     |
| 4             | N5P       | T3             | Temporal (left)     |
| 5             | N6P       | T4             | Temporal (right)    |
| 6             | N7P       | O1             | Occipital (left)    |
| 7             | N8P       | O2             | Occipital (right)   |
| 8             | N9P       | —              | — (not used)        |
| 9             | N10P      | —              | — (not used)        |
| 10            | N11P      | F3             | Frontal (left)      |
| 11            | N12P      | F4             | Frontal (right)     |
| 12            | N13P      | Fz             | Frontal (midline)   |
| 13            | N14P      | Pz             | Parietal (midline)  |
| 14            | N15P      | P3             | Parietal (left)     |
| 15            | N16P      | P4             | Parietal (right)    |

> Note: Channels 8 and 9 (N9P and N10P) were intentionally left unconnected to maintain spatial alignment in the 10–20 system layout. Only 14 of the 16 channels contain EEG data.

---
## Protocol Summary

- Participant sat comfortably, eyes closed, and remained still during recording
- EEG was recorded using the OpenBCI GUI (Cyton + Daisy, 14 channels)
- Impedance was tested and adjusted before each session
- Recording was initiated by clicking “Start Streaming” in the GUI
- A ~6-second stabilization period was observed before playback
- Audio stimulus was played via AirPods, consisting of 3 repetitions of the first 6 phrases of *Aquarela* by Toquinho
- Total audio duration: approximately 2 minutes and 13 seconds
- After each loop of 6 phrases, the participant blinked intentionally 3 times, providing a visible signal in the EEG for segmentation
- No additional external triggers or markers were used
- Recording was continuous for ~2 minutes and 20 seconds
- Impedance values were visually verified before each session and kept within acceptable limits (< 100 kΩ for all active channels)

---

## Notes

- All EEG values are in microvolts (µV)
- No markers/events were manually triggered
- Use the `.csv` files for signal analysis
- Use the `.txt` files for timestamp and logging verification on OpenBCI GUI
- The 20 sessions needs to be segmented using gaps in the `timestamp` field.

---

## License

This dataset is shared for non-commercial research and educational use.
Please cite the project **Creativity in vitro** by Lina Lopes & Eduardo Padilha when referencing this data.
