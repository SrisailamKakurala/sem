Got it Sri — here are the **same questions, same format, but each answer is now 2–3 lines** and still very simple and easy to remember.

---

# **Unit–1 (CO1)**

### **1. What is the role of a learning algorithm in machine learning?**

A learning algorithm finds patterns from data and adjusts model parameters automatically.
It improves the model’s predictions as it sees more examples.
Essentially, it converts raw data into useful knowledge.

### **2. Why do we use a validation set instead of only training and test sets?**

A validation set helps tune hyperparameters without touching the test set.
It shows when the model starts overfitting the training data.
This keeps the final test accuracy honest and unbiased.

### **3. How is MLE related to fitting parameters in a probabilistic model?**

MLE picks parameter values that make the observed data most likely under the model.
It fits the model based on probability rather than simple error measures.
This makes it widely useful for statistical learning.

### **4. What does bias represent in a model?**

Bias is the error caused by overly simple assumptions.
High bias prevents a model from learning true patterns.
It results in underfitting.

### **5. Give one challenge that motivated deep learning.**

Shallow models struggled with high-dimensional data like images and speech.
They could not learn complex features automatically.
Deep learning solved this by stacking multiple learned layers.

### **6. How does Bayes’ theorem update probabilities?**

It revises an old belief (prior) after seeing new evidence (likelihood).
The result is an updated belief called the posterior.
This process forms the basis of Bayesian reasoning.

### **7. What determines the depth of a neural network?**

The depth is the number of hidden layers between input and output.
More layers allow learning of more abstract features.
This increases modeling power but also training difficulty.

### **8. Why do hidden units allow neural networks to model complex functions?**

Hidden units apply nonlinear transformations to inputs.
These nonlinearities allow combining features in powerful ways.
As a result, networks learn highly complex relationships.

---

# **Unit–2 (CO2)**

### **9. What does L2 regularization penalize?**

It penalizes large weight values by pushing them toward smaller magnitudes.
This makes the model smoother and less likely to overfit.
It spreads importance across multiple features.

### **10. Why does L1 regularization promote sparsity in parameters?**

L1 encourages many weights to become exactly zero.
This results in simpler, more interpretable models.
It also helps when only a few features truly matter.

### **11. What is the main purpose of regularization?**

Regularization prevents models from memorizing training data.
It restricts model complexity so patterns generalize well to new data.
It is essential when training data is limited.

### **12. How does noise injection during training improve generalization?**

Noise forces the model to learn stable and robust patterns.
It prevents the network from relying on exact input values.
This results in better performance on unseen data.

### **13. What is the stopping criterion in early stopping?**

Training stops when validation accuracy stops improving.
This prevents the model from overfitting the training set.
It acts as a natural regularizer.

### **14. Why are sparse representations efficient in neural networks?**

Sparse representations activate only a few neurons at once.
This reduces computation and improves speed.
They also generalize better because they avoid unnecessary complexity.

### **15. What does tangent distance measure?**

It measures similarity between two images under small transformations.
These include shifts, rotations, and slight distortions.
It helps models become insensitive to small variations.

### **16. Why do vanishing gradients hinder training of deep networks?**

Very small gradients cause layers near the input to learn almost nothing.
As a result, deep networks fail to capture long-range information.
Training becomes slow or completely ineffective.

---

# **Unit–3 (CO3)**

### **17. What does the convolution operation compute in CNNs?**

It computes weighted sums over small local patches of an input.
This helps detect features like edges, textures, and shapes.
It works well for data with spatial structure.

### **18. Why are CNNs suited for structured outputs like segmentation maps?**

CNNs maintain the spatial arrangement of pixels.
This allows predicting labels for each pixel, not just the whole image.
Thus they excel at tasks requiring detailed spatial understanding.

### **19. What are random features in the context of convolutional networks?**

They are fixed, randomly initialized filters used for early feature extraction.
They provide generic patterns before learning begins.
Useful when labeled data is very limited.

### **20. How are FFT-based methods used for efficient convolution?**

FFT converts convolution into easier frequency-domain multiplication.
This speeds up large kernel operations significantly.
It is especially beneficial for big images or big filters.

### **21. Why is convolution preferred over fully connected layers for image data?**

Convolution captures local patterns using fewer parameters.
It reduces memory and computation dramatically.
It also matches the natural structure of images.

### **22. What kind of prior do convolution and pooling impose on data?**

They assume nearby pixels are related and patterns repeat across positions.
This is known as a spatial locality and translation-invariance prior.
It simplifies learning and improves generalization.

### **23. How is depthwise separable convolution more efficient than standard convolution?**

It splits filtering into channel-wise convolution and channel mixing.
This reduces computation and parameters by a large margin.
It is widely used in mobile and lightweight models.

---

# **Unit–4 (CO4)**

### **24. What does it mean to “unfold” an RNN into a computational graph?**

It means expanding the RNN across time steps like a chain.
Each time step becomes one layer in the unrolled graph.
This is required for backpropagation through time.

### **25. How does an RNN differ from a feedforward neural network for sequential data?**

An RNN keeps a memory of past inputs through hidden states.
A feedforward network treats every input independently.
Thus RNNs are better for sequences like text and audio.

### **26. What is the key structural difference between a unidirectional and bidirectional RNN?**

A unidirectional RNN reads input only forward in time.
A bidirectional RNN reads both forward and backward.
This gives better context for tasks like sentiment analysis.

### **27. Why is the encoder–decoder framework useful for machine translation?**

The encoder compresses the whole input sentence into a representation.
The decoder generates the translated sentence from this representation.
This handles variable-length sequences smoothly.

### **28. What type of data structure do recursive neural networks process?**

They process tree-like structures, such as parse trees in NLP.
Each node represents a substructure combining its children.
This helps understand hierarchical relationships in data.

### **29. What is the role of leaky units in recurrent architectures?**

Leaky units retain information slowly over time.
This helps capture medium-range dependencies.
They also stabilize training by preventing sudden forgetting.

### **30. What three gates are used in the standard LSTM?**

The input gate controls new information.
The forget gate decides what to remove.
The output gate produces the next hidden state.

### **31. How do specialized initialization strategies help RNNs learn long-term dependencies?**

They prevent gradients from exploding or vanishing.
Good initialization keeps signal strength stable across time.
This makes long sequence learning much easier.

---

# **Unit–5 (CO5)**

### **32. What is the difference between accuracy and precision?**

Accuracy measures how often the model is correct overall.
Precision measures how many predicted positives are actually correct.
Precision is especially important for imbalanced problems.

### **33. How can learning curves indicate if more data will improve performance?**

If training and validation curves are far apart, the model is overfitting.
More data can close this gap and improve generalization.
If both curves are high-error, more data won’t help.

### **34. What is the purpose of checking gradients?**

To ensure backpropagation is calculating correct updates.
Gradient errors can lead to unstable or incorrect learning.
Checking avoids silent failures during training.

### **35. How does distributed training enable scaling of deep models?**

It splits work across many GPUs or machines.
This allows training huge models that wouldn’t fit on one device.
It also speeds up training dramatically.

### **36. What type of neural network is most commonly used in computer vision?**

CNNs dominate computer vision tasks.
They efficiently capture spatial patterns in images.
Their parameter sharing makes them fast and scalable.

### **37. How can reinforcement learning extend deep learning beyond supervised learning?**

It enables learning by trial-and-error instead of labeled data.
The agent learns policies based on rewards.
This is used in robotics, gaming, and decision-making.

### **38. What input representation is typically used in speech recognition?**

Spectrograms or MFCCs represent audio frequency patterns.
They convert raw sound into visual-like grids.
This makes them compatible with CNNs and RNNs.

### **39. Why are convolutional layers well-suited for image processing?**

They detect edges, textures, and patterns using local filters.
They reuse the same filter across the image, reducing parameters.
This makes them efficient and highly accurate for images.

---
