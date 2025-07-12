# Mathematical Modeling for Neuroscience
## Decoding Static vs. Dynamic Visual Stimuli from Neural Activity in the Mouse Brain

This repository contains the code and analysis for a project completed in the **Mathematical Modeling for Neuroscience** course. The project investigates the differences in neural responses to static and dynamic visual stimuli in the mouse brain, using high-density neural recordings from the Allen Brain Observatory.

## 🧠 Project Overview

The brain's ability to differentiate between static and dynamic visual stimuli is a critical aspect of sensory processing. This project focuses on:

- analyzing neural activity in response to two types of visual stimuli: static natural scenes and dynamic natural movies;
- using data from neuropixels probes that record spiking activity across multiple brain regions in mice;
- applying mathematical modeling and machine learning to identify key differences in neural responses, including metrics such as firing rate, Fano factor, and latency.

## 📁 Data

The dataset used in this study is from the **Allen Brain Observatory's Visual Coding Neuropixels** project, which contains neural recordings from the following two experimental sessions:

1. **Session 798911424**:
   - includes 118 natural scenes, 2 natural movies (30s and 120s), and drifting gratings,
   - recorded neural activity across multiple brain regions including the visual cortex and hippocampal formation.

2. **Session 766640955**:
   - contains a 30s natural movie clip presented both in its original and shuffled version;
   - focuses on analyzing functional connectivity between various brain areas during stimulus presentation.

> **Note: Raw data from the Allen Brain Observatory is used via the AllenSDK.**

## 🧑‍💻 Methods

- **Spike time extraction**: Extracted spike times from the neural recordings aligned with stimulus presentations.
- **Support Vector Classifier (SVC)**: Trained to classify static vs. dynamic stimuli based on the firing rate of neurons.
- **Statistical analysis**: Employed the Mann-Whitney test to identify discriminative neurons and Kruskal-Wallis and Wilcoxon tests for comparing neural responses across different brain regions.
- **Principal Component Analysis (PCA)**: Used to visualize differences in neural activity across various stimulus conditions.

## 🎯 Key Findings

- **Perfect classification accuracy**: The SVC model achieved nearly perfect classification accuracy between static and dynamic stimuli.
- **Top discriminative neurons**: The Mann-Whitney test identified neurons with significantly different responses to static and dynamic stimuli, particularly in the **VISam** and **CA1** brain regions.
- **Neural response patterns**: PCA revealed distinct clusters for natural movies, images, and shuffled movies, with dynamic stimuli showing more coherent responses and reduced Fano factor and latency compared to static stimuli.

## 🧪 Tools & Technologies

- Python (NumPy, Pandas, SciPy, Matplotlib, Scikit-learn)
- AllenSDK (to access Allen Brain Observatory data)
- Jupyter Notebooks for interactive analysis
