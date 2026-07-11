# Training vs Inference

## 1-Liner Definition

**Training** is the compute-intensive process where an AI model learns
patterns from data by updating its internal parameters (weights and
biases). **Inference** is the phase where the trained model uses those
learned parameters to make predictions on new, unseen data.

------------------------------------------------------------------------

## Short Technical Explanation

### Training (Learning Phase)

Training is a two-way computational process:

1.  Forward Propagation
2.  Loss Calculation
3.  Backward Propagation
4.  Optimization using algorithms such as Gradient Descent

During training, weights and biases are repeatedly updated to minimize
prediction error. This process usually requires GPUs or TPUs and can
take hours, days, or weeks.

### Inference (Prediction Phase)

Inference is a one-way forward pass.

-   The learned weights remain frozen.
-   New data is processed.
-   The model generates predictions without updating its parameters.

Inference is significantly faster than training and usually completes
within milliseconds.

------------------------------------------------------------------------

## Real-World Scenarios

### Autonomous Driving

A self-driving vehicle is trained on massive driving datasets. Once
deployed, it performs inference in real time to detect pedestrians,
vehicles, and traffic signs.

### Large Language Models (LLMs)

AI companies spend extensive computational resources training foundation
models. When a user submits a prompt, the deployed model performs
inference to generate the response.

------------------------------------------------------------------------

## Code Snippet

``` python
from sklearn.linear_model import LinearRegression

# -------- TRAINING --------
X_train = [[1], [2], [4], [8]]
y_train = [10, 20, 40, 80]

model = LinearRegression()
model.fit(X_train, y_train)

print("Training complete.")
print(model.coef_[0])
print(model.intercept_)

# -------- INFERENCE --------
new_student_hours = [[6]]
predicted_score = model.predict(new_student_hours)

print(predicted_score[0])
```

### Expected Output

``` text
Training complete.

Learned Weight: ...

Learned Bias: ...

Prediction for 6 study hours: ~60
```
