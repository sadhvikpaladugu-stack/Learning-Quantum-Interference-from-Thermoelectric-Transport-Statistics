# Learning Quantum Interference from Thermoelectric Transport Statistics

**Researchers:** Sarayu Parsi, Sadhvik Paladugu, and Dr. Justin P. Bergfield (Illinois State University)
**Status:** Active Research (Code kept private pending publication)

## 📌 Project Overview
This project investigates the hidden transmission physics of molecular junctions by framing quantum interference as a statistical inverse problem. Single-molecule junction experiments typically rely on statistical ensembles of conductance measurements due to trace-to-trace variations in junction geometries and molecule–electrode couplings. 

Our research explores the extent to which destructive quantum-interference features can be reconstructed from simulated measurements of electrical conductance ($G$), thermopower ($S$), and electronic thermal conductance ($\kappa_e$). 

## 🔬 Core Methodology
Instead of analyzing single conductance traces, we generate synthetic break-junction-like ensembles from controlled model transmission functions. We then utilize machine learning to classify and regress hidden physical parameters.

*   **Synthetic Ensemble Generation:** We build ensembles simulating anodal resonant tunneling, quadratic transmission nodes, higher-order supernodes, and background tunneling.
*   **Statistical Feature Extraction:** We compute Landauer moments and construct physically informed statistical features, including moments, cumulants, and cross-correlations of $G$, $S$, and $\kappa_e$.
*   **Physics-Based Baselines:** We benchmark our models against known analytical diagnostics, such as the nodal anticorrelation rule ($\rho_{G,|S|} < 0$), which predicts that a transmission node can be identified when conductance and the magnitude of thermopower are anticorrelated.

## 🤖 Machine Learning Integration
To determine if we can identify broader statistical signatures of quantum interference beyond simple correlation rules, we employ several ML techniques:
*   **Models:** Logistic Regression, Decision Trees, Random Forests, Support-Vector Machines (SVM), and Shallow Neural Networks.
*   **Classification Tasks:** Distinguishing between anodal (longitudinal) and nodal (transverse) transport geometries based solely on observable ensemble-level features, explicitly hiding microscopic parameters like mean chemical potential or background transmission from the classifier.
*   **Regression Tasks:** Transitioning from simple classification to parameter reconstruction (e.g., estimating node location, node order, background transmission, and ensemble disorder).

## 🚀 Current Progress & Challenges
*   **Establishing Baselines:** Successfully validated that our full-feature machine learning classifier outperforms the single-feature analytical rule ($\rho_{G,|S|} < 0$) across tested energy ranges.
*   **Testing Identifiability & Robustness:** Systematically introducing physical complications into our synthetic data to test model limits. These complications include:
    *   Finite ensemble sizes (simulating experimental constraints)
    *   Measurement noise and coupling disorder
    *   Asymmetric lead couplings
    *   Background transmission and dephasing-like node filling

*The scripts, data simulations, and specific ML classification code for this project are currently maintained in a private environment to protect data integrity prior to formal academic publication.*
