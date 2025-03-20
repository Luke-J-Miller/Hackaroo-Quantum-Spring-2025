# Quantum-Enhanced Classification with Variational Quantum Circuits (VQC)

Designed for students with **10 minutes of access** to IBM quantum computers (**max 127 qubits**).

---

## **1. Variational Quantum Circuit (VQC) Classifier**
### **Objective:**  
Use a **Variational Quantum Circuit (VQC)** to classify data into two or more categories.

### **Dataset Options:**
- **[Iris Dataset](https://scikit-learn.org/stable/auto_examples/datasets/plot_iris_dataset.html)** (Flower classification)
- **[Wine Dataset](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_wine.html)** (Wine quality classification)
- **[Breast Cancer Dataset](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_breast_cancer.html)** (Cancer classification)

### **Steps:**
1. **Apply a Quantum Feature Map** to encode classical data into a quantum state.
2. **Train a Variational Quantum Classifier (VQC)** using Qiskit’s `NeuralNetworkClassifier`.
3. **Optimize circuit parameters** with a hybrid quantum-classical gradient descent method.
4. **Compare results with classical classifiers** (e.g., SVM, logistic regression).

### **IBM Q Execution Plan:**
- Use **low-depth quantum circuits** (≤10 qubits) for training.
- Train **on a simulator**, then test inference on IBM hardware.

🔗 **References:**
- [Qiskit Machine Learning - Variational Quantum Classifiers](https://qiskit.org/documentation/machine-learning/tutorials/03_variational_quantum_classifier.html)

---

## **2. Hybrid Quantum-Classical Classifier**
### **Objective:**  
Enhance a classical classifier with a quantum feature embedding for improved separability.

### **Dataset Options:**
- **[MNIST (Downsampled to 4x4)](http://yann.lecun.com/exdb/mnist/)** (Handwritten digits classification)
- **[Fashion-MNIST](https://github.com/zalandoresearch/fashion-mnist)** (Clothing classification)
- **[Text Classification Dataset](https://www.kaggle.com/datasets/rmisra/news-category-dataset)** (News topic classification)

### **Steps:**
1. **Apply a Quantum Feature Map** to extract quantum-encoded features.
2. **Train a classical classifier** (SVM, neural network) using quantum-enhanced features.
3. **Compare results to classical feature extraction techniques.**

### **IBM Q Execution Plan:**
- Use **hybrid training** where only feature extraction runs on quantum hardware.
- Limit **quantum circuit depth to optimize execution time.**

🔗 **References:**
- [Quantum Feature Maps](https://qiskit.org/textbook/ch-machine-learning/quantum-feature-maps.html)
- [Qiskit TorchConnector for Hybrid Training](https://qiskit.org/documentation/machine-learning/tutorials/05_torch_connector.html)

---

## **3. Quantum Classification with Kernel Methods**
### **Objective:**  
Use a **Quantum Kernel Estimator** to classify complex data in high-dimensional space.

### **Dataset Options:**
- **[Breast Cancer Dataset](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_breast_cancer.html)** (Binary classification)
- **[UCI Spam Dataset](https://archive.ics.uci.edu/ml/datasets/spambase)** (Spam detection)

### **Steps:**
1. **Train a Quantum Kernel Machine** to separate data in a quantum-enhanced feature space.
2. **Compare accuracy with classical kernel methods (RBF, polynomial kernels).**
3. **Analyze how quantum kernels scale with qubit count.**

### **IBM Q Execution Plan:**
- Use **a maximum of 12 qubits** for kernel calculations.
- Train on a simulator, then test **quantum kernel estimation on real hardware**.

🔗 **References:**
- [Quantum Kernel Methods in Qiskit](https://qiskit.org/documentation/machine-learning/tutorials/06_quantum_kernel.html)

---

## **4. Quantum-Enhanced Few-Shot Learning**
### **Objective:**  
Use Quantum Classification to improve learning with very limited labeled data.

### **Dataset Options:**
- **[Omniglot Dataset](https://github.com/brendenlake/omniglot)** (Handwritten character recognition)
- **[Few-Shot CIFAR-100](https://www.cs.toronto.edu/~kriz/cifar.html)** (Limited-label image classification)

### **Steps:**
1. **Use a Quantum Kernel Estimator** to classify with minimal training samples.
2. **Compare results against classical few-shot learning techniques.**
3. **Evaluate model performance as qubit count increases.**

### **IBM Q Execution Plan:**
- Use **a small dataset (few-shot setting)** to keep training time low.
- Limit circuits to **≤8 qubits for feasible execution**.

🔗 **References:**
- [Quantum Support Vector Machines](https://arxiv.org/abs/1804.11326)

---

## **Summary of Feasibility**
| **Project** | **Qubits Needed** | **Feasibility with 10-Minute IBMQ Access** | **Challenges & Mitigations** |
|------------|------------------|--------------------------------------|------------------------------|
| **Variational Quantum Classifier** | 6-10 | ✅ **Feasible** | Keep quantum circuit depth low. |
| **Hybrid Quantum-Classical Classifier** | 6-12 | ✅ **Feasible** | Use hybrid methods for efficiency. |
| **Quantum Kernel Methods** | 8-12 | ⚠️ **Feasible but Limited** | Limit kernel estimation circuit depth. |
| **Few-Shot Learning with QNNs** | 6-8 | ⚠️ **Partially Feasible** | Use very small datasets for fast inference. |

---
