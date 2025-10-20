
---

# 🧠 AI Foundations — Module: **AI Concepts, Domains & Tasks**

**Instructor:** Nick, Senior Cloud Engineer at Oracle
**Goal:** Understand what AI is, how it differs from ML and DL, and explore the main AI domains — **Language, Audio/Speech, and Vision** — along with real-world tasks and model types.

---

## 🎯 **Module Objectives**

By the end of this module, you should be able to:

* Explain **AI concepts** and core principles
* Describe **common AI domains and tasks**
* Distinguish between **AI, Machine Learning (ML), and Deep Learning (DL)**

---

## 🤖 **What Is Artificial Intelligence (AI)?**

**AI** is the ability of **machines to imitate human cognitive abilities** — learning, reasoning, understanding, communication, and creativity.

### 🧍 Human Intelligence Capabilities

Humans can:

* Learn new skills through observation and reasoning
* Understand abstract concepts
* Communicate effectively (language + non-verbal cues)
* Handle complex decisions dynamically
* Plan short-term and long-term tasks
* Create art, music, and original ideas

When machines replicate **any of these abilities**, we call it **Artificial Intelligence (AI)**.

---

## 🧠 **Artificial General Intelligence (AGI)** vs **Artificial Intelligence (AI)**

| Type                                      | Description                                                                                                                 | Example                                                                            |
| ----------------------------------------- | --------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| **AGI (Artificial General Intelligence)** | Mimics full human intelligence — sensory, motor, learning, and reasoning. Can perform complex tasks **without human help**. | A system that plans, learns, and solves problems in multiple domains like a human. |
| **AI (Narrow AI)**                        | Focuses on solving **specific, narrow objectives** using intelligent behavior.                                              | Email spam detection, product recommendations, or self-driving features.           |

---

## 💡 **Examples of AI in Everyday Life**

* 📸 **Vision:** Identify if an image shows an apple or an orange
* 📧 **Classification:** Detect spam vs. non-spam emails
* 💻 **Code Generation:** AI writing computer code
* 🚗 **Prediction:** Estimating the price of a used car

---

## ⚙️ **Why AI Is Needed**

AI helps overcome human limits in handling **massive data** and performing repetitive or complex tasks efficiently.

### 🔑 Two Core Reasons:

1. **Automate Routine Tasks**

   * Examples: Credit card approval, insurance claim processing, product recommendations.

2. **Enhance Creativity & Intelligence**

   * AI acts like a “smart friend” — can write stories, poems, music, design products, and generate code.

---

## 🌐 **Major AI Domains**

| Domain                        | Example Tasks                                       |
| ----------------------------- | --------------------------------------------------- |
| 🗣️ **Language**              | Text translation, question answering, summarization |
| 👁️ **Vision**                | Image classification, facial recognition            |
| 🎧 **Speech / Audio**         | Text-to-speech, speech recognition                  |
| 🛒 **Recommendations**        | Cross-selling, personalized offers                  |
| ⚠️ **Anomaly Detection**      | Fraud detection, machine fault prediction           |
| 🚘 **Reinforcement Learning** | Self-driving cars                                   |
| 🌦️ **Forecasting**           | Weather prediction, stock forecasting               |
| 🎨 **Generative AI**          | Creating new text, music, code, or images           |

---

# 📚 Module 2 — AI Tasks & Data in Language, Audio/Speech, and Vision Domains

---

## 🗣️ **Language Domain**

### 🔹 1. Text-Based Tasks

Use **text as input**, producing different text-based outputs.

Examples:

* Language detection
* Entity extraction
* Key phrase identification
* Text translation

### 🔹 2. Generative AI Tasks

Output is **newly generated text**.

Examples:

* Story or poem creation
* Text summarization
* Question answering (e.g., ChatGPT)

---

### 🧩 **How Text Data Works**

| Concept                 | Description                                                                 |
| ----------------------- | --------------------------------------------------------------------------- |
| **Sequential Nature**   | Text is ordered — sentences → words → tokens.                               |
| **Tokenization**        | Converts words into numerical representations for model training.           |
| **Padding**             | Ensures all sequences have equal length.                                    |
| **Similarity Measures** | Dot or cosine similarity used to measure closeness between words/sentences. |
| **Embeddings**          | Represent words/sentences in vector space based on meaning.                 |

---

### 🧠 **Language AI Model Architectures**

| Model Type                         | Function                                                                 |
| ---------------------------------- | ------------------------------------------------------------------------ |
| **RNN (Recurrent Neural Network)** | Processes data sequentially, remembers previous states.                  |
| **LSTM (Long Short-Term Memory)**  | Like RNN, but better at remembering long-term dependencies via gating.   |
| **Transformer**                    | Processes in parallel; uses self-attention to understand context deeply. |

---

## 🎧 **Audio & Speech Domain**

### 🔹 1. Audio/Speech Tasks

Input is **audio or speech**, output varies by use case.

Examples:

* Speech-to-text conversion
* Speaker recognition
* Voice conversion

### 🔹 2. Generative Audio Tasks

Output is **audio generated by models**.

Examples:

* Music composition
* Speech synthesis

---

### 🎼 **Understanding Audio Data**

| Concept                    | Description                                                                                                  |
| -------------------------- | ------------------------------------------------------------------------------------------------------------ |
| **Sampling Rate**          | Number of samples per second (44.1 kHz = 44,100 samples/sec).                                                |
| **Bit Depth**              | Number of bits per sample (defines quality/detail).                                                          |
| **Correlation of Samples** | A single sample means little; multiple samples form patterns (like hearing part of a song vs. the full one). |

---

### 🧠 **Audio/Speech Model Architectures**

| Model                             | Purpose                                             |
| --------------------------------- | --------------------------------------------------- |
| **RNN / LSTM**                    | Handle sequential sound patterns.                   |
| **Transformer**                   | Parallel processing of audio sequences.             |
| **VAE (Variational Autoencoder)** | Generate new audio samples.                         |
| **Waveform Models**               | Directly generate or modify wave signals.           |
| **Siamese Networks**              | Compare audio samples (e.g., speaker verification). |

---

## 👁️ **Vision Domain**

### 🔹 1. Image-Based Tasks

Input: Image → Output: Classification / Object detection

Examples:

* Image classification (cat vs. dog)
* Object detection
* Facial recognition (used in security, biometrics, law enforcement)

### 🔹 2. Generative Image Tasks

Model **creates new images**.

Examples:

* Text-to-image generation
* High-resolution image creation
* Generating 3D models (objects, buildings, people)

---

### 🖼️ **Understanding Image Data**

| Concept                 | Description                                                  |
| ----------------------- | ------------------------------------------------------------ |
| **Pixels**              | Basic units — grayscale or color.                            |
| **Pattern Recognition** | Multiple pixels form meaningful shapes/features.             |
| **Data Type**           | Depends on the task (classification, detection, generation). |

---

### 🧠 **Vision Model Architectures**

| Model                                    | Purpose                                              |
| ---------------------------------------- | ---------------------------------------------------- |
| **CNN (Convolutional Neural Network)**   | Detects visual patterns; builds feature hierarchies. |
| **YOLO (You Only Look Once)**            | Object detection in a single pass.                   |
| **GAN (Generative Adversarial Network)** | Generates realistic new images.                      |

---

## 🧩 **Other Common AI Tasks**

| Task                       | Type of Data      | Use Case                          |
| -------------------------- | ----------------- | --------------------------------- |
| **Anomaly Detection**      | Time-series       | Fraud detection, machine failures |
| **Recommendation Systems** | Product/user data | Personalized product suggestions  |
| **Forecasting**            | Time-series       | Weather, stock market trends      |

---

## 📘 **Quick Recap**

| Concept           | Key Idea                                         |
| ----------------- | ------------------------------------------------ |
| **AI**            | Machines imitating human intelligence            |
| **AGI**           | Human-level understanding and reasoning          |
| **ML**            | Algorithms learning from data                    |
| **DL**            | Neural networks learning complex patterns        |
| **Generative AI** | Models that create new data (text, image, sound) |

---

## 🎯 **End of Module Outcomes**

You can now:
✅ Explain AI fundamentals
✅ Identify key AI domains & their tasks
✅ Understand how text, audio, and image data are processed
✅ Recognize popular AI model architectures
✅ Differentiate between AI, ML, and DL in context

---

## 🧠 OCI AI Services Overview

Oracle Cloud Infrastructure (OCI) provides multiple AI services for vision and language tasks.
Let’s explore the two main ones covered in this lesson:

---

### 📸 **1. Vision AI Service**

The **OCI Vision AI Service** allows you to perform the following tasks:

* 🏷 **Image Classification**
* 🔲 **Object Detection**
* ✍️ **Text Detection (OCR)**
* 📄 **Document AI**

#### 🖼 Image Classification

* Upload an image → the model analyzes it and assigns **labels** with **confidence scores**.
  Example:

  * Image of greenery → labels like *vegetation (99.23%)*
  * Image of a zebra → labels such as *zebra, vegetation, grassland, mammal*
  * Multiple zebras → detects both animals with appropriate confidence.

#### 🎯 Object Detection

* Identifies **objects within an image** and draws **bounding boxes** around them.
  Examples:

  * Traffic image → detects *cars, taxis, people* with confidence scores.
  * Fruit basket → detects *oranges, bananas, apples, bowls*, etc.

#### 🔍 Text Detection

* Extracts text from images (Optical Character Recognition).
  Examples:

  * Bus image → extracts text like *M32HOD*, *45*, and other writings.
  * Text with different fonts → reads text line-by-line and identifies fonts accurately.

#### 📑 Document AI

> Now moved under a new service called **Document Understanding**, but functionality remains the same.

**Features:**

* Extracts:

  * 🧾 **Raw text** (full content)
  * 🔑 **Key-Value pairs** (e.g., *Date, Subtotal, Total, Transaction Time*)
  * 📊 **Tables** (line items, totals, authorization codes, etc.)
* Example: Receipt image → detects all details like totals, taxes, and transaction data.

---

### 💬 **2. AI Language Service**

Provides two key capabilities:

1. **Text Analysis**
2. **Text Translation**

#### 🧩 Text Analysis

Applies **pretrained NLP models** on text blocks to extract multiple insights.

**Tasks:**

* 🌍 **Language Detection** → e.g., identifies text language as *English*.
* 🏷 **Text Classification** → categorizes text (e.g., *Science and Technology*).
* 🧠 **Entity Extraction** → detects items like *products, events, instruments*, etc., with confidence scores.
* 🗝 **Key Phrase Extraction** → identifies phrases such as *“early computers”*.
* 😀 **Sentiment Analysis** → includes:

  * Aspect-based sentiment (per topic)
  * Sentence-level sentiment (positive, negative, or neutral)
* 🔐 **PII Detection** → detects sensitive data like *dates, names, historical events*.

#### 🌐 Text Translation

* Supports translation between **multiple languages**.
* Example:

  * Source: English → Target: French, Japanese, etc.
  * Fast translation within seconds.
* Also supports **custom model training** if you provide your own translation data.

---

### 🏁 Summary

| Service         | Core Features                                            | Example Use                                     |
| --------------- | -------------------------------------------------------- | ----------------------------------------------- |
| **Vision AI**   | Image classification, object detection, OCR, Document AI | Analyze images, detect objects, extract text    |
| **AI Language** | Text analysis, translation, custom models                | Analyze or translate text in multiple languages |

---

### 📘 Key Takeaways

* OCI Vision AI → best for **image-based** automation.
* OCI AI Language → best for **text-based** analysis and translation.
* Both services support **confidence scores**, **custom training**, and **pretrained models** for quick deployment.

---

## 🤖**Module: AI vs ML vs DL**

### 🎯 Objective

Understand the relationship and key differences between **Artificial Intelligence (AI)**, **Machine Learning (ML)**, and **Deep Learning (DL)** with simple examples and use cases.

---

## 🧠 1. Artificial Intelligence (AI)

### 📘 Definition

AI refers to the **broad concept** of creating machines or systems that can perform tasks that typically require **human intelligence** — such as reasoning, learning, problem-solving, and decision-making.

### 💡 Example

A **self-driving car** that:

* Navigates traffic
* Detects pedestrians
* Makes safe lane changes

➡️ AI allows the car to **mimic human decision-making**.

---

## 📊 2. Machine Learning (ML)

### 📘 Definition

ML is a **subset of AI** focused on developing **algorithms that enable systems to learn from data** and make predictions or decisions **without explicit programming**.

### 💡 Example

A **spam email filter** that:

* Learns from user behavior and email content
* Identifies and moves spam emails automatically

### 🧮 Key Concept: Algorithm

An **algorithm** is a set of mathematical rules or procedures that:

* Allows models to learn from data
* Improves predictions over time

---

## 🧩 3. Deep Learning (DL)

### 📘 Definition

DL is a **subset of ML** that uses **neural networks with multiple layers** (deep neural networks) to learn complex patterns from large datasets.

### 💡 Example

An **image recognition system** that:

* Identifies animals or objects in photos
* Learns features directly from raw pixels

➡️ Example: Detecting whether an image contains a **cat or a dog**.

---

## 🧭 4. Types of Machine Learning

| Type                       | Description                                                       | Example                                       |
| -------------------------- | ----------------------------------------------------------------- | --------------------------------------------- |
| **Supervised Learning**    | Learns from **labeled data** (input-output pairs).                | Credit card approval prediction               |
| **Unsupervised Learning**  | Finds **hidden patterns or clusters** in **unlabeled data**.      | Customer segmentation for marketing           |
| **Reinforcement Learning** | Learns through **trial and error** with **rewards or penalties**. | Training an autonomous robot or playing chess |

---

## 🧮 Supervised Learning – Example

### 📍 Scenario: Credit Card Approval

Steps:

1. Collect past approval data (applications, scores, outcomes)
2. Train a model using this labeled data
3. Model learns rules automatically instead of manual programming
4. Predicts whether a **new application** should be approved

#### ⚙️ Process

* **Input:** Historical labeled data (Approved / Rejected)
* **Algorithm:** Learns patterns from data samples
* **Output:** Predicts outcome for new applications

✅ **Key Point:** Model learns from labeled examples → *Supervised Learning.*

---

## 🔍 Unsupervised Learning – Example

### 📍 Scenario 1: Retail Marketing

* Input data: household size, income, location, occupation
* Algorithm: groups customers into clusters
  → e.g., *High Spenders*, *Small Families*, etc.
* Use: Personalized marketing & sales strategies

### 📍 Scenario 2: Nutritional Clustering

* Input: nutritional values of fruits & vegetables
* Output: clusters of nutritionally similar items
  ➡️ Helps plan balanced diets.

✅ **Key Point:** Finds hidden structures without labels → *Unsupervised Learning.*

---

## 🎮 Reinforcement Learning – Example

### 📍 Scenario: Learning to Play Chess

* The agent (player) takes actions (moves)
* Receives feedback (win, lose, draw)
* Learns strategy via **trial and error**

➡️ Used in **robotics** and **autonomous vehicles**.

✅ **Key Point:** Learning through interaction with an environment → *Reinforcement Learning.*

---

## 🧠 Deep Learning in Detail

### 🔹 Core Idea

* Uses **neural networks** (layers of artificial neurons)
* Automatically extracts features from raw data
* Excellent for **images, audio, and natural language**

### 📷 Example

Can’t identify cats/dogs from a single pixel —
but deep networks can learn complex features (like fur, ears, shape) automatically.

### 🧱 Neural Networks

* Inspired by biological neurons
* Layers of connected nodes process data
* Learns mappings between inputs and outputs
  ➡️ Example of **supervised learning** used for **functional approximation**.

---

## 🎨 Generative AI

### 📘 Definition

A **subset of Machine Learning** focused on **creating new content** (text, audio, image, video, etc.) by learning from existing data patterns.

### 💡 Example

* **ChatGPT** generates text-based responses by learning patterns in human language.
* **AI image generators** create new artwork from text prompts.

### ⚙️ Applications

* Text generation
* Image synthesis
* Music and video creation
* Code generation

---

## 🧾 Summary Table

| Concept           | Definition                            | Example           | Relationship                 |
| ----------------- | ------------------------------------- | ----------------- | ---------------------------- |
| **AI**            | Machines performing intelligent tasks | Self-driving car  | Broadest field               |
| **ML**            | Learning from data to make decisions  | Spam filter       | Subset of AI                 |
| **DL**            | Neural networks with many layers      | Image recognition | Subset of ML                 |
| **Generative AI** | Creating new data/content             | ChatGPT, DALL·E   | Specialized area under ML/DL |

---

## 📘 Key Takeaways

* **AI** → Big umbrella (goal: simulate human intelligence)
* **ML** → Teaches systems to learn from data
* **DL** → Uses neural networks for complex pattern learning
* **Generative AI** → Creates *new* data, not just analyzes existing ones

---



