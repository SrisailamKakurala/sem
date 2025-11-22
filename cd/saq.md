**UNIT – 1**

1. **What is the difference between a learning algorithm and a traditional program?**
   A traditional program follows fixed rules written by a programmer.
   A learning algorithm *learns patterns from data* and improves its behavior automatically.

2. **Define model capacity in machine learning.**
   Model capacity is the model’s ability to learn different kinds of patterns.
   High capacity → learns complex patterns; low capacity → learns only simple patterns.

3. **What does it mean when a model is overfitting?**
   Overfitting happens when a model memorizes the training data instead of learning general patterns.
   It performs well on training data but poorly on new data.

4. **Give one way to detect underfitting in a model.**
   If both training and validation accuracy are low, the model is underfitting.
   It means the model is too simple to learn the pattern.

5. **What is a hyperparameter? Give an example.**
   A hyperparameter is a setting chosen *before* training.
   Example: learning rate, number of hidden layers.

6. **Why do we need a validation set in model training?**
   A validation set helps check how well the model performs on unseen data during training.
   It guides tuning hyperparameters and prevents overfitting.

7. **Differentiate between bias and variance in predictive models.**
   Bias → error due to overly simple assumptions.
   Variance → error due to being too sensitive to training data.
   We aim for a balance between them.

8. **What is the goal of Maximum Likelihood Estimation (MLE)?**
   MLE finds the model parameters that make the observed data most probable.
   It chooses the “best-fitting” parameters.

9. **What does the “prior” represent in Bayesian statistics?**
   The prior represents what we believe about a parameter *before* looking at new data.
   It expresses our initial assumptions.

10. **State one example of a supervised learning algorithm.**
    Example: Linear Regression or Decision Tree.

11. **State one example of an unsupervised learning algorithm.**
    Example: K-Means Clustering.

12. **Why is Stochastic Gradient Descent (SGD) often used for large datasets?**
    It updates parameters using small batches, so it is much faster and memory-efficient.
    It works well even when the dataset is huge.

13. **List the main steps in building a machine learning algorithm.**
    Collect data → preprocess → train model → validate → tune → test → deploy.

14. **Why is the XOR problem important in the history of neural networks?**
    XOR showed that single-layer networks are limited.
    It proved that hidden layers are necessary for learning complex patterns.

15. **What role do hidden units play in deep neural networks?**
    Hidden units learn useful features from data.
    They allow the network to represent complex patterns.

16. **What does backpropagation compute during training?**
    It calculates how much each weight contributed to the error.
    Then it adjusts the weights to reduce future errors.

---

**UNIT – 2**

### **Regularization**

1. **What is the purpose of regularization in deep learning?**
   To prevent overfitting by keeping the model simpler.
   It helps the model generalize better.

2. **Which parameter norm penalty encourages sparsity, L1 or L2?**
   L1 encourages sparsity by pushing many weights to zero.

3. **How can norm penalties be interpreted as constrained optimization?**
   They restrict how large weights can grow.
   The model learns within a “boundary” to avoid overfitting.

4. **Give one example of dataset augmentation in computer vision.**
   Flipping or rotating an image to create extra training samples.

5. **Why does adding noise to inputs or weights improve robustness?**
   It teaches the model to handle small changes and not depend on exact values.
   This reduces overfitting.

6. **What is semi-supervised learning?**
   A method that uses both labeled and unlabeled data.
   Helpful when labeled data is limited.

7. **How does multi-task learning improve generalization?**
   The model learns multiple related tasks together.
   Shared learning reduces overfitting and improves performance.

8. **Define early stopping.**
   Stopping training when validation performance stops improving.
   Prevents the model from overfitting.

9. **Where is parameter sharing most commonly used in neural networks?**
   In CNNs, where the same filter is used across the image.

10. **What does a sparse representation mean in deep learning?**
    Only a few neurons are active at a time.
    This makes the representation efficient and easier to interpret.

11. **What is bagging in ensemble methods?**
    Training many models on different samples and combining their predictions.
    Reduces variance and improves stability.

12. **What does dropout do during training?**
    Randomly turns off some neurons during training.
    Prevents co-dependence and reduces overfitting.

13. **What is adversarial training?**
    Training the model with slightly altered (attacked) inputs.
    Teaches the model to be resistant to adversarial changes.

14. **What problem does tangent distance aim to solve?**
    It handles small distortions in images, such as rotation or slight movement.

15. **What does Tangent Prop encourage a model to learn?**
    It trains the model to be stable under small transformations.
    Helps improve generalization.

16. **What is the role of the manifold tangent classifier?**
    It keeps the model predictions smooth along the data manifold.
    Reduces sensitivity to small changes.

---

### **Optimization**

17. **How does training a deep model differ from pure optimization?**
    We don’t search for an exact mathematical minimum.
    We focus on finding a good-enough solution that generalizes well.

18. **Name one major challenge in neural network optimization.**
    Deep models often get stuck in poor local minima or saddle points.

19. **What is the simplest optimization algorithm used in training deep models?**
    Gradient Descent (or SGD when using batches).

20. **Why is good parameter initialization important?**
    Bad initialization can slow learning or prevent learning completely.
    Good initialization helps faster and stable training.

21. **Give one example of an algorithm with adaptive learning rates.**
    Adam, RMSProp, or Adagrad.

---

**UNIT – 3**

1. **The Convolution Operation**
   Convolution slides a small filter over an image and multiplies it with pixel values to extract features. It helps detect patterns like edges or textures.

2. **What is a kernel (or filter) in convolution?**
   A kernel is a small matrix that scans the image to detect specific features. Different kernels detect different patterns.

3. **How does stride affect convolution?**
   Stride is how many pixels the filter moves each step. Larger stride → smaller output and faster processing.

4. **What is the purpose of padding in convolution?**
   Padding adds extra pixels around the image to keep the output size the same or to preserve edge information.

5. **Why are CNNs preferred for image data?**
   CNNs capture spatial patterns and reduce parameters, making them very effective for images.

6. **What property of CNNs reduces the number of parameters compared to fully connected networks?**
   Weight sharing: the same filter is used across the whole image, reducing parameters.

7. **How does convolution help capture local patterns?**
   The filter looks at only a small region at a time, allowing it to detect local details like corners or lines.

8. **What does max pooling do?**
   It selects the highest value in a region, keeping the strongest feature.

9. **How does average pooling differ from max pooling?**
   Average pooling takes the average of the region, giving smoother outputs.

10. **Why is pooling important for CNNs?**
    Pooling reduces the size of feature maps, lowering computation and preventing overfitting.

11. **What prior knowledge is encoded by convolution?**
    The idea that nearby pixels are related and patterns can appear anywhere in the image.

12. **How does pooling contribute to translation invariance?**
    Small shifts in the image don’t change pooled values much, making features stable.

13. **Why is convolution considered a strong inductive bias?**
    It forces the model to focus on local patterns and reuse filters, guiding learning effectively.

14. **What is a dilated convolution?**
    A convolution where spaces are inserted between filter cells to capture wider context.

15. **What is the purpose of depthwise separable convolution?**
    To make convolution faster and lighter by splitting spatial and channel operations.

16. **Which convolution type is used for upsampling in CNNs?**
    Transposed convolution (also called deconvolution).

17. **What is a structured output in CNNs?**
    An output that contains multiple values arranged meaningfully, like a segmentation map.

18. **Which task requires pixel-level output from a CNN?**
    Image segmentation.

19. **How do CNNs handle image segmentation differently from classification?**
    Segmentation predicts a label for each pixel, while classification gives one label for the whole image.

20. **What type of data is 1D convolution typically used for?**
    Sequential data like audio or text sequences.

21. **Which kind of data requires 3D convolution?**
    Video data or 3D medical images with depth.

22. **Can CNNs be applied to text data?**
    Yes, by treating text as a sequence and applying 1D convolutions.

23. **Why are efficient convolution algorithms necessary?**
    They speed up training and reduce computation, especially in deep models.

24. **Name one algorithm that speeds up convolution.**
    FFT-based convolution or Winograd algorithm.

25. **How do efficient algorithms affect training time?**
    They reduce the number of operations, making training faster.

26. **What is a random feature in CNNs?**
    A feature learned from random initial filters before training.

27. **Why are unsupervised features useful when labeled data is scarce?**
    They allow models to learn basic patterns from unlabeled data.

28. **How can unsupervised learning help CNN pretraining?**
    A model first learns general features from unlabeled data, then fine-tunes on labeled data for better performance.

---

**UNIT – 4**

1. **What does it mean to unfold a computational graph in RNNs?**
   It means expanding the RNN across time steps to show repeated operations as a sequence.

2. **Which training algorithm relies on unfolding?**
   Backpropagation Through Time (BPTT).

3. **Why is unfolding necessary for sequence models?**
   It allows the model to compute gradients across all time steps.

4. **What type of data are RNNs designed for?**
   Sequential data like text, speech, or time series.

5. **What is the role of the hidden state in RNNs?**
   It stores past information and passes it to the next time step.

6. **Why are RNNs considered “memory-based” models?**
   Because they keep information from previous steps in their hidden state.

7. **How does a bidirectional RNN differ from a standard RNN?**
   It processes data both forward and backward for more context.

8. **Which tasks benefit most from bidirectional RNNs?**
   Tasks where full context helps, such as translation or sentiment analysis.

9. **Why can’t bidirectional RNNs be used for real-time prediction?**
   They need future input, which is unavailable in real-time settings.

10. **What are the two main parts of a seq2seq model?**
    Encoder and decoder.

11. **What is the role of the encoder in seq2seq architectures?**
    It converts the input sequence into a meaningful representation.

12. **Which type of problem is encoder-decoder architecture commonly used for?**
    Machine translation, summarization, and chatbots.

13. **What makes an RNN “deep”?**
    Using multiple stacked RNN layers.

14. **Why might stacking multiple RNN layers be beneficial?**
    It allows learning more complex patterns.

15. **What is one challenge of training deep RNNs?**
    They often suffer from vanishing or exploding gradients.

16. **What data structure do recursive neural networks work on?**
    Tree structures.

17. **Which NLP task commonly uses recursive neural networks?**
    Sentence parsing or sentiment analysis.

18. **How do recursive networks differ from recurrent networks?**
    Recursive networks follow tree structures; recurrent networks follow sequences.

19. **What is the vanishing gradient problem?**
    Gradients become very small, slowing or stopping learning.

20. **Why do RNNs struggle with long-term dependencies?**
    Gradients fade over long sequences, losing old information.

21. **What happens when gradients “explode” during training?**
    Very large gradients make the model unstable and weights blow up.

22. **What is the “reservoir” in an echo state network?**
    A large, fixed recurrent layer with random connections.

23. **Which part of an ESN is trained?**
    Only the output layer.

24. **How do ESNs simplify training compared to traditional RNNs?**
    They avoid training the recurrent weights, making training extremely fast.

25. **What is a leaky unit in RNNs?**
    A unit that keeps part of its previous state while updating slowly.

26. **Why are multiple time scales useful in sequence modeling?**
    They help capture both short and long-term patterns.

27. **How do leaky units help capture long-term patterns?**
    They update gradually, allowing memory to last longer.

28. **Which gates are used in an LSTM cell?**
    Input gate, forget gate, and output gate.

29. **What does the forget gate in LSTM do?**
    It decides what old information to erase from memory.

30. **How do GRUs differ from LSTMs?**
    GRUs have fewer gates and a simpler structure but similar performance.

31. **Which optimization issue arises in long RNN sequences?**
    Vanishing and exploding gradients.

32. **What is gradient clipping used for?**
    To prevent gradients from getting too large.

33. **Why does careful weight initialization matter in RNNs?**
    Bad initialization can worsen gradient problems.

34. **What is explicit memory in neural networks?**
    A separate memory component outside the main network.

35. **Name one model that uses explicit memory.**
    Neural Turing Machines or Memory Networks.

36. **How does explicit memory differ from implicit memory in RNNs?**
    Explicit memory stores information separately; implicit memory stores it in hidden states.

---

**UNIT – 5**

1. **What performance metric would you use for a binary classification problem with imbalanced data, and why?**
   Use **F1-score or AUC-ROC** because accuracy can be misleading when one class dominates.

2. **How does cross-entropy loss differ from accuracy as a performance measure?**
   Accuracy checks if predictions are correct, while cross-entropy measures how confident and close the predicted probabilities are to the true label.

3. **Why is it important to evaluate models with multiple metrics instead of just one?**
   Different metrics highlight different weaknesses. One metric alone may hide issues like imbalance or poor confidence.

4. **What is a baseline model, and why is it useful?**
   A baseline model is a simple reference model. It helps check if advanced models are actually improving performance.

5. **Give an example of a simple baseline model for text classification.**
   Predicting the most frequent class for all inputs.

6. **How do baseline models help in identifying whether a complex model is actually useful?**
   If the complex model doesn’t outperform the baseline, it signals poor learning or issues in data.

7. **What signs indicate that a model might benefit from more training data?**
   High variance between training and validation scores or unstable predictions.

8. **How can a learning curve help decide whether to gather additional data?**
   If validation error keeps decreasing as data increases, more data will likely improve performance.

9. **Why is more data not always the best solution for poor performance?**
   The issue might be the model design, poor features, or bad hyperparameters—not data size.

10. **What is the role of hyperparameters in deep learning models?**
    They control how the model learns, such as learning speed, structure, and regularization strength.

11. **Name three common hyperparameters that need tuning in neural networks.**
    Learning rate, number of layers, and batch size.

12. **Why is random search sometimes more effective than grid search for hyperparameter selection?**
    Random search explores a wider range of possibilities, while grid search wastes time on less important combinations.

13. **What can overfitting tell you about your model or dataset?**
    The model is too complex or the dataset is too small for the patterns it's trying to learn.

14. **Why is it useful to test a model on a small subset of data during debugging?**
    It helps catch basic bugs quickly without waiting for long training cycles.

15. **How can gradient checking help debug neural networks?**
    By comparing computed gradients with numerical estimates to detect mistakes in backpropagation.

16. **Why is multi-digit number recognition more challenging than single-digit recognition?**
    The model must understand multiple positions, shapes, and combinations simultaneously.

17. **Which deep learning architecture is often used for digit recognition tasks?**
    Convolutional Neural Networks (CNNs).

18. **What preprocessing step is important for recognizing handwritten digits?**
    Normalizing or resizing images to a fixed size.

19. **Why do large-scale datasets make deep learning models more effective?**
    More data helps models learn richer patterns and reduces overfitting.

20. **What is distributed training, and why is it important in large-scale deep learning?**
    It trains models across multiple machines to handle huge datasets faster.

21. **Give an example of an application that relies on large-scale deep learning.**
    Self-driving cars using massive image datasets.

22. **What are convolutional neural networks (CNNs) primarily used for in computer vision?**
    They detect patterns in images for tasks like classification and segmentation.

23. **Why is transfer learning important in vision applications?**
    It allows using pre-trained models to save time and perform well with less data.

24. **Give an example of a real-world computer vision application.**
    Face recognition in smartphones.

25. **What type of neural networks are often used for speech recognition tasks?**
    RNNs, LSTMs, or Transformers.

26. **Why is handling variable-length input important in speech recognition?**
    People speak at different speeds, and speech signals vary in duration.

27. **Give an example of a modern speech recognition system.**
    Google Assistant, Siri, or Alexa.

28. **What is word embedding in NLP, and why is it useful?**
    A method to represent words as vectors so models can understand meaning and similarity.

29. **Which deep learning models are widely used for NLP tasks today?**
    Transformers like BERT, GPT, and T5.

30. **Give an example of an NLP application powered by deep learning.**
    Machine translation like Google Translate.

31. **How is deep learning applied in healthcare?**
    Used for diagnosing diseases from scans, predicting risks, and analyzing medical records.

32. **Give an example of a deep learning application in recommendation systems.**
    Netflix or YouTube recommending personalized content.

33. **Why is interpretability important in sensitive deep learning applications like finance or medicine?**
    Decisions must be transparent so users can trust the system and understand why predictions were made.
