Overview

This notebook simulates EMG (electromyography) bio-signal analysis and gesture classification using a dummy dataset. It:

Loads EMG data (manual .txt files or generates dummy data)
Structures signals, labels, and timestamps into NumPy arrays
Plots multi-channel EMG signals
##Setup
MANUAL_DATA_DIR = "/content/emg_data_for_gestures"
OUT_DIR = "/content/outputs"
FS = 200  # Sampling rate
CHANNEL_NAMES = ["CH1", "CH2", ..., "CH8"]
GESTURE_LABELS = {0:"Unmarked",1:"Rest",2:"Fist",...,7:"Extended Palm"}
MAX_SUBJECTS = 3

Automatically creates dummy data if no .txt files are found.
First subject’s EMG signals are plotted with channel offsets.

##Output

Figures saved in /content/outputs
Structured EMG data available as NumPy arrays

##Dependencies

pip install numpy pandas matplotlib
Fully Colab-compatible, no external dataset required.

