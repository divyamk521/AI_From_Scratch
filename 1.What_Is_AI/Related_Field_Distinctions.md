# Related Field Distinctions

## A. AI vs. Machine Learning

### 1-Liner Definition

Artificial Intelligence (AI) is the broad vision of creating intelligent
machines, whereas Machine Learning (ML) is a subset of AI that enables
systems to learn from data without explicit programming.

### Short Technical Explanation

AI includes rule-based systems, search algorithms, expert systems, and
ML. Machine Learning uses statistical algorithms to learn patterns from
training data by minimizing a loss function and then making predictions
on unseen data.

### Real-World Scenarios

-   **AI (Rule-Based):** Tax software using hardcoded regulations.
-   **ML:** Audit-risk prediction based on historical tax return data.

### Code Snippet

``` python
def ai_rule(temp):
    return "Hot" if temp > 30 else "Cold"

from sklearn.linear_model import LogisticRegression

X, y = [[15], [22], [32], [40]], [0, 0, 1, 1]
ml_model = LogisticRegression().fit(X, y)

print("AI Rule:", ai_rule(35))
print("ML Model Guess:", ml_model.predict([[35]])[0])
```

------------------------------------------------------------------------

## B. AI vs. Data Science

### 1-Liner Definition

AI builds intelligent systems that act autonomously, while Data Science
extracts insights from data to support business decisions.

### Short Technical Explanation

AI focuses on automation, reasoning, and content generation. Data
Science focuses on data collection, cleaning, analysis, visualization,
predictive modeling, and communicating insights.

### Real-World Scenarios

-   AI-powered customer support chatbot.
-   Customer churn analysis dashboard.

### Code Snippet

``` python
import numpy as np

customer_spending = [120, 450, 80, 230, 600, 15]
print(np.mean(customer_spending))

def ai_discount_agent(spend):
    return "Send 20% Coupon" if spend < 100 else "Send Thank You Note"

print(ai_discount_agent(15))
```

------------------------------------------------------------------------

## C. Machine Learning vs. Deep Learning

### 1-Liner Definition

Machine Learning usually relies on manually engineered features, whereas
Deep Learning automatically learns features from raw data.

### Short Technical Explanation

Traditional ML requires structured inputs prepared by engineers. Deep
Learning uses multi-layer neural networks to automatically extract
increasingly complex features during training.

### Real-World Scenarios

-   ML for house price prediction.
-   Deep Learning for image-based damage detection.

### Code Snippet

``` python
def traditional_ml_predict(features):
    sq_ft, rooms = features
    return (sq_ft * 200) + (rooms * 10000)

import numpy as np

raw_image_pixels = np.array([0.1, 0.9, 0.4, 0.7])
hidden_weights = np.array([
    [0.5, 0.2],
    [0.1, 0.8],
    [0.9, 0.3],
    [0.2, 0.6]
])

extracted_features = np.dot(raw_image_pixels, hidden_weights)
print(extracted_features)
```

------------------------------------------------------------------------

## D. Deep Learning vs. Generative AI

### 1-Liner Definition

Deep Learning provides the neural network technology for prediction and
recognition, while Generative AI specializes in creating entirely new
content.

### Short Technical Explanation

Many deep learning models are discriminative, classifying inputs into
categories. Generative AI uses architectures such as Transformers and
Diffusion Models to generate new text, code, images, audio, and video.

### Real-World Scenarios

-   Defect classification in manufacturing.
-   AI code generation from prompts.

### Code Snippet

``` python
def dl_classifier(text):
    return "Category: Spam" if "buy now" in text.lower() else "Category: Ham"

def gen_ai_writer(prompt):
    return f"{prompt} once upon a time in a secure cloud database..."

print(dl_classifier("Click here to buy now!"))
print(gen_ai_writer("Write a story about a backend engineer:"))
```

------------------------------------------------------------------------

## E. AI Engineer vs. ML Engineer vs. AI Researcher vs. Data Scientist

### 1-Liner Definition

AI Researchers invent models, ML Engineers train and deploy them, AI
Engineers build applications using them, and Data Scientists analyze
data for business insights.

### Short Technical Explanation

-   **AI Researcher:** Develops new architectures and algorithms.
-   **ML Engineer:** Builds training pipelines, optimizes models, and
    deploys them.
-   **AI Engineer:** Integrates AI models into software products using
    APIs, RAG, agents, and frameworks.
-   **Data Scientist:** Performs analytics, visualization,
    experimentation, and business reporting.

### Real-World Scenarios

-   AI Researcher publishes a novel neural network architecture.
-   ML Engineer trains and serves the model.
-   AI Engineer builds a production RAG application.
-   Data Scientist creates executive dashboards from usage analytics.

### Code Snippet

``` python
def custom_attention_layer(query, key):
    return (query * key) / 1.414

def train_and_export_pipeline(data):
    return "Optimized Model Binary (.onnx)"

def ai_agent_workflow(user_query, vector_db_client, llm_api):
    context = vector_db_client.search(user_query)
    return llm_api.generate(prompt=user_query, context=context)

def analyze_system_metrics(dataframe):
    retention_rate = dataframe[dataframe["user_satisfied"] == True].count()
    return f"Business Metric: {retention_rate}"
```
