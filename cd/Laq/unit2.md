**SET – 2**

---

### **Q1) How convolutional architectures are adapted to handle structured outputs?**

Convolutional Neural Networks (CNNs) were first made for image classification (one label per image), but they can also handle **structured outputs**, where each pixel or region has its own label or value.

**How they are adapted:**

1. **Fully Convolutional Networks (FCNs):**
   Replace final dense layers with convolution layers so the model gives an **output map** instead of a single label.
   Example – Image segmentation, where every pixel gets a class label.

2. **Encoder–Decoder Architectures:**
   Encoder compresses the image into features, and the decoder rebuilds it into structured form (like another image or mask).
   Example – Autoencoders, U-Net.

3. **Skip Connections:**
   Connect earlier layers (which keep detailed features) with later layers (which have abstract info) for better accuracy.

4. **Multi-scale Feature Extraction:**
   Uses filters of different sizes to understand both small and large patterns in one image.

**Conclusion:**
By using these techniques, CNNs can produce structured and detailed outputs useful for **segmentation, detection, and image generation**, not just classification.

---

### **Q2) CNNs are not only used for classification but also for image segmentation, object detection, and sequence labeling. Justify your answer.**

CNNs can handle many visual and sequential tasks because they learn to detect patterns automatically at different levels — edges, shapes, and objects.

**1. Image Classification:**
CNNs learn to classify images into one category (e.g., dog or cat).
This is their most basic use.

**2. Image Segmentation:**
Each pixel is labeled, dividing the image into meaningful regions (e.g., separating road, car, sky).
CNNs do this using **Fully Convolutional Networks (FCN)** and **U-Net**.

**3. Object Detection:**
CNNs find and locate objects by drawing bounding boxes around them.
Examples: YOLO, Faster R-CNN.

**4. Sequence Labeling:**
CNNs can process sequences such as **text** or **speech** when combined with recurrent layers.
They find features in time-based or order-based data.

**Why it works:**

* CNNs capture spatial and local relationships.
* Deeper layers learn more abstract patterns.
* Can be customized for multiple outputs.

**Conclusion:**
CNNs are flexible feature extractors that work for **classification, segmentation, detection, and even sequences**, proving their power beyond simple image tasks.

---

### **Q5) How hyperparameters play a role in deep learning models?**

**Definition:**
Hyperparameters are **settings you choose before training** a model — they control how the model learns and performs.

**Examples:**
Learning rate, batch size, number of layers, number of neurons, dropout rate, optimizer type, etc.

**Role and Importance:**

1. **Learning Control:**
   The learning rate decides how big each training step is — too high causes unstable training, too low makes it slow.

2. **Model Complexity:**
   Number of layers and neurons affect how much the model can learn — more layers = more capacity, but also risk of overfitting.

3. **Regularization:**
   Dropout rate and weight decay prevent overfitting by keeping the model from memorizing the training data.

4. **Training Speed and Stability:**
   Batch size and optimizer influence how fast and smoothly learning happens.

5. **Performance Tuning:**
   The right combination of hyperparameters leads to better accuracy and faster convergence.

**Conclusion:**
Hyperparameters are like the **control knobs** of a deep learning model — tuning them properly can greatly improve performance, while wrong settings can completely spoil training.

---

### **Q6) Why is random search sometimes more effective than grid search for hyperparameter selection?**

**Grid Search:**
Tries every possible combination of hyperparameter values (like testing all points on a grid).
This is **slow** and wastes effort on unimportant areas.

**Random Search:**
Chooses **random combinations** of hyperparameters to test.
Surprisingly, this often finds good results faster.

**Why Random Search works better:**

1. **Covers more possibilities:**
   It explores a wider range instead of checking only fixed points.

2. **Saves time:**
   Doesn’t waste effort on all combinations — tests fewer but smarter samples.

3. **Focuses on important parameters:**
   Some hyperparameters (like learning rate) affect results more than others. Random search has a higher chance to hit good ones.

4. **Scales better:**
   Works well even when there are many hyperparameters.

**Example:**
If you have 5 parameters and only 1 or 2 really matter, grid search spends equal time on all, but random search finds good results faster by chance.

**Conclusion:**
Random search is often **faster and more efficient** for tuning deep learning models because it explores the parameter space more effectively without testing everything.
