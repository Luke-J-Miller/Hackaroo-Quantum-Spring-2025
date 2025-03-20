# Quantum Convolutional Neural Network (QCNN) Hackathon Projects

Designed for students with **10 minutes of access** to IBM quantum computers (**max 127 qubits**).

---

## **1. Quantum Convolutional Neural Network for Image Classification**
### **Objective:**  
Develop a Quantum Convolutional Neural Network (QCNN) to classify small images, inspired by classical CNNs but leveraging quantum feature encoding and entanglement.

### **Dataset Options:**
- **[MNIST (Downsampled to 4x4)](http://yann.lecun.com/exdb/mnist/)** (Handwritten digits)
- **[Fashion-MNIST](https://github.com/zalandoresearch/fashion-mnist)** (Clothing items)
- **[Synthetic Quantum Dataset](https://qiskit.org/textbook/ch-machine-learning/machine-learning-qiskit-pytorch.html)**

### **Steps:**
1. **Apply [Quantum Feature Maps](https://qiskit.org/textbook/ch-machine-learning/quantum-feature-maps.html)** to encode classical images.
2. **Build Quantum Convolutional and Pooling Layers** as described in **[Quantum CNN theory](https://arxiv.org/abs/1904.04767)**.
3. **Train a QCNN** using Qiskit's `NeuralNetworkClassifier`.
4. **Evaluate accuracy** and compare with classical CNNs.

### **IBM Q Execution Plan:**
- Limit feature map depth to **keep execution time within 10 minutes**.
- Train using a small batch size **to avoid long optimization times**.
- Use **quantum pooling** to **reduce qubit usage**.

---

## **2. Quantum Edge Detection with QCNNs**
### **Objective:**  
Use a Quantum CNN to detect edges in images, a common computer vision task in classical CNNs.

### **Dataset Options:**
- **[Canny Edge Detection Dataset](https://github.com/phillipi/pix2pix)**
- **[BSDS500](https://www2.eecs.berkeley.edu/Research/Projects/CS/vision/grouping/resources.html)**

### **Steps:**
1. **Apply Quantum Feature Maps** to encode grayscale images.
2. **Define Quantum Convolutional Filters** that highlight edges.
3. **Compare quantum vs. classical edge detection (e.g., Sobel operator).**
4. **Test performance on IBM Quantum hardware.**

### **IBM Q Execution Plan:**
- Use **shallow depth circuits** to allow execution within 10 minutes.
- Compare **quantum circuits vs. classical algorithms** for edge detection.

---

## **3. Hybrid Quantum-Classical CNN for Medical Imaging**
### **Objective:**  
Combine Quantum CNNs with classical CNNs to classify medical images, leveraging quantum circuits for feature extraction.

### **Dataset Options:**
- **[COVID-19 Chest X-ray Dataset](https://www.kaggle.com/datasets/tawsifurrahman/covid19-radiography-database)**
- **[Retinal OCT Dataset](https://www.kaggle.com/datasets/paultimothymooney/kermany2018)** (Eye disease classification)

### **Steps:**
1. **Use a Quantum Feature Map** to encode images into qubits.
2. **Extract quantum features** using a QCNN.
3. **Feed quantum-extracted features into a classical CNN.**
4. **Compare accuracy with fully classical CNNs.**

### **IBM Q Execution Plan:**
- Run **quantum feature extraction on IBMQ**, but use classical training.
- Limit **quantum convolutional layers** to **≤10 qubits**.
- Use **classical pooling layers** to reduce qubit overhead.

---

## **4. Quantum CNN for Anomaly Detection in Time-Series Data**
### **Objective:**  
Apply QCNNs to detect anomalies in time-series data, useful for financial fraud detection and cybersecurity.

### **Dataset Options:**
- **[KDD Cup '99](http://kdd.ics.uci.edu/databases/kddcup99/kddcup99.html)** (Network Intrusion Data)
- **[Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)** (Anomaly detection in finance)

### **Steps:**
1. **Transform time-series data into 2D representations.**
2. **Apply a QCNN** to detect anomalies based on learned patterns.
3. **Evaluate performance vs. classical anomaly detection methods.**

### **IBM Q Execution Plan:**
- Use **Grover’s Amplitude Amplification** for efficient pattern search.
- Limit **circuit depth to allow real-time anomaly detection.**

---

## **Summary of Feasibility**
| **Project** | **Qubits Needed** | **Feasibility with 10-Minute IBMQ Access** | **Challenges & Mitigations** |
|------------|------------------|--------------------------------------|------------------------------|
| **Quantum CNN for Image Classification** | 6-12 | ✅ **Feasible** | Limit dataset size, use efficient pooling. |
| **Quantum Edge Detection** | 6-10 | ✅ **Feasible** | Optimize convolutional layers for execution time. |
| **Hybrid Quantum-Classical CNN** | 6-12 | ⚠️ **Partially Feasible** | Offload classical CNN components for efficiency. |
| **Quantum CNN for Anomaly Detection** | 8-12 | ⚠️ **Feasible but Limited** | Use hybrid models for practical execution time. |

---


