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
*Similar words have similar vectors
*Opposite or unrelated words have distant vectors:


### Step 3. (Attention mechanism begins)s

Now model focuses on the question:

```
What are you trying to explain?
```

The model looks at the word ```explain``` because it's the main action of the question.

It asks:
```
Which words in the sentence are important to understand what is being explained?
```

Then it starts assigning attention scores to each word based on how much it helps answer that/

### Step 4. Attention Weights

Let's say the attention is centered on the word ```explain```. The model looks at all other words and gives them a score like this:

| Word          | Attention Score |
| ------------- | --------------- |
| Currently     | 0.02            |
| I             | 0.10            |
| am            | 0.05            |
| trying        | 0.10            |
| to            | 0.02            |
| explain       | 0.05 (center)   |
| how           | 0.15            |
| **attention** | **0.30**        |
| **works**     | **0.18**        |
| to            | 0.01            |
| my            | 0.01            |
| friend        | 0.01            |


The model pays most attention to ```attention``` and ```works``` because they tell what is being explained.


### Step 5: Output Generation