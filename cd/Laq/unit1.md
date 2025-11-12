**SET – 1**

---

### **Q1) Discuss the importance of structured output prediction in computer vision and natural language processing tasks.**

Structured output prediction means producing outputs that are **connected or related to each other**, not just one simple answer.
For example:

* In **computer vision**, predicting each pixel’s label in **image segmentation** (like separating sky, road, and trees).
* In **NLP**, predicting words in a sentence during **machine translation** or **speech recognition**.

**Importance:**

1. **Real-life relevance:** Many real-world problems have linked outputs (like words in a sentence or pixels in an image).
2. **Better accuracy:** Considering relationships between outputs gives more meaningful results.
3. **Less manual correction:** The model learns structure automatically instead of combining many small predictions.
4. **Handles complex data:** Useful for tasks that can’t be represented by a single label.
5. **Smarter decisions:** Model learns how parts of the output depend on each other (like grammar or object shapes).

**Conclusion:**
Structured output prediction helps AI models make decisions that are more **realistic, connected, and context-aware**, improving performance in both images and language tasks.

---

### **Q2) How FFT-based convolution algorithms reduce the computational cost compared to naive convolution.**

In deep learning, **convolution** is used to detect features in images, but normal convolution takes a lot of time because it multiplies and adds many values repeatedly.
The **FFT method** (Fast Fourier Transform) makes it faster by doing the work in a smarter way.

**How it helps:**

1. It **changes the data** from normal space to a special form called frequency space.
2. In that form, **convolution becomes simple multiplication**, which is quicker.
3. Then it changes it back to normal form after finishing the calculation.

**Why it’s better:**

* Saves time when images or filters are **large**.
* Used in many **modern deep learning libraries** for faster training.
* Especially helpful in **signal processing or large image processing**.

**Limitations:**

* Not useful for very small filters (like 3×3).
* Needs extra memory and conversion time.
* Slightly harder to implement manually.

**Conclusion:**
FFT-based convolution reduces repeated calculations, making the process **much faster** for large data while keeping results the same.

---

### **Q5) How can gradient checking help debug neural networks.**

When training a neural network, the model learns by adjusting weights using **gradients** (which tell how much to change each weight).
Sometimes these gradients are calculated incorrectly, leading to poor training.
**Gradient checking** is a simple way to make sure those gradients are correct.

**How it works:**

1. You take a small model and calculate the gradients in two ways — one by the computer (normal training way) and another by changing the weights slightly to see how the result changes.
2. Then you compare both results.
3. If they are close, your gradient calculation is correct; if not, there is a mistake in your code or layer logic.

**Why it’s useful:**

* Helps **find bugs early** in training.
* Ensures the **backpropagation** process is working right.
* Saves time by catching mistakes before running large models.
* Builds **trust** in your model’s training process.

**Conclusion:**
Gradient checking is a **debugging tool** that gives confidence your model is learning correctly before you spend hours on full training.

---

### **Q6) Why is multi-digit number recognition more challenging than single-digit recognition.**

Recognizing a single digit (like “5”) is simple — it’s one clear label.
But recognizing multi-digit numbers (like “548”) is harder because the model has to identify **each digit separately** and in the **correct order**.

**Reasons it’s harder:**

1. **Multiple outputs:** The system must predict several digits, not just one.
2. **Overlapping or touching digits:** Makes it harder to separate them clearly.
3. **Different lengths:** Some numbers have 2 digits, some have 5, so the model must handle variable output size.
4. **Background noise:** In real images, numbers might be faint or unclear.
5. **One mistake ruins the output:** If one digit is wrong, the entire number is wrong.

**Ways to handle it:**

* Use models like **RNNs or encoder–decoder networks** that can predict sequences.
* Use **data with many examples** so the model learns all patterns.
* Improve preprocessing — e.g., clear background, resize digits properly.

**Conclusion:**
Multi-digit recognition is tougher because it’s not just about identifying digits, but also **understanding their sequence, spacing, and relationships**, which needs smarter models.
