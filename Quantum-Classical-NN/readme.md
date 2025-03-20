# Hybrid Quantum-Classical Machine Learning Hackathon Projects

Designed for students with **10 minutes of access** to IBM quantum computers (**max 127 qubits**).

---

## **1. Hybrid Quantum-Classical Neural Network for Classification**
### **Objective:**  
Combine Quantum Neural Networks (QNNs) with classical layers to classify structured data.

### **Dataset Options:**
- **[UCI Mushroom Dataset](https://archive.ics.uci.edu/ml/datasets/Mushroom)** (edibility classification)
- **[MNIST (Downsampled to 4x4)](http://yann.lecun.com/exdb/mnist/)** (Handwritten digits)
- **[Wine Quality Dataset](https://archive.ics.uci.edu/ml/datasets/Wine+Quality)** (Red vs. White wine)

### **Steps:**
1. **Use [Quantum Feature Maps](https://qiskit.org/textbook/ch-machine-learning/quantum-feature-maps.html)** to encode data.
2. **Train a hybrid model with QNN layers via [TorchConnector](https://qiskit.org/documentation/machine-learning/tutorials/05_torch_connector.html).**
3. **Evaluate accuracy against fully classical neural networks.**

### **IBM Q Execution Plan:**
- Limit **QNN circuit depth** to keep execution time feasible.
- Use **QNN for feature extraction**, followed by classical classification.

---

## **2. Hybrid Quantum CNN for Image Recognition**
### **Objective:**  
Enhance a classical convolutional neural network (CNN) with a quantum layer for improved feature extraction.

### **Dataset Options:**
- **[Fashion-MNIST](https://github.com/zalandoresearch/fashion-mnist)** (Clothing classification)
- **[Retinal OCT Dataset](https://www.kaggle.com/datasets/paultimothymooney/kermany2018)** (Eye disease classification)

### **Steps:**
1. **Use a classical CNN for initial feature extraction.**
2. **Integrate a Quantum Neural Network (QNN) layer using `TorchConnector`.**
3. **Train and compare hybrid model performance with classical CNNs.**

### **IBM Q Execution Plan:**
- Limit quantum circuit execution to **≤10 qubits**.
- Apply **hybrid training** where only QNN weights are optimized on IBMQ.

---

## **3. Hybrid QNN for Time-Series Anomaly Detection**
### **Objective:**  
Use Quantum Neural Networks (QNNs) to detect anomalies in time-series data, enhancing traditional detection methods.

### **Dataset Options:**
- **[KDD Cup '99](http://kdd.ics.uci.edu/databases/kddcup99/kddcup99.html)** (Network Intrusion Data)
- **[Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)** (Financial anomaly detection)

### **Steps:**
1. **Transform time-series data into a feature representation.**
2. **Use a hybrid QNN to extract complex patterns.**
3. **Compare quantum anomaly detection vs. classical methods.**

### **IBM Q Execution Plan:**
- Apply **[Grover’s Amplitude Amplification](https://qiskit.org/textbook/ch-algorithms/grover.html)** for anomaly detection.
- Optimize **QNN layers to run efficiently on quantum hardware.**

---

## **4. Hybrid Quantum-Classical Regression Model**
### **Objective:**  
Use Quantum Neural Networks (QNNs) for regression tasks, improving generalization over classical models.

### **Dataset Options:**
- **[Boston Housing Dataset](https://www.kaggle.com/datasets/vikrishnan/boston-house-prices)** (Predict house prices)
- **[Sine Wave Regression](https://qiskit.org/documentation/machine-learning/tutorials/04_qnn_regression.html)** (Synthetic data for function approximation)

### **Steps:**
1. **Use a hybrid QNN to model nonlinear relationships in data.**
2. **Train using a loss function such as Mean Squared Error (MSE).**
3. **Compare QNN regression with classical linear regression and neural networks.**

### **IBM Q Execution Plan:**
- Use **QNN feature maps** to encode data into qubits.
- Keep **circuit depth low** for fast execution on IBMQ.

---

## **Summary of Feasibility**
| **Project** | **Qubits Needed** | **Feasibility with 10-Minute IBMQ Access** | **Challenges & Mitigations** |
|------------|------------------|--------------------------------------|------------------------------|
| **Hybrid Quantum-Classical NN** | 6-12 | ✅ **Feasible** | Keep QNN layers shallow and efficient. |
| **Hybrid Quantum CNN** | 6-10 | ⚠️ **Partially Feasible** | Limit QNN layers and offload feature extraction to classical CNN. |
| **Hybrid QNN for Anomaly Detection** | 8-12 | ⚠️ **Feasible but Limited** | Use hybrid models to balance accuracy and execution time. |
| **Hybrid QNN Regression** | 6-10 | ✅ **Feasible** | Optimize quantum circuit depth for practical use. |

---



