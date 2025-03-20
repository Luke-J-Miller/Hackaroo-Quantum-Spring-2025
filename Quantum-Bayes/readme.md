# Quantum Bayesian Inference (QBI) Hackathon Projects

Designed for students with **10 minutes of access** to IBM quantum computers (**max 127 qubits**).

---

## **1. Quantum Bayesian Classifier**
### **Objective:**  
Build a quantum Bayesian classifier that learns probabilities from a dataset and classifies new samples using **[Quantum Bayesian Inference (QBI)](https://qiskit.org/documentation/machine-learning/tutorials/08_quantum_bayesian_inference.html)**.

### **Dataset Options:**
- **[UCI Mushroom Dataset](https://archive.ics.uci.edu/ml/datasets/Mushroom)** (edibility based on features)
- **[UCI Breast Cancer Dataset](https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+%28Diagnostic%29)** (binary classification)
- **[MNIST (Downsampled to 4x4)](http://yann.lecun.com/exdb/mnist/)** (digit classification)

### **Steps:**
1. **Encode features** into quantum Bayesian networks.
2. **Train Bayesian networks** to model class probabilities.
3. **Perform Quantum Inference** to classify new inputs.
4. **Compare with [Classical Bayesian Inference](https://en.wikipedia.org/wiki/Bayesian_inference).**

### **IBM Q Execution Plan:**
- Limit quantum network to **≤10 nodes** for efficiency.
- Use **[Quantum Rejection Sampling](https://arxiv.org/abs/quant-ph/0007020)** to refine probability estimates.
- Compare quantum classifier vs. classical Bayesian classifier.

---

## **2. Quantum Bayesian Network for Anomaly Detection**
### **Objective:**  
Use QBI to detect anomalies in financial transactions, network logs, or medical data.

### **Dataset Options:**
- **[KDD Cup '99](http://kdd.ics.uci.edu/databases/kddcup99/kddcup99.html)** (Network Intrusion Data)
- **[Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)** (Kaggle)
- **[MIT-BIH Arrhythmia Dataset](https://www.physionet.org/content/mitdb/1.0.0/)** (Anomaly Detection in ECG Signals)

### **Steps:**
1. **Train Bayesian networks** on normal data distribution.
2. **Introduce anomalies** and test detection.
3. **Use Quantum Rejection Sampling** to infer likelihood of anomalies.
4. **Compare with [Classical Bayesian Detection](https://en.wikipedia.org/wiki/Anomaly_detection).**

### **IBM Q Execution Plan:**
- Encode **limited feature sets** into Bayesian networks.
- Use **[Grover’s Amplitude Amplification](https://qiskit.org/textbook/ch-algorithms/grover.html)** for efficient rejection sampling.
- Evaluate performance metrics (False Positives, True Positives).

---

## **3. Hybrid Quantum-Classical Bayesian Inference**
### **Objective:**  
Use quantum inference to **speed up complex Bayesian networks** while handling computationally expensive parts classically.

### **Dataset Options:**
- **[Medical Decision Making](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4601104/)** (Likelihood of Disease Given Symptoms)
- **[Financial Risk Assessment](https://www.sciencedirect.com/science/article/abs/pii/S0377221721003891)** (Bayesian Portfolio Models)

### **Steps:**
1. **Construct a hybrid Bayesian network** where:
   - Simple probability updates are handled classically.
   - Complex probabilistic inferences use quantum circuits.
2. **Run inference on IBMQ** and compare against classical inference methods.

### **IBM Q Execution Plan:**
- Use **a small quantum circuit (≤10 qubits) for critical inferences**.
- Optimize classical-quantum interaction for efficiency.
- Compare results to fully classical Bayesian inference.

---

## **4. Quantum Causal Inference**
### **Objective:**  
Use QBI to **test causal relationships** instead of just correlations.

### **Dataset Options:**
- **[Health Study Data](https://www.cdc.gov/nchs/nhanes/index.htm)** (Does Smoking Cause Cancer?)
- **[World Bank Economic Indicators](https://databank.worldbank.org/source/world-development-indicators)** (Does Inflation Affect Employment?)

### **Steps:**
1. **Model causal relationships** using [Bayesian Networks](https://en.wikipedia.org/wiki/Bayesian_network).
2. **Use Quantum Bayesian Inference** to test intervention-based causal effects.
3. **Compare results with [Classical Causal Inference](https://en.wikipedia.org/wiki/Causal_inference).**

### **IBM Q Execution Plan:**
- Use **Grover’s amplitude amplification** to simulate interventions efficiently.
- **Limit quantum network to key causal nodes** for efficiency.

---

## **Summary of Feasibility**
| **Project** | **Qubits Needed** | **Feasibility with 10-Minute IBMQ Access** | **Challenges & Mitigations** |
|------------|------------------|--------------------------------------|------------------------------|
| **Quantum Bayesian Classifier** | 6-10 | ✅ **Feasible** | Limit dataset size, run batch queries. |
| **Quantum Anomaly Detection** | 6-12 | ⚠️ **Feasible but Limited** | Reduce feature set to keep circuit depth low. |
| **Hybrid Quantum-Classical Bayesian Inference** | 6-10 | ✅ **Feasible** | Offload non-critical inference to classical methods. |
| **Quantum Causal Inference** | 8-12 | ⚠️ **Partially Feasible** | Optimize quantum sampling to stay within execution time limits. |

---

