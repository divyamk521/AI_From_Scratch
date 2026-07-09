# Definition Of Artificial Intelligence

## 1-Liner Definition

Artificial Intelligence (AI) is the simulation of human intelligence processes by machines, especially computer systems, enabling them to learn, reason, and self-correct.

---

## Short Technical Explanation

AI operates by executing algorithms across large datasets to recognize patterns, build probabilistic models, and make predictions or decisions without explicit task-specific programming.

Modern AI primarily relies on **Machine Learning (ML)** and **Deep Learning (DL)**, where artificial neural networks process inputs through multiple layers of nodes (neurons) to optimize a specific loss function using mathematical techniques such as **backpropagation** and **gradient descent**.

---

## Real-World Scenarios

### 1. E-commerce Recommendation Engines

Systems like **Amazon** or **Netflix** analyze past user behavior and matrix factorization to predict and suggest the next product or movie.

### 2. Autonomous Vehicles

Self-driving cars process real-time computer vision data from cameras and LiDAR to detect obstacles, predict pedestrian movement, and navigate routes safely.

---

## Code Snippet

The following example demonstrates a simple Artificial Intelligence model using **Linear Regression** from **scikit-learn**.

```python
from sklearn.linear_model import LinearRegression

# 1. Training Data: [Feature (e.g., Size)] -> [Target (e.g., Price)]
X = [[1000], [1500], [2000], [2500]]
y = [300000, 450000, 600000, 750000]

# 2. Initialize and train the AI model
model = LinearRegression()
model.fit(X, y)

# 3. Predict the price for a new house of 1800 sq ft
predicted_price = model.predict([[1800]])
print(f"Predicted Price: ${predicted_price[0]:.2f}")
```
