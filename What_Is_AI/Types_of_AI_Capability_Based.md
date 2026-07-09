# Types of AI (Capability-Based)

## A. Narrow AI (ANI)

### 1-Liner Definition

Narrow AI (Artificial Narrow Intelligence) is an AI system designed,
trained, and optimized to excel at one specific task or a limited range
of tasks.

### Short Technical Explanation

ANI operates within a highly confined scope. It uses specialized
algorithms such as neural networks, decision trees, or statistical
models trained on specific datasets. It cannot transfer knowledge
between domains. Nearly all AI systems in use today are examples of
Narrow AI.

### Real-World Scenarios

-   **Language Translation:** Google Translate translates between
    languages but cannot perform unrelated tasks like driving a car.
-   **Medical Image Analysis:** AI models detect tumors in X-rays but
    cannot understand medicine beyond their training domain.

### Code Snippet

``` python
# Narrow AI: Optimized for one specific task
def narrow_sentiment_analyzer(text):
    positive_words = ["great", "clean", "fast", "efficient"]
    if any(word in text.lower() for word in positive_words):
        return "Positive Sentiment"
    return "Neutral/Negative Sentiment"

print(narrow_sentiment_analyzer("The backend code is very clean!"))
print(narrow_sentiment_analyzer("What is 5 + 5?"))  # Out of scope
```

------------------------------------------------------------------------

## B. General AI (AGI)

### 1-Liner Definition

General AI (Artificial General Intelligence) is a theoretical AI capable
of understanding, learning, and performing any intellectual task that a
human can.

### Short Technical Explanation

AGI would demonstrate cross-domain learning, common-sense reasoning,
abstract thinking, and knowledge transfer across different fields. A
single architecture could continuously acquire new skills without
requiring separate task-specific models.

### Real-World Scenarios

-   **Universal Assistant:** A robot capable of cooking, coding,
    reasoning, and learning unfamiliar tasks independently.
-   **Autonomous Scientific Researcher:** An AI capable of reading
    research, generating hypotheses, and conducting experiments.

### Code Snippet

``` python
# Conceptual AGI
class ConceptualAGI:
    def __init__(self):
        self.skills = {}

    def learn_new_skill(self, skill_name, logic_function):
        self.skills[skill_name] = logic_function
        print(self.skills[skill_name]("Learning complete!"))

agi = ConceptualAGI()
agi.learn_new_skill("cook_pasta", lambda msg: f"Pasta Status: {msg} Parsing steps...")
agi.learn_new_skill("fix_bug", lambda msg: f"Code Status: {msg} Compiling fixes...")
```

------------------------------------------------------------------------

## C. Super AI (ASI)

### 1-Liner Definition

Super AI (Artificial Superintelligence) is a hypothetical AI that
surpasses human intelligence across every domain, including science,
creativity, reasoning, and social intelligence.

### Short Technical Explanation

ASI is theorized to emerge through recursive self-improvement after AGI.
By repeatedly redesigning its own software and hardware, it could
improve exponentially, eventually exceeding human cognitive capabilities
by a vast margin.

### Real-World Scenarios

-   **Global Optimization:** Managing energy, logistics, healthcare, and
    climate systems with near-perfect efficiency.
-   **Scientific Breakthroughs:** Discovering revolutionary technologies
    and medical treatments beyond current human understanding.

### Code Snippet

``` python
# Conceptual ASI
class ConceptualASI:
    def __init__(self, intelligence_level):
        self.intelligence = intelligence_level

    def trigger_self_improvement(self):
        while self.intelligence < 1000000:
            self.intelligence *= 10
            print(f"Intelligence Level: {self.intelligence}")
        return "Human comprehension limit exceeded."

asi = ConceptualASI(intelligence_level=100)
print(asi.trigger_self_improvement())
```
