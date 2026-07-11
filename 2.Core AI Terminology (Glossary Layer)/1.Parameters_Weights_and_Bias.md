# Parameters (Weights and Bias)

## 1-Liner Definition

Parameters are the configuration variables that an AI model learns from
training data to make predictions. They mainly consist of **Weights**
(which control the influence of inputs) and **Bias** (which shifts the
output).

------------------------------------------------------------------------

## Short Technical Explanation

In a neural network, each neuron computes a weighted sum of its inputs
and then adds a bias before passing the result to an activation
function.

### Mathematical Formula

\[ z = `\sum `{=tex}(x_i `\cdot `{=tex}w_i) + b \]

Where:

-   **(x_i)** = Input features
-   **(w_i)** = Weights
-   **(b)** = Bias
-   **(z)** = Weighted sum before activation

### Weights ((w))

Weights are coefficients multiplied with input features. They determine
how much influence each feature has on the prediction. Increasing or
decreasing a weight changes the importance of its corresponding input.

### Bias ((b))

Bias is a constant value added after the weighted sum. It shifts the
model's output, allowing the decision boundary to fit data more
accurately. Without bias, many models would be forced to pass through
the origin, limiting their flexibility.

### Training Process

During training, optimization algorithms such as **Gradient Descent**
automatically adjust the weights and bias to minimize the model's
prediction error (loss).

------------------------------------------------------------------------

## Real-World Scenarios

### Predicting Real Estate Prices

Suppose a model predicts house prices using:

-   Square footage
-   Distance to the nearest metro station

The **weights** determine how much each feature increases or decreases
the predicted price, while the **bias** represents the base value of a
house before considering these features.

### Smart Security Camera

A security camera may assign a high **weight** to pixel patterns
resembling a human face. The **bias** acts as a threshold, helping
prevent false detections under poor lighting conditions.

------------------------------------------------------------------------

## Code Snippet

``` python
# 1. Raw input features (e.g., [House Size Score, Location Rating Score])
inputs = [1.5, 2.0]

# 2. Model Parameters (Learned during training)
weights = [0.8, -0.4]
bias = 0.5

# 3. Neuron Calculation
weighted_sum = sum(x * w for x, w in zip(inputs, weights))
neuron_output = weighted_sum + bias

print(f"Inputs: {inputs}")
print(f"Weighted Sum: {weighted_sum}")
print(f"Final Prediction (with Bias): {neuron_output}")
```

### Expected Output

``` text
Inputs: [1.5, 2.0]
Weighted Sum: 0.4
Final Prediction (with Bias): 0.9
```
