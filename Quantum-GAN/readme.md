# Quantum Generative Adversarial Networks (qGAN) Hackathon Projects

Designed for students with **10 minutes of access** to IBM quantum computers (**max 127 qubits**).

---

## **1. Quantum GAN for Learning Probability Distributions**
### **Objective:**  
Use a Quantum GAN (qGAN) to learn and generate probability distributions from a dataset.

### **Dataset Options:**
- **[Gaussian Mixture Model Data](https://scikit-learn.org/stable/modules/generated/sklearn.mixture.GaussianMixture.html)** (Synthetic distribution modeling)
- **[Multivariate Normal Distribution](https://numpy.org/doc/stable/reference/random/generated/numpy.random.multivariate_normal.html)** (Financial modeling and risk estimation)

### **Steps:**
1. **Define a Quantum Generator** using a parameterized quantum circuit.
2. **Use a classical discriminator** trained with PyTorch to differentiate real vs. generated distributions.
3. **Train using adversarial loss functions.**
4. **Compare generated probability distributions with actual distributions.**

### **IBM Q Execution Plan:**
- Use **a low-depth quantum circuit (≤10 qubits)** to represent probability distributions.
- Train on a simulator, then test the trained generator on IBMQ.

🔗 **References:**
- [Quantum GANs in Qiskit](https://qiskit.org/documentation/machine-learning/tutorials/09_qgans_for_loading_random_distributions.html)
- [Original qGAN Paper (Zoufal et al.)](https://arxiv.org/abs/1904.00043)

---

## **2. Hybrid Quantum-Classical GAN for Image Generation**
### **Objective:**  
Combine a quantum generator with a classical convolutional discriminator for generating simple images.

### **Dataset Options:**
- **[Fashion-MNIST (Downsampled to 4x4)](https://github.com/zalandoresearch/fashion-mnist)** (Clothing image generation)
- **[Omniglot](https://github.com/brendenlake/omniglot)** (Handwritten character generation)

### **Steps:**
1. **Apply quantum feature maps** to encode images as qubit states.
2. **Train a quantum generator** with a classical convolutional discriminator.
3. **Evaluate generated images for realism and diversity.**

### **IBM Q Execution Plan:**
- Train **only the generator** on IBMQ, keeping the discriminator classical.
- Limit **quantum circuit depth to ensure fast execution.**

🔗 **References:**
- [Qiskit Hybrid GAN Tutorial](https://qiskit.org/documentation/machine-learning/tutorials/09_qgans_for_loading_random_distributions.html)

---

## **3. Quantum GAN for Financial Modeling**
### **Objective:**  
Use qGANs to model financial data distributions for risk assessment and derivative pricing.

### **Dataset Options:**
- **[S&P 500 Stock Prices](https://www.kaggle.com/datasets/camnugent/sandp500)** (Market trend simulation)
- **[Option Pricing Dataset](https://qiskit.org/documentation/finance/tutorials/10_qgan_option_pricing.html)** (Financial derivative modeling)

### **Steps:**
1. **Train a qGAN on historical market data.**
2. **Use the trained generator to simulate new market scenarios.**
3. **Compare qGAN outputs with classical Monte Carlo simulations.**

### **IBM Q Execution Plan:**
- Use **a quantum generator with ≤12 qubits** to model stock return distributions.
- Train on a **simulator** and deploy on IBMQ for inference.

🔗 **References:**
- [Option Pricing with qGANs](https://qiskit-community.github.io/qiskit-finance/tutorials/10_qgan_option_pricing.html)

---

## **4. Quantum GAN for Medical Data Generation**
### **Objective:**  
Use qGANs to generate synthetic medical data for privacy-preserving machine learning applications.

### **Dataset Options:**
- **[COVID-19 Chest X-ray Dataset](https://www.kaggle.com/datasets/tawsifurrahman/covid19-radiography-database)** (Medical imaging synthesis)
- **[UCI Diabetes Dataset](https://www.kaggle.com/datasets/mathchi/diabetes-data-set)** (Patient data generation)

### **Steps:**
1. **Train a qGAN to generate synthetic medical data.**
2. **Compare generated data with real medical samples.**
3. **Evaluate potential applications for privacy-preserving AI.**

### **IBM Q Execution Plan:**
- Train **a small quantum generator (≤10 qubits)** on patient record distributions.
- Use IBMQ to **generate synthetic medical samples.**

🔗 **References:**
- [Quantum GANs for Healthcare](https://arxiv.org/abs/2006.05436)

---

## **Summary of Feasibility**
| **Project** | **Qubits Needed** | **Feasibility with 10-Minute IBMQ Access** | **Challenges & Mitigations** |
|------------|------------------|--------------------------------------|------------------------------|
| **Quantum GAN for Probability Distributions** | 6-10 | ✅ **Feasible** | Keep generator circuits shallow. |
| **Hybrid Quantum-Classical GAN for Image Generation** | 6-12 | ⚠️ **Partially Feasible** | Offload the discriminator to classical computation. |
| **Quantum GAN for Financial Modeling** | 8-12 | ⚠️ **Feasible but Limited** | Optimize training with batch-based execution. |
| **Quantum GAN for Medical Data Generation** | 6-10 | ✅ **Feasible** | Use small datasets to keep execution times low. |

---


