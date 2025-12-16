# EMG-Based_Neuropathy_Diagnosis

Repository of the paper named "SHAP-Guided LightGBM Classification of Neuropathic EMG Signals", submitted at ACIIDS 2026 and available in this repository, which extends the research started with:
M. Coppotelli, D. Albert, J. G. Barrena, R. E. Khoury, P. Conde-Cespedes and M. Trocan, "Machine Learning Models for EMG-Based Diagnosis of Neuromuscular Disorders," 2025 20th International Conference on PhD Research in Microelectronics and Electronics (PRIME), Taormina, Italy, 2025, pp. 1-4, doi: 10.1109/PRIME66228.2025.11203505.

## EMG Dataset Repository

The original dataset: EMG Dataset Repository is obtained from:
A. Messekher, S. Mekaooui, M. Kedir-Talha, M. I. Kediha and F. Mostefaoui, Electromyographic data recordings during isometric contractions of the biceps brachii and deltoid collected from patients and healthy subjects, version V1, Mendeley Data, 2023. DOI: 10.17632/543xpjycj9.1.
\newline
It contains 397 5-second EMG recordings sampled at 32768 Hz, in 397 .asc files containing series of EMG aplitude values in microVolts.
\newline
The dataset is organised as follows:
In EMG Dataset Repository there are two directories: 01_Deltoid and 02_Biceps Brachii;
In both of them there are three directories: Healthy, Myopathy, and Neuropathy;
Each of them contains several .asc files with EMG recordings.
\newline
It contains the following EMG recordings:
100 Healthy Deltoid
100 Healthy Biceps Brachii
50 Myopathy Deltoid
47 Myopathy Biceps Brachii
50 Neuropathy Deltoid
50 Neuropathy Biceps Brachii
\newline
EMG files are named as follows:
EMG _009 _05_ RD_Hea.asc
EMG _109 _08_ LD_Myo.asc
EMG _359 _55_ RB_Neu.asc

where the first three digits are a unique identifier of the EMG recording; the second two digits are an identifier of the patient in its group (Healthy, Myopathy or Neuropathy); RD, LD, RB, and LB stand for Right and Left Deltoid and Biceps Brachii; Hea, Myo, and Neu stand for Healthy, Myopathy, and Neuropathy.

## features_dataset_healthy_vs_neuropathy_8_20_2000_3.csv

This is a dataset we generated from EMG Dataset Repository using EMG_dataset.ipynb.
In contains the following samples:
50 Healthy Deltoid
50 Healthy Biceps
50 Neuropathy Deltoid
50 Neuropathy Biceps

Instead of the EMG recording, it contains vectors of 17 features extracted from each EMG sample, that have been used to train a LightGBM classificator.


