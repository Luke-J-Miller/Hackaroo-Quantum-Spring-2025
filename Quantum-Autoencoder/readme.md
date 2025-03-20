# Quantum Autoencoder (QAE) Hackathon Projects

Designed for students with **10 minutes of access** to IBM quantum computers (**max 127 qubits**).

---

## **1. Quantum Autoencoder for Data Compression**
### **Objective:**  
Use a quantum autoencoder (QAE) to compress images from a dataset, demonstrating quantum data compression.

### **Dataset Options:**
- **USPS (16x16 grayscale handwritten digits)**
- **Semeion (16x16 grayscale handwritten digits)**
- **Fashion-MNIST (28x28 grayscale, downsampled to 16x16 if necessary)**

### **Steps:**
1. **Amplitude Encoding**: Encode images into **6-8 qubits**.
2. **Compression**: Train a quantum autoencoder to **reduce qubits from 6 to 5 or 4**.
3. **Reconstruction**: Measure fidelity to assess compression quality.
4. **Analysis**:  
   - Discuss how compressing **64x28-bit data into 4 qubits** affects information retention.  
   - Compare quantum and classical autoencoders.

### **IBM Q Execution Plan:**
- Run **batch amplitude encoding** into 6-8 qubits.
- Train a **shallow** variational quantum circuit for compression.
- Measure outputs and reconstruct classically.

---

## **2. Quantum Autoencoder for Denoising**
### **Objective:**  
Extend the quantum autoencoder to remove noise from images and compare performance against classical models.

### **Dataset Options:**
- **USPS or Semeion with artificially added noise (Gaussian, salt & pepper)**
- **Fashion-MNIST (downsampled)**

### **Steps:**
1. **Introduce Noise**: Add noise to images.
2. **Train QAE**: Use quantum circuits to **reconstruct clean images**.
3. **Compare with Classical Methods**: Train a classical autoencoder and measure:
   - **Peak Signal-to-Noise Ratio (PSNR)**
   - **Structural Similarity Index (SSIM)**

### **IBM Q Execution Plan:**
- Train a **shallow QAE model** to filter noise.
- Use a **small subset of images** (to stay within execution limits).
- Output classical representations for final denoising.

---

## **3. Quantum Feature Extraction for Classical ML**
### **Objective:**  
Use quantum autoencoder embeddings as feature inputs for a classical machine learning model.

### **Dataset Options:**
- **USPS, Semeion, or Fashion-MNIST**

### **Steps:**
1. **Quantum Encoding**: Encode images into **6-10 qubits**.
2. **Quantum Feature Extraction**: Train a quantum autoencoder, extract latent space representations.
3. **Classical Classification**: Use an SVM or Random Forest to classify based on quantum-extracted features.
4. **Compare Accuracy**: Compare results to raw pixel-based classification.

### **IBM Q Execution Plan:**
- Run a **low-depth quantum encoder** to generate feature vectors.
- Measure qubit states and convert to classical features.
- Train a classical model using extracted quantum features.

---

## **4. Hybrid Quantum-Classical Autoencoder**
### **Objective:**  
Combine quantum encoding with classical decoding for an efficient hybrid QAE.

### **Dataset Options:**
- **USPS, Semeion, Fashion-MNIST**

### **Steps:**
1. **Quantum Encoding**: Encode images into 6-10 qubits.
2. **Train Hybrid Model**:
   - Use **quantum circuits** for encoding.
   - Use **classical neural networks** for decoding.
3. **Evaluate Performance**:
   - Compare hybrid QAE vs. fully classical autoencoders in terms of reconstruction fidelity.

### **IBM Q Execution Plan:**
- Use a **small, efficient quantum encoder** on IBMQ.
- Train a classical decoder to reconstruct images.

---

## **Summary of Feasibility**
| **Project** | **Qubits Needed** | **Feasibility with 10-Minute IBMQ Access** | **Challenges & Mitigations** |
|------------|------------------|--------------------------------------|------------------------------|
| **Quantum Autoencoder for Compression** | 6-8 | ✅ **Feasible** | Keep circuit depth low, batch process images. |
| **Quantum Autoencoder for Denoising** | 6-8 | ⚠️ **Feasible but Limited** | Train on a subset of images, use a hybrid approach. |
| **Quantum Feature Extraction for Classical ML** | 6-10 | ✅ **Feasible** | Reduce quantum circuit depth, use classical models for final classification. |
| **Hybrid Quantum-Classical Autoencoder** | 6-10 | ✅ **Feasible** | Offload classical processing to maintain efficiency. |

---
