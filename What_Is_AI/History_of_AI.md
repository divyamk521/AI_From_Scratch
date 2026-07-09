# History of AI

## A. Symbolic AI / Rule-Based Systems

### 1-Liner Definition

Symbolic AI is an early approach to AI that relies on hardcoded rules
and logical **IF--THEN** statements written by humans to process symbols
and make decisions.

### Short Technical Explanation

Instead of learning from data, Symbolic AI represents real-world facts
as tokens or words (symbols). Engineers explicitly program every logical
rule into the system using formal logic. If the input matches a
predefined rule, the system executes the corresponding output;
otherwise, it fails because it cannot generalize or learn on its own.

### Real-World Scenarios

-   **Classic Chess Video Games:** Early computer chess programs used
    hardcoded rules to determine the next move.
-   **Basic Tax Calculators:** Software applies government tax rules to
    calculate refunds based on user inputs.

### Code Snippet

``` python
# Rule-Based System: Everything must be hardcoded by a human programmer
def rule_based_loan_approval(credit_score, income):
    if credit_score > 700 and income > 50000:
        return "Approved"
    elif credit_score <= 700 and income > 100000:
        return "Approved with higher interest"
    else:
        return "Rejected"

print(rule_based_loan_approval(720, 60000))  # Output: Approved
```

------------------------------------------------------------------------

## B. Expert Systems

### 1-Liner Definition

Expert Systems are specialized rule-based programs designed to mimic the
decision-making ability of a human expert in a very specific domain.

### Short Technical Explanation

An Expert System consists of: - **Knowledge Base:** A repository of
IF--THEN rules collected from domain experts. - **Inference Engine:**
Applies those rules to user-provided facts to derive conclusions.

They represented the commercial peak of Symbolic AI during the 1980s.

### Real-World Scenarios

-   **MYCIN (Medical Diagnosis):** Diagnosed blood infections and
    recommended antibiotics.
-   **Oil Exploration:** Estimated drilling success using geological
    rules.

### Code Snippet

``` python
knowledge_base = {
    ("fever", "cough"): "Common Flu",
    ("fever", "rash"): "Measles",
    ("no_fever", "cough"): "Mild Cold"
}

def inference_engine(symptoms):
    return knowledge_base.get(symptoms, "Unknown Condition - Consult a doctor")

patient_symptoms = ("fever", "cough")
print("Diagnosis:", inference_engine(patient_symptoms))
```

------------------------------------------------------------------------

## C. AI Winters (Causes)

### 1-Liner Definition

AI Winters were periods when funding and research declined because AI
systems failed to meet overly optimistic expectations.

### Short Technical Explanation

Two major AI Winters occurred in the **mid-1970s** and **late-1980s**
due to: - Overhyped promises - Limited computing power - Insufficient
memory - Slow processors - Combinatorial explosion of rule-based systems

### Real-World Scenarios

-   Government funding cuts for machine translation.
-   Collapse of the Lisp Machine industry.

### Code Snippet

``` python
def funding_lifecycle(ai_performance, hype_level):
    if hype_level > 90 and ai_performance < 30:
        return "Funding Withdrawn: Entering AI Winter ❄️"
    return "Funding Active 👍"

print(funding_lifecycle(ai_performance=20, hype_level=95))
```

------------------------------------------------------------------------

## D. Statistical / Machine Learning Era

### 1-Liner Definition

Machine Learning shifted AI from manually written rules to systems that
automatically learn patterns from data.

### Short Technical Explanation

Algorithms learn statistical relationships between **features (X)** and
**labels (y)** by minimizing prediction error. Once trained, they can
predict outcomes for unseen data.

### Real-World Scenarios

-   Credit card fraud detection
-   Housing price prediction

### Code Snippet

``` python
import numpy as np
from sklearn.linear_model import LinearRegression

X = np.array([[800], [1200], [1800], [2400]])
y = np.array([160000, 240000, 360000, 480000])

model = LinearRegression().fit(X, y)

print(model.predict([[1500]])[0])
```

------------------------------------------------------------------------

## E. Deep Learning Era

### 1-Liner Definition

Deep Learning is a subset of Machine Learning that uses multi-layer
artificial neural networks to automatically learn complex patterns from
raw data.

### Short Technical Explanation

Neural networks learn hierarchical features: - Early layers detect
edges - Middle layers identify shapes - Deep layers recognize objects

Training relies heavily on GPUs and **backpropagation**.

### Real-World Scenarios

-   Facial recognition
-   Voice assistants

### Code Snippet

``` python
import numpy as np

inputs = np.array([0.5, 0.8])

weights_layer_1 = np.array([[0.2, 0.4], [0.6, 0.1]])
weights_layer_2 = np.array([0.3, 0.7])

hidden_output = np.dot(inputs, weights_layer_1)
final_prediction = np.dot(hidden_output, weights_layer_2)

print(final_prediction)
```

------------------------------------------------------------------------

## F. Generative AI / LLM Era

### 1-Liner Definition

The Generative AI and Large Language Model (LLM) era focuses on models
trained on internet-scale data to generate human-like text, code, and
reasoning.

### Short Technical Explanation

Modern LLMs use the **Transformer architecture** and **Self-Attention**
to process all words in a sentence simultaneously. They learn by
predicting the next token from massive datasets, enabling coding,
reasoning, and conversational capabilities.

### Real-World Scenarios

-   AI coding assistants
-   Automated customer support agents

### Code Snippet

``` python
context = "The software engineer wrote a clean piece of"

next_token_probabilities = {
    "code": 0.85,
    "paper": 0.10,
    "banana": 0.05
}

best_next_word = max(next_token_probabilities, key=next_token_probabilities.get)

print(f"LLM Generation: {context} [{best_next_word}]")
```
