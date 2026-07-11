# Tokenization

## 1-Liner Definition

Tokenization is the process of breaking raw text into smaller units
called **tokens** (words, subwords, or characters) so an AI model can
convert text into mathematical representations.

------------------------------------------------------------------------

## Short Technical Explanation

Large Language Models (LLMs) cannot directly understand text as strings.
A **tokenizer** converts text into tokens using algorithms such as
**Byte-Pair Encoding (BPE)** or **WordPiece**.

Instead of splitting only on spaces, modern tokenizers split text
according to a learned vocabulary. Common words remain intact, while
rare or complex words are divided into meaningful subwords.

Example:

-   `develop` → `["develop"]`
-   `developing` → `["develop", "ing"]`

Each token is then mapped to a unique integer ID from the model's
vocabulary. These IDs are fed into embedding layers, where they become
vectors that neural networks can process.

------------------------------------------------------------------------

## Real-World Scenarios

### LLM Content Generation

LLMs measure usage and context windows in **tokens**. Simple sentences
use relatively few tokens, while code snippets and uncommon words often
consume more because they are split into multiple subword tokens.

### Search Engine Indexing

Search engines tokenize documents into searchable words, remove
punctuation, and build indexes so user queries can be matched
efficiently.

------------------------------------------------------------------------

## Code Snippet

``` python
# A mock vocabulary representing a tokenizer's trained internal dictionary
tokenizer_vocab = {
    "<PAD>": 0,
    "the": 1,
    "backend": 2,
    "engineer": 3,
    "is": 4,
    "code": 5,
    "develop": 6,
    "ing": 7,
    "!": 8
}

raw_text = "The backend engineer is developing code!"

tokens = ["the", "backend", "engineer", "is", "develop", "ing", "!"]

token_ids = [tokenizer_vocab.get(token, 0) for token in tokens]

print(f"Raw Text: {raw_text}\\n")
print(f"Tokens: {tokens}")
print(f"Token IDs: {token_ids}")
```

### Expected Output

``` text
Raw Text: The backend engineer is developing code!

Tokens:
['the', 'backend', 'engineer', 'is', 'develop', 'ing', '!']

Token IDs:
[1, 2, 3, 4, 6, 7, 8]
```
