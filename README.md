# LLM Challenges

Welcome to the LLM Challenges repository! This project is designed to help learners explore and understand large language models (LLMs) through a series of engaging challenges. Each challenge is structured to build knowledge progressively, from basic concepts to more advanced applications.

## How Attention works in AI
### Lets say your friend asks: '''What does attention mean in AI?'''' Help them understand by showing, not just telling:
Example:
```
Currently i am trying to explain how attenttion works to my friend.
```
### Step 1. (Tokenization)
The model stplits the sentence into tokens
```
["Currently", "I", "am", "trying", "to", "explain", "how", "attention", "works", "to". "my", "friend", "."]
```

### Step 2. (Embeddings)

Each word is turned into a vector - a list of numbers that carry meaning. For example:
**Attention -> [0.13, 0.44, -0.65 ..., 0.02]
**friend -> [0.91, -0.17, 0.33, ..., -0.03]

But the point every word is treated equally. Thats where attention comes in.

So what are the Embading?
Because computer can't understand words like "attention" or "friend" but they can work with numbers/
And not just any numbers - there are vectors are dsigned so that:ww
**Similar words have similar vectors
**Opposite or unrelated words have distant vectors:
For example:

| Word      | Embedding Meaning (Simplified)          |
| --------- | --------------------------------------- |
| attention | close to: focus, concentrate, awareness |
| friend    | close to: buddy, pal, companion         |
| cat       | close to: dog, animal, pet              |
| war       | far from: peace, flower, banana         |


