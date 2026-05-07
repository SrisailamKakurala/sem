# 1. Explain Ambiguity Resolution Models (10M)

## Introduction

Ambiguity is a common problem in NLP where a word or sentence can have more than one meaning. Ambiguity resolution models help identify the correct meaning based on context.

---

## What is Ambiguity?

Ambiguity occurs when:

* A word has multiple meanings
* A sentence has multiple interpretations

---

## Example

Sentence:
“I saw a bat.”

Here “bat” may mean:

* An animal
* A cricket bat

---

## Need for Ambiguity Resolution

* Improve language understanding
* Increase NLP accuracy
* Avoid incorrect interpretation

---

## Types of Ambiguity

### 1. Lexical Ambiguity

A single word has multiple meanings.

---

### 2. Syntactic Ambiguity

Sentence structure creates multiple meanings.

---

### 3. Semantic Ambiguity

Meaning of sentence is unclear.

---

## Ambiguity Resolution Models

---

### 1. Rule-Based Models

Uses grammar and language rules to resolve ambiguity.

#### Example

Context rules identify correct meaning.

---

#### Advantages

* Easy to understand
* Gives controlled output

---

#### Limitations

* Difficult to create many rules

---

### 2. Statistical Models

Uses probabilities and large datasets.

#### Working

* Chooses most probable meaning based on data frequency.

---

#### Advantages

* Handles large-scale language data
* More flexible

---

### 3. Machine Learning Models

Learns ambiguity patterns from training data.

#### Techniques

* Decision trees
* Neural networks

---

### 4. Knowledge-Based Models

Uses dictionaries and semantic databases.

#### Example

WordNet for word meanings.

---

### 5. Context-Based Models

Uses nearby words and sentence context.

#### Example

“river bank” vs “bank account”

---

## Applications

* Machine translation
* Chatbots
* Search engines
* Speech recognition

---

## Challenges

* Complex language usage
* Limited training data
* Context understanding difficulty

---

## Conclusion

Ambiguity resolution models help NLP systems determine correct meanings and improve language understanding using rules, probability, and context.

---

# 2. Explain Multilingual Issues in NLP (10M)

## Introduction

Multilingual NLP deals with processing multiple languages. Different languages create many challenges for NLP systems.

---

## What is Multilingual NLP?

It is the ability of NLP systems to:

* Understand
* Process
* Translate multiple languages

---

## Need for Multilingual NLP

* Global communication
* Translation systems
* Multilingual applications

---

## Major Multilingual Issues

---

### 1. Different Grammar Structures

Languages follow different sentence patterns.

#### Example

English:
“Ram eats mango”

Japanese structure is different.

---

### 2. Vocabulary Differences

Words differ across languages.

#### Problem

Same meaning may have different words.

---

### 3. Morphological Complexity

Some languages have complex word formations.

#### Example

Indian languages often contain long compound words.

---

### 4. Ambiguity

A word may have multiple meanings in different languages.

---

### 5. Lack of Training Data

Many languages have limited datasets.

---

### 6. Script and Writing System Differences

Languages use different scripts.

#### Examples

* English → Latin script
* Hindi → Devanagari

---

### 7. Cultural and Contextual Differences

Meaning changes based on culture and usage.

---

### 8. Translation Challenges

Direct translation may not preserve meaning.

---

## Solutions for Multilingual Issues

### 1. Machine Translation

Automatically translates languages.

---

### 2. Cross-Lingual Models

Shared models for multiple languages.

---

### 3. Large Multilingual Datasets

Training on multiple language corpora.

---

## Applications

* Google Translate
* Multilingual chatbots
* Speech assistants

---

## Conclusion

Multilingual issues make NLP challenging due to grammar, scripts, and cultural differences, but advanced models help process multiple languages effectively.


# 3. Explain Word Sense Disambiguation (WSD) Techniques (10M)

## Introduction

Word Sense Disambiguation (WSD) is the process of identifying the correct meaning of a word based on context.

---

## What is WSD?

Many words have multiple meanings.
WSD helps NLP systems choose the correct meaning.

---

## Example

Sentence:
“He sat on the bank.”

Here “bank” may mean:

* River bank
* Financial bank

Context determines correct meaning.

---

## Need for WSD

* Improve language understanding
* Reduce ambiguity
* Increase NLP accuracy

---

## WSD Techniques

---

### 1. Knowledge-Based Techniques

Uses dictionaries, semantic networks, and lexical databases.

#### Example

WordNet is commonly used.

---

#### Advantages

* Does not require large training data

---

#### Limitations

* Depends on knowledge resources

---

### 2. Supervised Learning Technique

Uses labeled training data.

#### Working

* Model learns correct meanings from examples.

---

#### Advantages

* High accuracy

---

#### Limitations

* Requires large annotated datasets

---

### 3. Unsupervised Technique

Uses clustering and similarity methods without labeled data.

---

#### Advantages

* No training data needed

---

#### Limitations

* Lower accuracy

---

### 4. Semi-Supervised Technique

Combines labeled and unlabeled data.

---

### 5. Context-Based Technique

Uses nearby words to determine meaning.

#### Example

“money” near “bank” indicates financial meaning.

---

## Applications

* Machine translation
* Search engines
* Chatbots
* Speech recognition

---

## Challenges

* Complex contexts
* Multiple meanings
* Lack of training data

---

## Conclusion

WSD techniques help NLP systems identify correct word meanings using knowledge, machine learning, and context analysis.

---

# 4. Explain Semantic Parsing Paradigms (10M)

## Introduction

Semantic parsing is the process of converting natural language into a machine-understandable meaning representation.

---

## What is Semantic Parsing?

It analyzes sentence meaning rather than only grammar.

---

## Purpose

* Understand sentence meaning
* Represent meaning formally
* Support intelligent systems

---

## Semantic Parsing Paradigms

---

### 1. Rule-Based Paradigm

Uses predefined grammar and semantic rules.

#### Features

* Human-designed rules
* Controlled processing

---

#### Advantages

* Easy interpretation

---

#### Limitations

* Difficult for large systems

---

### 2. Statistical Paradigm

Uses probabilities and training data.

#### Working

* Learns meaning patterns from data.

---

#### Advantages

* Handles large datasets
* More flexible

---

### 3. Machine Learning Paradigm

Uses AI and neural networks for semantic understanding.

#### Techniques

* Deep learning
* Neural semantic parsing

---

### 4. Logic-Based Paradigm

Represents meaning using formal logic.

#### Example

First Order Logic (FOL)

---

### 5. Frame-Based Paradigm

Represents meaning using predefined frames or structures.

---

## Applications

* Question answering systems
* Virtual assistants
* Machine translation
* Chatbots

---

## Challenges

* Ambiguous sentences
* Complex language structures
* Context understanding

---

## Conclusion

Semantic parsing paradigms help NLP systems understand and represent sentence meaning using rules, logic, and machine learning approaches.

---

# 5. Explain Knowledge-Based WSD vs Statistical WSD (10M)

## Introduction

Knowledge-based and statistical approaches are two major methods used for Word Sense Disambiguation (WSD).

---

# Knowledge-Based WSD

## What is it?

Uses dictionaries, semantic databases, and linguistic knowledge to identify meanings.

---

## Working

* Compares word meanings using lexical resources
* Uses semantic similarity

---

## Example Resources

* WordNet
* Dictionaries

---

## Advantages

* No large training data needed
* Easy to interpret

---

## Limitations

* Depends heavily on knowledge resources
* Limited coverage

---

# Statistical WSD

## What is it?

Uses probability and machine learning techniques.

---

## Working

* Learns word meanings from large datasets
* Uses context frequency and patterns

---

## Advantages

* Higher accuracy with large data
* Handles real-world usage better

---

## Limitations

* Requires training data
* Computationally expensive

---

# Difference Between Knowledge-Based and Statistical WSD

| Knowledge-Based WSD       | Statistical WSD                |
| ------------------------- | ------------------------------ |
| Uses dictionaries         | Uses data and probability      |
| No training data required | Requires large datasets        |
| Rule/knowledge driven     | Data-driven                    |
| Easier to explain         | More accurate in large systems |

---

## Applications

* Search engines
* Machine translation
* Chatbots
* Information retrieval

---

## Conclusion

Knowledge-based WSD uses semantic resources, while statistical WSD uses data-driven learning. Modern NLP often combines both approaches for better accuracy.
