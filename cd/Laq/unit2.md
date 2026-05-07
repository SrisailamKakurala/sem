# 1. Explain Parsing Algorithms (10M)

## Introduction

Parsing algorithms are methods used in NLP to analyze the grammatical structure of sentences. They help computers understand how words are arranged in a sentence.

---

## What is Parsing?

Parsing is the process of:

* Breaking a sentence into parts
* Checking grammatical correctness
* Creating sentence structure

---

## Purpose of Parsing Algorithms

* Understand sentence meaning
* Identify relationships between words
* Support NLP applications

---

## Types of Parsing Algorithms

---

### 1. Top-Down Parsing

Starts from the main grammar rule and moves toward words.

#### Working

* Begins with the start symbol
* Expands grammar rules step-by-step

---

#### Advantages

* Simple to understand

---

#### Limitations

* May repeat unnecessary steps

---

### 2. Bottom-Up Parsing

Starts from words and builds sentence structure upward.

#### Working

* Individual words are combined into phrases
* Phrases form complete sentence

---

#### Advantages

* More efficient for many cases

---

#### Limitations

* Complex implementation

---

### 3. Recursive Descent Parsing

Uses recursive procedures to analyze sentence structure.

#### Features

* Simple parsing technique
* Based on grammar rules

---

### 4. CYK Algorithm

A dynamic programming parsing algorithm used with CFG.

#### Features

* Efficient for complex parsing
* Uses table-based processing

---

### 5. Dependency Parsing

Finds relationships between words in a sentence.

#### Example

Subject → verb → object relation

---

## Applications

* Machine translation
* Grammar checking
* Question answering systems
* Speech processing

---

## Challenges

* Ambiguous sentences
* Complex grammar
* Multiple sentence interpretations

---

## Conclusion

Parsing algorithms are important in NLP for understanding sentence structure and improving language processing systems.

---

# 2. Explain Syntactic Structure Representation (10M)

## Introduction

Syntactic structure representation is the method of showing how words are arranged grammatically in a sentence.

---

## What is Syntax?

Syntax is the study of:

* Sentence structure
* Word arrangement
* Grammar rules

---

## Purpose of Syntactic Representation

* Understand grammatical relationships
* Represent sentence structure clearly
* Help NLP systems process language

---

## Types of Syntactic Structure Representation

---

### 1. Parse Tree Representation

Represents sentence structure using a tree format.

#### Features

* Root node represents sentence
* Branches represent phrases and words

---

#### Example

Sentence:
“The boy plays cricket”

* Sentence

  * Noun Phrase
  * Verb Phrase

---

### 2. Dependency Representation

Shows dependency relations between words.

#### Example

* Subject connected to verb
* Verb connected to object

---

### 3. Phrase Structure Representation

Groups words into phrases.

#### Types of Phrases

* Noun phrase
* Verb phrase
* Prepositional phrase

---

### 4. Bracket Notation

Represents sentence structure using brackets.

#### Example

(S (NP Boy) (VP plays cricket))

---

## Advantages

* Improves sentence understanding
* Helps semantic analysis
* Supports parsing systems

---

## Applications

* Machine translation
* Speech recognition
* Grammar correction
* Chatbots

---

## Challenges

* Ambiguity in sentences
* Complex sentence structures
* Multiple interpretations

---

## Conclusion

Syntactic structure representation helps NLP systems understand grammatical structure and relationships between words effectively.


# 3. Explain the Role of Treebanks (10M)

## Introduction

Treebanks are important resources in NLP used to store sentences along with their grammatical structure.

---

## What is a Treebank?

A treebank is a collection of:

* Sentences
* Parse trees
* Syntactic annotations

It helps computers learn language structure.

---

## Purpose of Treebanks

* Train NLP systems
* Study grammar patterns
* Improve parsing accuracy

---

## Structure of a Treebank

Each sentence is stored with:

* Words
* Grammar labels
* Tree structure

---

## Example

Sentence:
“The cat sleeps”

Treebank stores:

* Noun phrase
* Verb phrase
* Relationships between words

---

## Types of Treebanks

### 1. Constituency Treebank

Represents phrase structure.

---

### 2. Dependency Treebank

Represents word dependencies.

---

## Role of Treebanks in NLP

### 1. Parser Training

Used to train parsing algorithms.

---

### 2. Grammar Analysis

Helps identify language patterns.

---

### 3. Machine Translation

Improves translation quality.

---

### 4. Speech Recognition

Helps understand sentence structure.

---

### 5. Research and Development

Useful for NLP experiments and evaluation.

---

## Advantages

* Improves parsing accuracy
* Provides structured language data
* Useful for machine learning

---

## Challenges

* Time-consuming annotation
* Expensive to create
* Language complexity

---

## Conclusion

Treebanks play a major role in NLP by providing structured grammatical data for training and improving language processing systems.

---

# 4. Explain PCFG (Probabilistic Context-Free Grammar) (10M)

## Introduction

PCFG is an extension of Context-Free Grammar that uses probabilities for grammar rules.

---

## What is PCFG?

Probabilistic Context-Free Grammar assigns:

* Grammar rules
* Probability values

This helps choose the most likely sentence structure.

---

## Need for PCFG

A sentence may have multiple parse trees due to ambiguity.
PCFG helps identify the most probable interpretation.

---

## Components of PCFG

### 1. Non-Terminals

Grammar symbols like:

* Sentence (S)
* Noun Phrase (NP)

---

### 2. Terminals

Actual words in sentence.

---

### 3. Production Rules

Rules used to form sentences.

Example:
S → NP + VP

---

### 4. Probabilities

Each rule has a probability value.

---

## Working of PCFG

### Step 1

Apply grammar rules.

---

### Step 2

Calculate probability of parse trees.

---

### Step 3

Select parse tree with highest probability.

---

## Advantages

* Handles ambiguity better
* Improves parsing accuracy
* Useful in statistical NLP

---

## Applications

* Speech recognition
* Machine translation
* Syntax parsing

---

## Limitations

* Requires training data
* Complex probability calculations

---

## Conclusion

PCFG combines grammar rules with probability to improve sentence parsing and ambiguity resolution in NLP.

---

# 5. Explain Chart Parsing (10M)

## Introduction

Chart parsing is an efficient parsing technique used in NLP to analyze sentence structure.

---

## What is Chart Parsing?

Chart parsing stores intermediate parsing results in a table called a chart to avoid repeated calculations.

---

## Purpose

* Improve parsing efficiency
* Reduce repeated work
* Handle ambiguity effectively

---

## Main Components

### 1. Chart

A data structure storing partial parsing results.

---

### 2. Edges

Represent parsing progress in the chart.

---

### 3. Grammar Rules

Used for sentence analysis.

---

## Working of Chart Parsing

### Step 1

Sentence words are entered into chart.

---

### Step 2

Grammar rules are applied.

---

### Step 3

Partial results are stored.

---

### Step 4

Final parse tree is generated.

---

## Types of Chart Parsing

### 1. Top-Down Chart Parsing

Starts from grammar rules.

---

### 2. Bottom-Up Chart Parsing

Starts from words.

---

### 3. Earley Parser

A popular chart parsing algorithm.

---

## Advantages

* Avoids repeated computations
* Efficient for long sentences
* Handles ambiguity well

---

## Applications

* Syntax analysis
* Machine translation
* Grammar checking

---

## Challenges

* Memory usage can be high
* Complex implementation

---

## Conclusion

Chart parsing is an efficient NLP parsing method that improves sentence analysis by storing intermediate parsing results.
