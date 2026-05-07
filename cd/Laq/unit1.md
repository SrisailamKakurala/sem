# 1. Explain Morphological Models (10M)

## Introduction

Morphological models are used in NLP to study the structure and formation of words. They help computers understand how words are formed using roots, prefixes, and suffixes.

---

## What is Morphology?

Morphology is the study of:

* Word formation
* Word structure
* Meaningful parts of words

---

## What are Morphological Models?

Morphological models are systems that:

* Break words into smaller meaningful parts
* Identify root words and endings
* Analyze grammatical changes

---

## Components of a Word

### Root

Main part carrying meaning.

Example:

* “play” in playing

---

### Prefix

Added before root.

Example:

* “un” in unhappy

---

### Suffix

Added after root.

Example:

* “ing” in playing

---

## Types of Morphology

### 1. Inflectional Morphology

Changes grammatical form without changing meaning.

Examples:

* play → played
* book → books

---

### 2. Derivational Morphology

Creates a new word with new meaning.

Examples:

* happy → happiness
* teach → teacher

---

## Working of Morphological Models

### Step 1: Input Word

The model receives a word.

---

### Step 2: Segmentation

Word is divided into morphemes.

Example:

* “unhappiness” → un + happy + ness

---

### Step 3: Analysis

Meaning and grammar are identified.

---

## Applications in NLP

* Machine translation
* Spell checking
* Speech recognition
* Search engines

---

## Challenges

* Irregular words
* Complex languages
* Multiple meanings

---

## Conclusion

Morphological models help NLP systems understand word structure and meaning, improving language processing and analysis.

---

# 2. Explain Finite State Morphology (10M)

## Introduction

Finite State Morphology is a method used in NLP to analyze and generate words using finite state machines.

---

## What is Finite State Morphology?

It is a computational model that:

* Processes word structures
* Uses states and transitions
* Recognizes valid word forms

---

## Basic Idea

Words are analyzed step-by-step using rules.

Example:

* play → playing
* walk → walked

---

## Finite State Machine (FSM)

A finite state machine contains:

* States
* Transitions
* Input symbols

---

## Working of Finite State Morphology

### Step 1: Start State

Processing begins from an initial state.

---

### Step 2: Read Characters

Characters are checked one by one.

---

### Step 3: State Transition

Machine moves between states based on rules.

---

### Step 4: Final State

If valid pattern is found, word is accepted.

---

## Example

For word “playing”:

* Root → play
* Suffix → ing

FSM recognizes both parts using transitions.

---

## Advantages

* Fast processing
* Efficient word analysis
* Handles large vocabularies

---

## Applications

* Spell checking
* Text analysis
* Morphological parsing
* Language generation

---

## Limitations

* Difficult for irregular forms
* Complex for rich morphology languages

---

## Conclusion

Finite State Morphology is an efficient method for analyzing word structures using state-based models in NLP.


# 3. Explain Document Structure Analysis Methods (10M)

## Introduction

Document structure analysis is the process of identifying and understanding the structure of a document such as headings, paragraphs, tables, and images.

---

## Purpose of Document Structure Analysis

* Organize document content
* Extract useful information
* Improve document understanding in NLP systems

---

## Common Document Structure Analysis Methods

---

### 1. Rule-Based Method

Uses predefined rules to identify document parts.

#### Example

* Large bold text → heading
* Numbered lines → list

---

### 2. Statistical Method

Uses probability and data patterns for analysis.

#### Example

Frequently occurring patterns are identified automatically.

---

### 3. Layout-Based Analysis

Studies physical arrangement of document elements.

#### Includes

* Text alignment
* Spacing
* Columns

---

### 4. Machine Learning Method

Uses training data to classify document sections.

#### Applications

* OCR systems
* PDF analysis

---

### 5. Template Matching

Compares documents with predefined templates.

#### Example

* Invoice recognition
* Form processing

---

## Applications

* Digital libraries
* Document search systems
* Automated form processing
* Information extraction

---

## Challenges

* Different document formats
* Complex layouts
* Handwritten documents

---

## Conclusion

Document structure analysis helps NLP systems understand and organize documents efficiently for better information processing.

---

# 4. Explain Rule-Based vs Statistical Approaches (10M)

## Introduction

Rule-based and statistical approaches are two important methods used in NLP for language processing and analysis.

---

# Rule-Based Approach

## What is it?

This method uses predefined linguistic rules created by experts.

---

## Working

* Rules are manually written
* System follows grammar and language patterns

---

## Example

If a word ends with “ing”, identify it as a verb form.

---

## Advantages

* Easy to understand
* Gives predictable results
* Good for small systems

---

## Limitations

* Difficult to create many rules
* Cannot handle all language variations

---

# Statistical Approach

## What is it?

Uses probability and large amounts of data for language analysis.

---

## Working

* Learns patterns from training data
* Uses statistical models and probabilities

---

## Example

Predicting next word based on frequency.

---

## Advantages

* Handles complex language patterns
* More flexible
* Better for large datasets

---

## Limitations

* Requires huge data
* Training takes time

---

# Difference Between Rule-Based and Statistical Approaches

| Rule-Based             | Statistical      |
| ---------------------- | ---------------- |
| Uses fixed rules       | Uses probability |
| Human-designed         | Data-driven      |
| Less flexible          | More flexible    |
| Works on grammar rules | Learns from data |

---

## Applications

* Machine translation
* Speech recognition
* Text classification

---

## Conclusion

Rule-based approaches rely on predefined rules, while statistical approaches learn from data. Modern NLP often combines both methods.

---

# 5. Explain Features in Document Classification (10M)

## Introduction

Document classification is the process of grouping documents into categories based on their content.

---

## What are Features?

Features are important characteristics used to classify documents.

---

## Types of Features in Document Classification

---

### 1. Word Features

Uses words present in the document.

#### Example

Words like “sports” or “cricket” indicate sports category.

---

### 2. Frequency Features

Uses how often words appear.

#### Example

Repeated words may indicate document topic.

---

### 3. N-gram Features

Uses combinations of words.

#### Example

* Bigram → “machine learning”
* Trigram → “natural language processing”

---

### 4. Syntax Features

Uses grammatical structure.

#### Includes

* Parts of speech
* Sentence patterns

---

### 5. Semantic Features

Uses meaning of words and sentences.

---

### 6. Metadata Features

Uses extra information.

#### Example

* Author
* Date
* File type

---

## Applications

* Email spam detection
* News categorization
* Sentiment analysis

---

## Challenges

* Large vocabulary
* Ambiguous words
* Noisy data

---

## Conclusion

Features play an important role in document classification by helping systems identify and categorize documents accurately.

