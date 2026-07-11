# Context Window

## 1-Liner Definition

A **context window** is the maximum number of text tokens (including
both the input prompt and generated output) that a Large Language Model
(LLM) can process and remember at one time during a conversation.

------------------------------------------------------------------------

## Short Technical Explanation

The size of a context window is determined during the model's training.
Modern LLMs use the **Transformer** architecture with a
**Self-Attention** mechanism, where every token is compared with every
other token in the current context.

In traditional Transformer architectures, the computational complexity
grows quadratically with sequence length:

\[ O(N\^2) \]

where **N** is the number of tokens.

If a conversation exceeds the model's context window, the oldest tokens
are removed from the active memory. As a result, the model can no longer
attend to or reference that earlier information.

------------------------------------------------------------------------

## Real-World Scenarios

### Debugging Large Codebases

When analyzing a large backend project with multiple files and API
routes, a larger context window allows the model to understand
relationships across the entire codebase without forgetting earlier
functions.

### Long Document Summarization

Summarizing lengthy documents such as financial reports, legal
contracts, or research papers requires a large context window (for
example, **128K tokens**) so the model can process the entire document
in a single pass.

------------------------------------------------------------------------

## Code Snippet

``` python
class ModelContextWindow:
    def __init__(self, max_tokens):
        self.max_tokens = max_tokens
        self.active_buffer = []

    def add_tokens(self, new_tokens):
        # Add new text tokens
        self.active_buffer.extend(new_tokens)

        # Remove oldest tokens if context window is exceeded
        while len(self.active_buffer) > self.max_tokens:
            dropped = self.active_buffer.pop(0)
            print(f"⚠️ Context window full! Dropped token: '{dropped}'")

    def get_active_memory(self):
        return " ".join(self.active_buffer)

# Initialize a small context window
chat_session = ModelContextWindow(max_tokens=5)

# Initial conversation
chat_session.add_tokens(["user", "wants", "to", "build", "a"])
print("Active Context:", chat_session.get_active_memory(), "\n")

# Add more tokens
chat_session.add_tokens(["modular", "backend", "application"])
print("Final Active Context:", chat_session.get_active_memory())
```

### Expected Output

``` text
Active Context: user wants to build a

⚠️ Context window full! Dropped token: 'user'
⚠️ Context window full! Dropped token: 'wants'
⚠️ Context window full! Dropped token: 'to'

Final Active Context: build a modular backend application
```
