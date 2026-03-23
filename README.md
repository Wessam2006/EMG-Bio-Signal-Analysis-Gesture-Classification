# EMG-Bio-Signal-Analysis-Gesture-Classification
Overview

This notebook simulates EMG (electromyography) bio-signal analysis and gesture classification using a dummy dataset in Google Colab. It demonstrates:

Loading EMG data (manual text files or dummy data if none exists)
Structuring signals, labels, and timestamps into NumPy arrays
Visualizing multi-channel EMG signals

Note: In this Colab version, a small dummy dataset is automatically generated to allow the code to run without the official UCI dataset.

Directory Structure
/content/emg_data_for_gestures   # folder for .txt EMG files
/content/outputs                 # folder for saved figures and CSVs

Manual EMG files: Space-separated text files per subject:

time_ms CH1 CH2 CH3 ... CH8 class
Outputs: Figures and structured CSVs saved here
MANUAL_DATA_DIR = "/content/emg_data_for_gestures"
OUT_DIR = "/content/outputs"
FS = 200  # Sampling rate (Hz)
CHANNEL_NAMES = ["CH1", "CH2", ..., "CH8"]
Configuration
MANUAL_DATA_DIR = "/content/emg_data_for_gestures"
OUT_DIR = "/content/outputs"
FS = 200  # Sampling rate (Hz)
CHANNEL_NAMES = ["CH1", "CH2", ..., "CH8"]
GESTURE_LABELS = {0: "Unmarked", 1: "Rest", 2: "Fist", ... , 7: "Extended Palm"}
MAX_SUBJECTS = 3
MAX_SUBJECTS limits how many subjects are loaded (memory-friendly in Colab)
FS is the EMG sampling rate (200 Hz for MYO bracelet)
GESTURE_LABELS maps numeric class IDs to gesture names
Features
Automatic dummy data generation if no text files exist
Loads EMG signals into NumPy arrays
signals[subject_id] → EMG channels
labels[subject_id] → gesture labels
times[subject_id] → timestamps in seconds
Visualization
Multi-channel EMG plot for the first subject
Overlaid channels with offset for clarity
Running the Code
Open the Colab notebook.
Run all cells.
If no EMG files exist in MANUAL_DATA_DIR, the notebook will generate dummy data automatically.
A plot of the first 200 samples of subject 1’s EMG channels will be displayed.
Output
Figures saved to /content/outputs
Example: raw_emg_subject1.png
Structured data can be exported as CSV for further processing.
ip install numpy pandas matplotlib
No external EMG datasets required; dummy data is automatically generated
Compatible with Google Colab
Notes
This is a minimal Colab-friendly version of EMG processing.
