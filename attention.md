 # LLM Challenges

Welcome to the LLM Challenges repository! This project is designed to help learners explore and understand large language models (LLMs) through a series of engaging challenges. Each challenge is structured to build knowledge progressively, from basic concepts to more advanced applications.

## How Attention works in AI
### Lets say your friend asks: "What does attention mean in AI?" Help them understand by showing, not just telling:
Example:
```
Currently i am trying to explain how attenttion works to my friend.
```
In this challange i will try to simplify the attention mechanisms in Transformers, exploring what they are, why they are essential, and how they work their magic.

## What is the attention mechanism?

* At its core, an attention mechanism is a computational method inspired by human congnition that helps models in AI focus on specific parts of the input data while processing it.

* Attention is the ability of the model to ***focus on importatnt part*** of the sentence. It helps in understanding the context of the text data or any sequential data. 

* Think of it as a way for the model to decide which parts of the data are more relevant or important at any given moment.


## Attention mechanism intuition 

<p align="center">
  <img src="https://raw.githubusercontent.com/YusuCoder/LLM-challenges/main/example.png" alt="Example" width="500"/>
</p>

* Imagine you are reading a book: Your attention naturally shifts from word to word, emphasing certain words or phrases based on their context and relevance to understand the text better. Attention mechanisms in AI work somewhat similar.

* Thus, Attention is a mechanism that enables models to focus on specific parts of thee input data, assigning ***varying degrees of importance*** to different words. It's like telling the model where to pay attention when processing information.

In simple words:
```
With the help of the attention mechanism, we try to understand context of tthe sentence byu understanding the importance of the specific words by assigning more or less weights to the words.
```

## Self attention mechanism

* Self attention is like looking at different words within the same sentence and deciding how much importance to give to each word when understanding the meaning of the sentence. It helps the model to consider the ***relationship between words within the next***.
* We compare the words of the sentence to the words of the same sentence during computation.

example picture here: 

For example in our sentece, self-attention helps to understand model that ```cat``` and ```mat``` are related because they have high attention wights, indicating they are the subject and object of the action ```sat```.

example picture here:



## How do attention mechanism work?
Lets dive deeper into attention weghts and how they work within the context of self-attention.

## Attention weights:
* In self-attentin, attention weights are numerical values that indicate how much focus or importance each words in sentence should recive from other words in the same sentence.

* The goal is to calculate these weights so that the model can assign higher values to words that are more relevant or have stronger relationships with the cuirrent word which is being processed.

## Calculation of attention weights:
***Query***, ***Key***, and ***Value***: In self-attention, each word in the sentence is associated with three vectors:

* Query: A vector representing the current word that we want to calculate attention weights for.
* Key: Vectors associated with all other words in the sentence, serving as a comparison.
* Value: Vectors associated with all other words, which will be used for the weighted sum.

## Scoring by dot product:
To calculate the attention weights, the model performs a dot product between the query of the current word and the key of all other words. This dot product measures how similar or relevant each word is to the current word.

***Scaling:*** The dot products are scaled down (***divided by the square root of the dimension of the key vectors***) to prevent the gradients from becoming too large.


***SoftMax:***  The scaled dot products are then passed through a softmax function. This function ***normalizes the scores***, turning then into a probability distribution where higher score get higher probabilities. This ensures that the ***attention weights sum up to 1***


***Wighted Sum***: Finally the attention wights obtained from the softmax are used to calculate a weighted sum of the value vactors of all words. This weughted sum represents the new representation of the current wordm, incorporating information from all other words based on their importance scores.



## Interpretation:
* If the attention weight for a specific word is high, it means the model considers that the word highly relevant to understanding the current word's context.

* Lower attention weights indicate that the word is less important or related to the current word.
