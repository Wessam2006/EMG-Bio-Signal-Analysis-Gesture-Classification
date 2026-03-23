# EMG Gesture Analysis 

## Overview
This notebook simulates EMG (electromyography) bio-signal analysis and gesture classification using a dummy dataset. It:

- Loads EMG data from manual `.txt` files, or generates dummy data if none exist
- Structures signals, labels, and timestamps into NumPy arrays
- Plots multi-channel EMG signals for the first subject

---

## Setup
```python
MANUAL_DATA_DIR = "/content/emg_data_for_gestures"
OUT_DIR = "/content/outputs"
FS = 200  # Sampling rate
CHANNEL_NAMES = ["CH1", "CH2", "CH3", "CH4", "CH5", "CH6", "CH7", "CH8"]
GESTURE_LABELS = {
    0: "Unmarked", 1: "Rest", 2: "Fist", 3: "Wrist Flexion",
    4: "Wrist Extension", 5: "Radial Deviation", 
    6: "Ulnar Deviation", 7: "Extended Palm"
}
MAX_SUBJECTS = 3
