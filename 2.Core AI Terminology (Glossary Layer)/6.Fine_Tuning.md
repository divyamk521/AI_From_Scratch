# Fine-Tuning

## 1-Liner Definition

**Fine-tuning** is the process of taking a pre-trained AI model with
general knowledge and training it further on a smaller, specialized
dataset so it performs better on a specific task or domain.

------------------------------------------------------------------------

## Short Technical Explanation

During **pre-training**, an AI model learns broad language patterns,
facts, and reasoning abilities from billions of tokens by adjusting its
weights.

During **fine-tuning**, the model starts from these learned weights
instead of random initialization. It is then trained on a
domain-specific dataset using a much lower learning rate.

Common fine-tuning approaches include:

-   **Supervised Fine-Tuning (SFT)** -- Trains the model using
    prompt-response pairs.
-   **LoRA (Low-Rank Adaptation)** -- Updates only a small number of
    parameters, making fine-tuning faster and more memory-efficient.

The goal is to adapt the model's behavior, formatting style,
terminology, or domain expertise without losing its general knowledge.

------------------------------------------------------------------------

## Real-World Scenarios

### Medical Diagnostic Assistant

A general LLM is fine-tuned on medical records and clinical notes so it
can generate responses using accurate medical terminology and healthcare
guidelines.

### Customer Support Agent

A company fine-tunes an open-source model (such as Llama) on historical
support tickets so the AI responds in the organization's preferred tone
and follows internal support policies.

------------------------------------------------------------------------

## Code Snippet

``` python
# Simulating a pre-trained model
class MockLLM:
    def __init__(self):
        self.weights = {
            "medical_query": "I am a helpful assistant. Take two aspirin."
        }

    def generate(self, prompt):
        return self.weights.get(prompt, "I don't understand.")

    # Fine-tuning updates the model's parameters
    def fine_tune(self, training_data, learning_rate=0.1):
        print("--- Starting Fine-Tuning Loop ---")
        for prompt, target_answer in training_data.items():
            self.weights[prompt] = target_answer
        print("Fine-tuning complete.\n")

# Pre-trained model
ai_model = MockLLM()
print("Pre-trained Output:")
print(ai_model.generate("medical_query"))

# Domain-specific dataset
medical_dataset = {
    "medical_query":
    "Based on clinical guidelines, please consult a cardiologist immediately."
}

# Fine-tune the model
ai_model.fine_tune(medical_dataset)

# Test after fine-tuning
print("Fine-Tuned Output:")
print(ai_model.generate("medical_query"))
```

### Expected Output

``` text
Pre-trained Output:
I am a helpful assistant. Take two aspirin.

--- Starting Fine-Tuning Loop ---
Fine-tuning complete.

Fine-Tuned Output:
Based on clinical guidelines, please consult a cardiologist immediately.
```
