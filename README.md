# Quantum Variational Autoencoder for Anomaly Detection in Network Traffic

This repository accompanies the capstone project titled “Quantum Anomaly Detection System for Network Traffic”, developed by Saad Bara under the supervision of Dr. Fouad Mohammed Abbou during Spring 2025. The project implements a hybrid Quantum Variational Autoencoder (Q-VAE) model to detect network intrusions in the UNSW-NB15 dataset using quantum-enhanced learning.

⸻

📘 Abstract

This project presents a hybrid quantum-classical anomaly detection system using a Q-VAE model. The system is designed to learn the statistical patterns of normal network traffic and identify deviations indicative of cyber intrusions. The model leverages quantum circuits for the encoder component and classical processing for preprocessing, optimization, and inference.

The primary dataset used is UNSW-NB15, and performance is compared against classical baselines such as Random Forests and classical autoencoders. Results show that Q-VAE can achieve comparable precision and recall, validating the feasibility of quantum machine learning (QML) in cybersecurity contexts.

⸻

🗂️ Project Structure

Q-VAE-Anomaly-Detection/
-  data: Preprocessed UNSW-NB15 data (train/test split)
-  model:  Q-VAE model architecture (Qiskit)
-  classical_baseline: Classical ML baselines (RF, AE)
-  notebooks: Development notebooks (Jupyter)
-  utils: PCA, threshold tuning, evaluation metrics
-  results: Confusion matrices, ROC, and loss curves
-  report: Capstone final report (PDF)
-  README.md                 # Project overview and instructions


⸻

🧠 Core Features
	•	Quantum Encoder: 4-qubit variational quantum circuit using amplitude encoding.
	•	Hybrid Workflow: Classical preprocessing (PCA), quantum classification, and classical postprocessing.
	•	Optimizer Experimentation: Training using both SPSA (gradient-free) and ADAM (adaptive gradient descent).
	•	Threshold Tuning: Adaptive thresholding strategy to maximize F1-score.
	•	Baseline Comparison: Compared to Random Forest and classical autoencoder.

⸻

📊 Dataset Overview
	•	Dataset: UNSW-NB15
	•	Features: Original 45 features reduced to 4 via PCA.
	•	Samples: 175,341 training samples, 82,332 test samples.
	•	Labeling: 0 (normal), 1 (anomaly).

⸻

🚀 How to Run

Installation

# Clone repo
$ git clone https://github.com/saadbara/qvae-anomaly-detection.git
$ cd QVAE-Research


Run Training

# Train Q-VAE model
$ python model/train_qvae.py --epochs 50 --optimizer SPSA --qubits 4

Run Classical Baseline

# Run Random Forest
$ python classical_baseline/random_forest.py

Evaluate Model

$ python utils/evaluate.py --threshold 0.5


⸻

📈 Results Summary

Model	        Precision	Recall	  F1-Score	Accuracy
Initial Q-VAE   0.68	         0.98	     0.80	   0.67
Improved Q-VAE	0.85	         0.90	     0.87	   0.88
Classical RF	0.82	         0.88	     0.85	   0.86


⸻

📚 Research Contributions
	•	Designed a 4-qubit, 8-layer variational circuit for anomaly detection.
	•	Demonstrated effective mitigation of barren plateaus using optimizer switching.
	•	Introduced threshold tuning mechanism for better classification balance.
	•	Achieved quantum-classical parity in cybersecurity anomaly detection.

⸻

📎 Report and Documentation
	•	📄 Capstone_Report_Final_SaadBara.pdf

⸻

🧪 Technologies Used
	•	Quantum: Qiskit, SamplerQNN
	•	Classical ML: Scikit-learn, PCA, Random Forest
	•	Programming: Python, Jupyter
	•	Visualization: Matplotlib, Seaborn

⸻

🧭 Future Directions
	•	Extend to online (streaming) intrusion detection.
	•	Test on real-time packet captures.
	•	Compare with other QML models (e.g., QGAN, QBoost).
	•	Migrate to real quantum hardware once more stable.

⸻

👨‍💻 Author

Saad Bara
Al Akhawayn University
📧 saad.bara@aui.ma
🔗 LinkedIn

