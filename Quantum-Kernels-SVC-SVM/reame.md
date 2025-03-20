# Quantum Kernel-Based Machine Learning Hackathon Projects

Designed for students with **10 minutes of access** to IBM quantum computers (**max 127 qubits**).

---

## **1. Quantum Support Vector Machine (QSVC) for Classification**
### **Objective:**  
Use a **Quantum Kernel Estimator** with a Support Vector Machine (SVM) to classify structured data.

### **Dataset Options:**
- **[Iris Dataset](https://scikit-learn.org/stable/auto_examples/datasets/plot_iris_dataset.html)** (Flower classification)
- **[Breast Cancer Dataset](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_breast_cancer.html)** (Binary classification)
- **[Wine Dataset](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_wine.html)** (Quality classification)

### **Steps:**
1. **Use a Quantum Feature Map** to encode data into qubits.
2. **Compute the Quantum Kernel Matrix** using `FidelityQuantumKernel`.
3. **Train an SVM model** with the quantum kernel.
4. **Compare with classical SVM using RBF and polynomial kernels.**

### **IBM Q Execution Plan:**
- Use **≤10 qubits** to compute the kernel matrix.
- Train on **a simulator**, then test inference on IBM hardware.

🔗 **References:**
- [Quantum Kernel Methods in Qiskit](https://qiskit.org/documentation/machine-learning/tutorials/06_quantum_kernel.html)

---

## **2. Pegasos Quantum SVM for Faster Classification**
### **Objective:**  
Implement a **Pegasos Quantum Support Vector Classifier (Pegasos QSVC)** for improved training efficiency.

### **Dataset Options:**
- **[UCI Spam Dataset](https://archive.ics.uci.edu/ml/datasets/spambase)** (Spam detection)
- **[MNIST (Downsampled to 4x4)](http://yann.lecun.com/exdb/mnist/)** (Handwritten digit classification)

### **Steps:**
1. **Use a Quantum Kernel Estimator** to compute the kernel matrix.
2. **Train a Pegasos QSVC**, an optimization-based quantum SVM.
3. **Compare training time with classical QSVC.**

### **IBM Q Execution Plan:**
- Use **≤12 qubits** to compute the quantum kernel.
- Train on a simulator and test classification accuracy.

🔗 **References:**
- [Pegasos Quantum SVM](https://home.ttic.edu/~nati/Publications/PegasosMPB.pdf)
- [Qiskit PegasosQSVC Implementation](https://qiskit.org/documentation/machine-learning/tutorials/07_pegasos_qsvc.html)

---

## **3. Quantum Kernel Alignment for Optimized Classification**
### **Objective:**  
Use **Quantum Kernel Alignment (QKA)** to optimize a quantum kernel for classification tasks.

### **Dataset Options:**
- **[Ad Hoc Quantum Dataset](https://qiskit.org/documentation/machine-learning/stubs/qiskit_machine_learning.datasets.ad_hoc_data.html)** (Synthetic classification data)
- **[UCI Credit Card Default Dataset](https://www.kaggle.com/datasets/uciml/default-of-credit-card-clients-dataset)** (Financial risk assessment)

### **Steps:**
1. **Use a Trainable Quantum Feature Map** to construct the initial quantum kernel.
2. **Train the kernel using `QuantumKernelTrainer`** to maximize SVM margin.
3. **Compare optimized quantum kernel vs. untrained kernel.**

### **IBM Q Execution Plan:**
- Use **≤10 qubits** for kernel computation.
- Train on a simulator and validate results on IBMQ.

🔗 **References:**
- [Quantum Kernel Training in Qiskit](https://qiskit.org/documentation/machine-learning/tutorials/08_quantum_kernel_training.html)

---

## **4. Hybrid Quantum Kernel PCA for Feature Extraction**
### **Objective:**  
Use **Quantum Kernel Principal Component Analysis (KPCA)** to extract quantum-enhanced features.

### **Dataset Options:**
- **[Fashion-MNIST](https://github.com/zalandoresearch/fashion-mnist)** (Image feature extraction)
- **[Retinal OCT Dataset](https://www.kaggle.com/datasets/paultimothymooney/kermany2018)** (Medical image feature extraction)

### **Steps:**
1. **Use a Quantum Kernel to compute a similarity matrix.**
2. **Apply KPCA to reduce feature dimensionality.**
3. **Use extracted quantum features in a classical classifier.**

### **IBM Q Execution Plan:**
- Compute **quantum kernel similarity matrix using ≤12 qubits**.
- Use IBMQ to **compute KPCA projections**.

🔗 **References:**
- [Kernel PCA with Quantum Kernels](https://qiskit.org/documentation/machine-learning/tutorials/09_quantum_kernel_pca.html)

---

## **Summary of Feasibility**
| **Project** | **Qubits Needed** | **Feasibility with 10-Minute IBMQ Access** | **Challenges & Mitigations** |
|------------|------------------|--------------------------------------|------------------------------|
| **Quantum SVM for Classification** | 6-10 | ✅ **Feasible** | Limit dataset size, use efficient kernel estimation. |
| **Pegasos Quantum SVM** | 8-12 | ⚠️ **Feasible but Limited** | Optimize hyperparameters to improve training efficiency. |
| **Quantum Kernel Alignment for Optimization** | 6-10 | ✅ **Feasible** | Use small datasets for fast convergence. |
| **Hybrid Quantum Kernel PCA** | 8-12 | ⚠️ **Partially Feasible** | Limit feature extraction to a small subset. |

---

