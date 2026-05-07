# 1. Explain N-Gram Models (10M)

## Introduction

N-gram models are important language models used in NLP to predict the next word in a sentence based on previous words.

---

## What is an N-Gram?

An N-gram is a sequence of N consecutive words.

---

## Basic Idea

The model predicts a word using nearby words.

---

## Types of N-Gram Models

---

### 1. Unigram

Uses one word at a time.

#### Example

“I”, “love”, “music”

---

### 2. Bigram

Uses two consecutive words.

#### Example

“I love”, “love music”

---

### 3. Trigram

Uses three consecutive words.

#### Example

“I love music”

---

### 4. Higher Order N-Grams

Uses more than three words.

---

## Working of N-Gram Model

### Step 1

Sentence is divided into word sequences.

---

### Step 2

Frequency of sequences is calculated.

---

### Step 3

Probability of next word is predicted.

---

## Example

Sentence:
“I love NLP”

Bigram model:

* P(love | I)
* P(NLP | love)

---

## Applications

* Text prediction
* Speech recognition
* Machine translation
* Spell checking

---

## Advantages

* Simple and easy to implement
* Efficient for prediction tasks

---

## Limitations

* Requires large data
* Cannot understand deep meaning
* Data sparsity problem

---

## Conclusion

N-gram models are simple statistical language models that predict word sequences using previous words.

---

# 2. Explain Evaluation Methods in Language Modelling (10M)

## Introduction

Evaluation methods are used to measure the performance and accuracy of language models in NLP.

---

## Need for Evaluation

* Measure model quality
* Compare models
* Improve prediction accuracy

---

## Common Evaluation Methods

---

### 1. Perplexity

Most commonly used evaluation metric.

---

## What is Perplexity?

Perplexity measures how well a language model predicts text.

---

### Interpretation

* Lower perplexity → better model
* Higher perplexity → poor prediction

---

## Example

If a model predicts words correctly, perplexity becomes low.

---

### 2. Accuracy

Measures how many predictions are correct.

---

### 3. Precision

Measures correctness of positive predictions.

---

### 4. Recall

Measures how many relevant results are identified.

---

### 5. F1-Score

Combination of precision and recall.

---

### 6. Human Evaluation

Humans manually judge output quality.

---

## Applications

* Machine translation
* Chatbots
* Text generation
* Speech systems

---

## Challenges

* Different datasets produce different results
* Human language complexity
* Context understanding difficulty

---

## Conclusion

Evaluation methods help determine how effectively a language model predicts and understands language data.

---

# 3. Explain Bayesian Estimation (10M)

## Introduction

Bayesian estimation is a statistical method used in NLP and machine learning for probability prediction and decision making.

---

## What is Bayesian Estimation?

It uses:

* Prior knowledge
* Observed data
* Probability theory

to estimate outcomes.

---

## Basic Idea

Bayesian estimation updates predictions when new information becomes available.

---

## Components of Bayesian Estimation

---

### 1. Prior Probability

Initial belief before observing data.

---

### 2. Likelihood

Probability of observed data.

---

### 3. Posterior Probability

Updated probability after observing data.

---

## Working Process

### Step 1

Start with prior probability.

---

### Step 2

Observe new data.

---

### Step 3

Update probability using Bayes theorem.

---

## Example

Spam email detection:

* Prior belief about spam
* Analyze email words
* Update spam probability

---

## Applications

* Spam filtering
* Speech recognition
* Machine translation
* Text classification

---

## Advantages

* Handles uncertainty well
* Learns from new data
* Flexible probabilistic approach

---

## Limitations

* Requires probability estimation
* Computational complexity

---

## Conclusion

Bayesian estimation is an important probabilistic method used in NLP for prediction, classification, and decision-making.



# 4. Explain Adaptation Techniques in Language Modelling (10M)

## Introduction

Adaptation techniques are methods used to improve language models for specific tasks, users, or domains by adjusting them using new data.

---

## What is Adaptation?

Adaptation means modifying a language model so it performs better in a particular environment or application.

---

## Need for Adaptation Techniques

* General models may not work well in all domains
* Different applications use different vocabulary and styles
* Improves prediction accuracy

---

## Example

A medical chatbot requires medical vocabulary, while a banking chatbot requires financial terms.

---

## Types of Adaptation Techniques

---

### 1. Domain Adaptation

Adapts model to a specific domain.

#### Examples

* Medical domain
* Legal domain
* Banking domain

---

### 2. Speaker Adaptation

Used in speech systems to adapt to different speakers.

---

### 3. Topic Adaptation

Model adjusts according to discussion topic.

---

### 4. Vocabulary Adaptation

Adds new words and terms to improve understanding.

---

### 5. Context Adaptation

Uses user context and previous information.

---

### 6. Online Adaptation

Model continuously learns from new incoming data.

---

## Methods Used in Adaptation

### Fine-Tuning

Training the model again with domain-specific data.

---

### Transfer Learning

Using knowledge from one task for another task.

---

### Interpolation

Combining multiple language models together.

---

## Applications

* Chatbots
* Speech recognition
* Machine translation
* Personalized assistants

---

## Advantages

* Improves accuracy
* Handles domain-specific language
* Better user experience

---

## Challenges

* Requires additional data
* Training complexity
* Risk of overfitting

---

## Conclusion

Adaptation techniques help language models perform efficiently in specific domains and applications by learning from specialized data.

---

# 5. Explain Multilingual Models in NLP (10M)

## Introduction

Multilingual models are NLP models designed to process and understand multiple languages using a single system.

---

## What are Multilingual Models?

These models can:

* Read
* Understand
* Translate
  multiple languages together.

---

## Need for Multilingual Models

* Global communication
* Multilingual applications
* Reduced need for separate models for each language

---

## Working of Multilingual Models

The model is trained using text from multiple languages so it learns common language patterns.

---

## Features of Multilingual Models

### Shared Learning

Knowledge from one language helps another language.

---

### Cross-Lingual Understanding

Model understands relationships between languages.

---

### Common Representation

Different languages are represented in a shared format.

---

## Types of Multilingual Models

---

### 1. Multilingual BERT (mBERT)

Supports many languages using transformer architecture.

---

### 2. XLM Models

Cross-lingual models for multilingual understanding.

---

### 3. Translation Models

Used for translating between languages.

---

## Applications

* Machine translation
* Multilingual chatbots
* Cross-language search
* Speech assistants

---

## Advantages

* Supports many languages
* Reduces training cost
* Helps low-resource languages

---

## Challenges

### 1. Different Grammar Structures

Languages have different syntax.

---

### 2. Data Imbalance

Some languages have less training data.

---

### 3. Script Differences

Languages use different writing systems.

---

### 4. Cultural Context

Meaning changes across cultures.

---

## Conclusion

Multilingual models help NLP systems process multiple languages efficiently using shared learning and cross-lingual understanding.
