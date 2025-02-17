# ✈️ Physics-Informed Neural Network (PINN) Module for Aircraft Simulator

This repository contains the implementation of a **Physics-Informed Neural Network (PINN)** for predicting aircraft movement within a simulation environment. Developed as part of a final project at **Ben-Gurion University**, this work integrates physical principles into machine learning models to achieve high accuracy and computational efficiency in flight simulations.

---

## 📚 Project Overview

Traditional simulation methods in aviation rely on computationally intensive physics-based models, which often lead to long processing times. This project addresses these challenges by leveraging **PINNs**, which embed physical laws directly into the neural network's training process.

Key contributions:

- Integration of physical loss functions to ensure realistic predictions.
- Reduction in **Mean Squared Error (MSE)** by 25%-50% compared to traditional models.
- Introduction of rolling predictions for real-time simulation.

---

## ✨ Features

- **Physics-Informed Learning**: Incorporates physical laws (e.g., Newton's laws of motion) into the loss function for improved prediction accuracy.
- **Multi-Feature Prediction**: Simultaneously predicts up to 13 aircraft movement features, including position, velocity, and orientation.
- **Rolling Predictions**: Supports real-time applications with continuous data streams.
- **Modular Design**: Easily adaptable for additional features and new datasets.

---

## 🛠️ Technologies

- **Programming Language**: Python
- **Libraries**:
  - PyTorch: Neural network framework.
  - NumPy & Pandas: Data preprocessing and analysis.
  - Matplotlib: Visualization of results.

---

## 📂 File Structure

```
PINN-module-for-aircraft-simulator/
├── data/                 # Directory containing training data
├── models/               # Directory containing trained models
├── Physics.ipynb         # PINN model implementation
├── PinnProject.ipynb     # Rolling prediction method implementation
├── README.md             # Project documentation
```

---

## 🚀 How to Run

1. **Clone the repository**:

   ```bash
   git clone https://github.com/Peridan9/PINN-module-for-aircraft-simulator.git
   cd PINN-module-for-aircraft-simulator
   ```

2. **Ensure dependencies are installed**:

   Install the required dependencies using the following command:

   ```bash
   pip install torch torchvision torchaudio numpy pandas matplotlib
   ```

   Additionally, ensure you have **PyTorch with CUDA** installed for GPU acceleration. Follow the installation guide at [PyTorch](https://pytorch.org/get-started/locally/).

3. **Run the preferred notebook**:

   - **Physics.ipynb**: For general PINN-based prediction.
   - **PinnProject.ipynb**: For real-time rolling prediction, where each step's prediction is based on the previous step's output.

   Open the desired notebook in Jupyter and follow the instructions to train and evaluate the model.

---

## 🧪 Experiments

### Experiment Goals

1. Evaluate the baseline model's performance.
2. Analyze the impact of adding physical loss functions.
3. Test longer sequence lengths and dropout rates to improve generalization.

### Key Results

- **MSE Reduction**: PINN models outperformed traditional models with up to 50% lower error.
- **Feature-Specific Performance**: Features like altitude and velocity showed the most significant improvements.
- **Challenges**: Multi-feature prediction highlighted areas needing further refinement, particularly for features like roll and heading.

---

## 📊 Results

### Performance Comparison

The chart below highlights the average normalized MSE for key features across models:

![MSE Comparison](results/mse_comparison.png)

- **Baseline Model**: Higher error rates due to lack of physical constraints.
- **PINN Model**: Achieved the lowest MSE across all features.

---

## 🌟 Future Work

- Real-time implementation for live simulation and monitoring.
- Exploration of additional features and architectures for improved scalability.
- Enhanced data preprocessing to address noise and improve reliability.
- Extension to handle various aircraft types and dynamic scenarios.

---

## 💡 Ideas for Improvement

I believe **PINN** could be the future of many real-time simulators, significantly reducing hardware costs associated with solving complex differential equations with numerous variables. 

Our model predicted aircraft movement with medium accuracy, but implementing physical equations into the loss function improved accuracy by up to **50%**. This is remarkable considering the model predicts **13 features simultaneously**! Imagine breaking each equation into smaller, dedicated models—this could further enhance accuracy and efficiency.

We also demonstrated the rolling prediction mechanism because the end goal is to integrate the model into a physics engine within a simulator. In such cases, each next-step prediction is based on previous ones, making real-time accuracy crucial.

---

## 📄 Related Articles

[**Link to article (to be added)**]

---

## 🗓 Project Details

- **Institution**: Ben-Gurion University of the Negev
- **Course**: Final Project in Software and Information Systems Engineering
- **Team Members**:
  - [Daniel Peri](https://github.com/Peridan9)
  - Daniella Kapustyan
  - Shay Milner
- **Supervisor**: Prof. Mark Last

---

Feel free to explore the repository and reach out with any questions or suggestions! 😊

More about this project: [GitHub Repository](https://github.com/Peridan9/PINN-module-for-aircraft-simulator/tree/main?tab=readme-ov-file)


