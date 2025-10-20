

---

## 🎓 **OCI Language & Speech Services**

### 🧩 **1. OCI Language – Text Analytics**

**Overview:**

* Analyzes **unstructured text** without requiring data science expertise
* Provides **pretrained models** for enterprise language analysis
* Supports **75 languages**

**Key Capabilities:**

1. **Language Detection** – Detects language of text with confidence score
2. **Named Entity Recognition (NER)** – Identifies 14 entity types:

   * Names, places, dates, emails, currency, organizations, phone numbers, etc.
3. **Sentiment Analysis**

   * Document-level: overall sentiment of the text
   * Aspect-based: sentiment per topic/aspect (e.g., “food positive, service negative”)
   * Sentence-level: sentiment per sentence (positive/neutral/negative)
4. **Key Phrase Extraction** – Extracts important phrases representing main ideas
5. **Text Classification** – Classifies text into **600+ categories/subcategories**

**Console Workflow:**

* Navigate: **Analytics & AI → AI Services → Language**
* Use **Text Analytics** to analyze default or custom text
* Output includes:

  * Language detected with confidence
  * Named entities with types and confidence scores
  * Key phrases
  * Sentiments at document, aspect, and sentence levels
  * Text classification

---

### 🧩 **2. OCI Speech – Speech-to-Text**

**Overview:**

* Converts **audio/video files to text** with high accuracy
* Uses Oracle’s **acoustic language models** and deep learning
* No data science experience required

**Key Capabilities:**

1. **Transcription**

   * Processes audio/video directly from **Object Storage**
   * Timestamped, grammatically accurate transcriptions
2. **Language Support** – English, Spanish, Portuguese (more coming)
3. **Batch Processing** – Multiple files per call, fast processing (hours of audio in <10 minutes)
4. **Confidence Scores** – Per word and per transcription
5. **Normalization** – Converts numbers, addresses, URLs, etc., into readable format
6. **Profanity Filtering** – Options to **remove, mask, or tag** profanity
7. **SRT Output** – Generates closed caption files for videos

**Console Workflow:**

* Navigate: **Analytics & AI → AI Services → Speech**
* Load audio/video into **Object Storage bucket**
* Create a **Transcription Job** specifying:

  * Compartment
  * Bucket & file
* Run job → results include:

  * Punctuated, normalized transcription
  * Multiple speaker recognition
  * Readable, ready-to-use text

**Use Case Example:**

* Transcribed a support conversation:

  * Speaker 1: “I’m having an issue with my wireless headphones…”
  * Speaker 2: “Hi, thanks for contacting support…”
* Output includes proper punctuation, normalization, and speaker separation

---

✅ **Key Takeaways:**

* **OCI Language**: Extract insights from text (entities, sentiment, key phrases, categories)
* **OCI Speech**: Convert audio/video to clean, readable text with timestamps and speaker info
* Both services **require no data science expertise** and integrate with **Oracle Cloud Object Storage**
* Can be used for **chatbots, call center analytics, content classification, subtitles, and more**

---


---

## 🎓 **OCI Vision – Image & Document AI**

### 🖼️ **1. Image Analysis**

**Overview:**

* OCI Vision analyzes **photographic images** for insights using **pretrained models** or **custom retrained models**
* Two main features: **Object Detection** and **Image Classification**

**Capabilities:**

1. **Object Detection**

   * Detects objects in images with **bounding boxes** and **accuracy percentage**
   * Can **detect text** in the scene (e.g., signs, license plates, logos)
   * Can identify **nested objects** (e.g., person on a bicycle)
   * Custom models can be trained to detect specialized objects not recognized by default

2. **Image Classification**

   * Assigns **classification labels** based on major features in the image
   * Can identify multiple elements in a scene (e.g., “skyscraper, water, building, bridge, boat”)
   * Works with default pretrained models or **custom-trained models**

**Console Workflow:**

* Navigate: **Analytics & AI → AI Services → Vision**
* Upload an image or use default images
* Choose **Image Classification** or **Object Detection**
* Review tags, bounding boxes, detected objects, and extracted text

---

### 📄 **2. Document AI**

**Overview:**

* Analyzes **document images** such as PDFs, JPEGs, PNGs, TIFFs, or photos of text
* Extracts structured information for **document understanding and automation**

**Capabilities:**

1. **Text Recognition (OCR)**

   * Extracts text, including **handwritten, tilted, shaded, or rotated documents**

2. **Document Classification**

   * Classifies documents into **10 types** (e.g., invoice, receipt, resume)
   * Uses **visual features** and **keywords**

3. **Language Detection**

   * Determines language based on **visual text features**

4. **Table Extraction**

   * Detects tables in documents and extracts content in **tabular form**

5. **Key-Value Extraction**

   * Extracts values for **common fields** (e.g., merchant name, transaction date, line items)

**Console Workflow:**

* Navigate: **Analytics & AI → AI Services → Vision → Document AI**
* Upload document image (receipt, invoice, etc.)
* Run **analysis** → outputs:

  * Extracted text (line-wise and word-wise)
  * Key values (merchant, date, line items)
  * Tabular data extraction

**Example Use Cases:**

* Receipt processing: Extract merchant info, date, line items for expense automation
* Invoice analysis: Extract quantities, descriptions, unit prices, totals, and handwritten/stamped info

---

✅ **Key Takeaways:**

* **OCI Vision Image Analysis:** Understands scene content, objects, and text in images
* **OCI Vision Document AI:** Extracts structured information from documents for automation
* Supports **pretrained models** and **custom retrained models**
* Integrates easily via **OCI Console** for quick prototyping and testing

---





Do you want me to do that next?
