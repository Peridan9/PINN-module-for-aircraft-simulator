# ✈️ Physics-Informed Neural Network (PINN) Module for Aircraft Simulator  

This repository contains the implementation of a **Physics-Informed Neural Network (PINN)** for predicting aircraft movement within a simulation environment. Developed as part of a final project at **Ben-Gurion University**, this work integrates physical principles into machine learning models to achieve high accuracy and computational efficiency in flight simulations.  

---

## 📘 Project Overview  

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
├── data/
│   └── flight_data.csv        # Simulated flight data from X-Plane 12.
├── models/
│   ├── base_lstm.py           # Baseline LSTM model implementation.
│   ├── sequence_lstm.py       # LSTM model with sequence-based predictions.
│   └── pinn.py                # Physics-Informed Neural Network model.
├── notebooks/
│   ├── data_analysis.ipynb    # Exploratory data analysis and preprocessing.
│   └── training_results.ipynb # Visualization of training outcomes.
├── results/
│   └── mse_comparison.png     # Comparison of MSE across models.
├── utils/
│   ├── data_preprocessing.py  # Data cleaning and normalization scripts.
│   └── physics_loss.py        # Implementation of physics-based loss functions.
├── requirements.txt           # Required Python libraries.
├── README.md                  # Project documentation.
└── main.py                    # Entry point for training and evaluation.
```

---

## 🚀 How to Run  

1. **Clone the repository**:  
   ```bash
   git clone https://github.com/Peridan9/PINN-module-for-aircraft-simulator.git
   cd PINN-module-for-aircraft-simulator
   ```  

2. **Install dependencies**:  
   ```bash
   pip install -r requirements.txt
   ```  

3. **Prepare the data**:  
   - Place your flight data in the `data/` directory.  
   - Ensure it follows the structure used in the provided dataset.  

4. **Train the model**:  
   ```bash
   python main.py --model pinn --epochs 50
   ```  

5. **Visualize results**:  
   - Open the `notebooks/training_results.ipynb` notebook to analyze the training and testing outcomes.  

---

## 🧪 Experiments  

### Experiment Goals  

1. Evaluate the baseline LSTM model's performance.  
2. Analyze the impact of adding physical loss functions.  
3. Test longer sequence lengths and dropout rates to improve generalization.  

### Key Results  

- **MSE Reduction**: PINN models outperformed traditional LSTM models with up to 50% lower error.  
- **Feature-Specific Performance**: Features like altitude and velocity showed the most significant improvements.  
- **Challenges**: Multi-feature prediction highlighted areas needing further refinement, particularly for features like roll and heading.  

---

## 📊 Results  

### Performance Comparison  

The chart below highlights the average normalized MSE for key features across models:  

![MSE Comparison](results/mse_comparison.png)  

- **Baseline LSTM**: Higher error rates due to lack of physical constraints.  
- **PINN Model**: Achieved the lowest MSE across all features.  

---

## 🌟 Future Work  

- Real-time implementation for live simulation and monitoring.  
- Exploration of additional features and architectures for improved scalability.  
- Enhanced data preprocessing to address noise and improve reliability.  
- Extension to handle various aircraft types and dynamic scenarios.  

---

## 📅 Project Details  

- **Institution**: Ben-Gurion University of the Negev  
- **Course**: Final Project in Software and Information Systems Engineering  
- **Team Members**:  
  - Daniel Peri  
  - Daniella Kapustyan  
  - Shay Milner  
- **Supervisor**: Prof. Mark Last  

---

Feel free to explore the repository and reach out with any questions or suggestions! 😊  
