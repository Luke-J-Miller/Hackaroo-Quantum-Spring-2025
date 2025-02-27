# UMKC Research-A-Thon, Spring 2025, Quantum Track

This is still being developed, more resources and information will be added in the current week.
This event is our first quantum hackathon. We do not expect participants to be experts in quantum programming. The examples in this repository can help participants learn the basics.

## Event Overview
- **Submission Requirements**:
  1. A well-organized GitHub repository. This includes a readme describing your project. Avoid large amounts of 'helper' files. The function should be evident and understandable from your main notebook.
  2. A 5-minute video explaining your approach and results. Some judges may not be able to attend in person, they will judge you on this.
  3. A poster summarizing your method and findings. You will stand next to your poster and explain your project. You should rehearse a 45 second 'elevator pitch'. What is your project, how does it work, why your methods, what impact could it have?

## Grading Rubric
| Task | Points | Description|
|------|--------|-------------|
|1. Code Quality and Comments	| 20	| Clear, working code. Each function or section should have comments.|
|2. Classical vs. Quantum Comparison	| 20	| Clear comparison of the classical approach with the quantum approach.|
|3. Explanation of Quantum Methods	| 20	| Solid understanding of the quantum algorithms or concepts used.|
|4. Potential for Quantum Advantage	| 20	| Explanation of how the quantum method might surpass classical methods as hardware improves.|
|5. Future Impact	| 20	| Discussion of how this algorithm could change problem-solving approaches if quantum hardware grows more capable.|

Below is a set of project ideas for a quantum‑enhanced AI track using **Qiskit**. Each project is described at a high level, with suggestions on how to adapt it to different datasets and how to emphasize the potential quantum advantage. These projects focus on **machine learning / AI** use cases, but they can be flexibly extended or simplified, depending on the participants’ skill levels.

---

## 1. Quantum-Enhanced Classification with Variational Quantum Circuits

**Concept**  
- Build a **variational quantum circuit (VQC)** classifier (using `qiskit.machine_learning` or custom parameterized circuits) to distinguish between two or more classes in a dataset.  
- Train the circuit’s parameters with a hybrid quantum-classical loop (using gradient descent or another optimizer in Qiskit).  

**Dataset Adaptation**  
- Start with small/low-dimensional datasets (e.g., **Iris**, **Wine**, or **Breast Cancer** from scikit-learn).  
- For a more advanced project, students can select a custom dataset (e.g., a subset of **MNIST** images or a text classification dataset).  
- Emphasize how quantum feature maps can encode data into the quantum circuit.

**Potential Quantum Advantage**  
- Discuss how **quantum feature spaces** might offer better class separability.  
- Show how the circuit scales with qubit number vs. classical approaches. Even if near-term quantum hardware is limited, highlight **theoretical** advantage or **hybrid** approaches that reduce parameter count.

---

## 2. Quantum Kernel Methods (Quantum SVM)

**Concept**  
- Implement a **quantum kernel** that maps classical data into a higher-dimensional Hilbert space.  
- Use a Support Vector Machine (SVM) algorithm on top of the quantum kernel.  
- Qiskit’s `QuantumKernel` class provides functionality for designing custom quantum feature maps.

**Dataset Adaptation**  
- Adapt the same small tabular datasets (Iris, Wine, etc.) or pick a domain-specific dataset (e.g., classifying tweets as positive/negative, or time-series classification data).  
- Students can experiment with different feature maps (e.g., Pauli feature maps or custom ansätze).

**Potential Quantum Advantage**  
- The idea is that a properly chosen **quantum feature map** can yield more powerful decision boundaries than a purely classical kernel.  
- Students can analyze performance for different kernel parameters (e.g., depth of the circuit).

---

## 3. Hybrid Quantum-Classical Neural Networks

**Concept**  
- Combine a **small quantum circuit** (with parameterized gates) as part of a **larger classical neural network** pipeline.  
- For instance, use PyTorch or TensorFlow to build a network, but replace one (or more) dense layers with a **quantum layer** (via Qiskit’s Torch Connector or a custom interface).

**Dataset Adaptation**  
- This can be demonstrated on standard image datasets (like a subset of **MNIST**—e.g., digits 0 and 1 only for binary classification).  
- Alternatively, for tabular or time-series data, a quantum layer can act as a “feature extraction” stage within an end-to-end model.

**Potential Quantum Advantage**  
- The network can tap into quantum effects while retaining classical scalability.  
- Show how even a few qubits in a quantum layer might reduce the total number of classical trainable parameters.

---

## 4. Quantum Autoencoder for Dimensionality Reduction

**Concept**  
- A **quantum autoencoder** is designed to compress quantum states or classical data mapped to quantum states.  
- Students can adapt it to reduce data dimensionality and attempt to reconstruct the original data from the compressed state.

**Dataset Adaptation**  
- Focus on small images (e.g., 8×8 digit images from scikit-learn’s “digits” dataset) or low-dimensional tabular data.  
- Encode each data point into the amplitudes of a quantum state (may require normalization).

**Potential Quantum Advantage**  
- Demonstrates how a quantum circuit might compress data more efficiently or learn compression strategies not easily accessible classically.  
- Great for teams to discuss state fidelity as a metric vs. classical reconstruction error.

---

## 5. Quantum Generative Adversarial Network (QGAN)

**Concept**  
- A **QGAN** has two components: a classical or quantum Discriminator and a quantum Generator, or vice versa.  
- Use Qiskit’s `qiskit_machine_learning.algorithms.generative` module or build from scratch to show how quantum sampling might help in data generation.

**Dataset Adaptation**  
- Start with very low-dimensional data (e.g., 1D or 2D distributions, simple statistical distributions like Gaussian, etc.).  
- Scale up to something like small tabular data with 2–4 features to keep quantum state size manageable.

**Potential Quantum Advantage**  
- Quantum systems can **sample from complex distributions** that might be harder to model classically.  
- Even if the advantage is small with near-term hardware, this project can spark discussion on potential future benefits in large-scale quantum sampling.

---

## 6. Quantum K-Means Clustering

**Concept**  
- Implement a variation of **K-Means** (or other clustering algorithms) that uses a quantum distance estimator or quantum kernel.  
- For example, you can estimate the distance between data points in a quantum feature space, then proceed with a standard K-Means update.

**Dataset Adaptation**  
- Works well on unlabeled datasets.  
- Could use an open dataset from Kaggle (e.g., customer segmentation) or a small sensor dataset (e.g., IoT sensor readings) to group unlabeled samples.

**Potential Quantum Advantage**  
- Leverage quantum distance metrics that might better capture relationships between data points in certain feature embeddings.  
- Encourages participants to compare classical vs. quantum distances.

---

## 7. Quantum-Assisted Reinforcement Learning

**Concept**  
- A more advanced project: incorporate a **quantum policy network** or a **quantum Q-network** for a simple RL task.  
- For instance, solve a basic problem like **CartPole** or **FrozenLake** from OpenAI Gym, but replace the policy or value function with a variational quantum circuit.

**Dataset Adaptation**  
- RL is not strictly a “dataset” approach, but logs of state-action-reward transitions can be treated as a dataset for offline training.  
- Can also adapt simpler tasks if time is short.

**Potential Quantum Advantage**  
- Investigate how quantum states might capture state representations or lead to faster training with fewer parameters.  
- This can spark creativity around exploration strategies (though success will likely be conceptual at hackathon scales).

---

## 8. Quantum Feature Selection with QAOA or VQE

**Concept**  
- Use the **Quantum Approximate Optimization Algorithm (QAOA)** or **Variational Quantum Eigensolver (VQE)** approach to tackle a small feature selection or optimization problem in ML pipelines.  
- Frame feature selection as a combinatorial optimization problem (e.g., limited number of features allowed, maximize some classification accuracy measure).

**Dataset Adaptation**  
- Any dataset with multiple features (tabular data works best). Students can set a constraint (e.g., pick 3 out of 10 features) to optimize classification accuracy on a small hold-out set.

**Potential Quantum Advantage**  
- QAOA might produce good approximate solutions for combinatorial problems.  
- Students can compare the QAOA approach to a classical solver (like a standard heuristic or a classical approximate method).

---

## General Tips for Your Hackathon GitHub

1. **Starter Notebooks**: Provide a few Jupyter notebooks that show minimal working examples of these ideas (e.g., a VQC notebook, a QKernel notebook, etc.).  
2. **Qiskit Installation & Setup**: Include instructions on installing Qiskit and (optionally) how to sign up for IBM Quantum’s cloud backends.  
3. **Data Handling & Preprocessing**: Show how to load datasets (from `sklearn.datasets` or CSV files) and how to **normalize** or **reduce dimensionality** before encoding into quantum states.  
4. **Comparison to Classical Baselines**: Encourage students to run a quick classical version (e.g., classical SVM, classical neural net) to compare performance and discuss differences.  
5. **Focus on Explanation**: Since you emphasized that grading will consider the **explanation of the project and potential quantum advantage**, prompt students to discuss:
   - Why a quantum approach might (in theory) outperform classical methods in certain scenarios.  
   - The constraints of today’s NISQ (Noisy Intermediate-Scale Quantum) hardware and how that impacts results.  

With these starter ideas, participants can choose what resonates with them (classification, clustering, generative modeling, optimization, etc.) and adapt to any dataset of interest. By providing clear examples and a structured GitHub repo, you’ll lower the barrier to entry for first-time quantum hackers and create a fun, educational environment. Good luck with your quantum track!


Go [here](https://docs.quantum.ibm.com/migration-guides/qiskit-runtime-examples) to learn how to run on quantum hardware.
