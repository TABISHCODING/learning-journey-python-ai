

---

## 🎓 **Module: OCI Generative AI Services**

### 🧩 **Lesson Overview**

This lesson covers:

1. Overview of OCI Generative AI service
2. Key characteristics: **pre-trained foundational models**, **flexible fine-tuning**, **dedicated AI clusters**
3. Use cases and capabilities
4. Demonstration of model types and customization

---

## 🧠 **1. OCI Generative AI Service Overview**

* **Fully managed service** for building **Generative AI applications**
* Provides **single API access** → easily switch between different foundational models with minimal code changes
* **Serverless** → no infrastructure to manage

**Key Features:**

1. Pre-trained foundational models
2. Flexible fine-tuning
3. Dedicated AI clusters

**How it works:**

* Provide **text input** (prompt) → service generates response
* Supports additional text input like **documents, emails, product reviews**
* Capable of **reasoning, generating, and processing human language at scale**

**Example Use Cases:**

* Chat / dialogue
* Text generation
* Information retrieval
* Semantic search

---

## 🧩 **2. Pre-Trained Foundational Models**

### **2.1 Chat Models**

| Model                | Provider | Token Limit                       | Use Case                               |
| -------------------- | -------- | --------------------------------- | -------------------------------------- |
| Command-R            | Cohere   | 16,000                            | Entry-level chat applications          |
| Command-R Plus       | Cohere   | 128,000                           | Advanced chat with high request volume |
| LLaMA 3 70B Instruct | Meta     | Large-scale instruction-following | Complex instruction-based tasks        |

**Characteristics:**

* Maintain **context of previous prompts** → continue conversations
* **Instruction-tuned models** → follow human instructions (e.g., summarize text, generate email)

### **2.2 Embedding Models**

| Model              | Description                        | Languages Supported |
| ------------------ | ---------------------------------- | ------------------- |
| Embed English      | Converts text to vector embeddings | English             |
| Embed Multilingual | Converts text to vector embeddings | 100+ languages      |

**Use Cases:**

* **Semantic search:** meaning-based search rather than keyword-based
* **Cross-language search:** query in one language, search documents in another

---

## 🧩 **3. Flexible Fine-Tuning**

* **Purpose:** Customize pre-trained models for **domain-specific tasks**
* **Benefits:**

  * Improve model performance on specific tasks
  * Increase efficiency for your use case

**Fine-Tuning Methods:**

* **Vanilla fine-tuning:** update most or all layers → expensive & time-consuming
* **T-Few fine-tuning:**

  * Inserts new layers into base model
  * Updates only a fraction of model weights
  * **Faster, cheaper, and efficient customization**

**When to Use:**

* Pre-trained model doesn’t perform well on your domain
* You want to **teach the model new knowledge**

---

## 🧩 **4. Dedicated AI Clusters**

* GPU-based compute resources for **fine-tuning and inference workloads**
* Features:

  * **Dedicated GPU pools** → isolated for security
  * **Exclusive RDMA networking** → ultra low latency for large clusters
  * Enables **scalable AI infrastructure** for heavy generative AI workloads

---

## 🏁 **Key Takeaways**

1. OCI Generative AI service = **pre-trained models + flexible fine-tuning + dedicated AI clusters**
2. **Single API access** allows easy integration and experimentation
3. **Chat models** → conversational AI with instruction-following
4. **Embedding models** → semantic search & multilingual applications
5. **T-Few fine-tuning** → efficient customization of large models
6. **Dedicated clusters** → secure, low-latency GPU infrastructure for high-performance AI

---


---

## 🎓 **OCI Generative AI Service – Demo Overview**

### 🧩 **1. Getting Started**

* Logged into **OCI Console** (Demo in Germany Central, Frankfurt region)
* **Service availability:** Generative AI is available in select regions (e.g., Frankfurt)
* Navigation:
  `Burger Menu → Analytics & AI → AI Services → Generative AI`

**Dashboard Features:**

1. **Service Tools** → tutorials and videos
2. **Documentation** → API endpoints, model info
3. **Playground** → visual interface to test models **without code**
4. **Dedicated AI Clusters** → GPU resources for fine-tuning & hosting models
5. **Custom Models** → fine-tuned models
6. **Endpoints** → hosting inference traffic

---

### 🧩 **2. Playground Walkthrough**

**Playground Purpose:**

* Explore **pretrained and custom models**
* Refine prompts and parameters
* View generated **integration code** (Python/Java)

**Model Classes:**

1. **Chat Models**

   * `Command-R` → affordable, smaller token limit (16,000)
   * `Command-R Plus` → powerful, large token limit (128,000)
   * `Meta LLaMA 3 70B` → instruction-following, 8,000 tokens
   * **Chat context:** remembers previous prompts for follow-up queries

   **Interactive Features:**

   * **View Code:** auto-generated Python/Java code for integration
   * **Preamble override:** change model tone or behavior (e.g., pirate style)
   * **Temperature:** control randomness of output

2. **Embedding Models**

   * Converts text → numerical vectors
   * **Semantic search:** focuses on **meaning**, not just keywords
   * **Multilingual support:** 100+ languages
   * Example: HR Help Center articles → clustered based on semantic similarity

   **Key Insight:**

   * Vectors that are numerically close → semantically similar
   * Enables returning relevant results based on meaning (e.g., skills, vacation, timecard)

---

### 🧩 **3. Dedicated AI Clusters**

* **Purpose:** GPU-based compute for fine-tuning & inference
* **Creation Steps:**

  1. Click **Create Dedicated AI Cluster**
  2. Provide name & select purpose: hosting or fine-tuning
  3. Choose **pretrained base model**
  4. Create cluster → ready for AI tasks

---

### 🧩 **4. Fine-Tuning Custom Models**

* **Steps to create a custom model:**

  1. Click **Create Model**
  2. Provide name → select **base model**
  3. Select **fine-tune method** (e.g., T-Few)
  4. Assign **dedicated AI cluster** (required for GPU compute)
  5. Execute fine-tuning → generates **custom model**

---

### 🧩 **5. Creating Endpoints**

* Purpose: serve production inference traffic from fine-tuned models
* Steps:

  1. Click **Create Endpoint**
  2. Provide name & hosting configuration
  3. Select **fine-tuned model** & dedicated AI cluster
  4. Endpoint ready → handle inference requests

---

### 🏁 **Key Takeaways from Demo**

1. **Playground**: test models and generate integration code
2. **Chat Models**: conversational, context-aware, instruction-following
3. **Embedding Models**: semantic clustering, multilingual support
4. **Dedicated AI Clusters**: secure, GPU-powered compute
5. **Fine-tuning**: custom models for domain-specific needs
6. **Endpoints**: easily deploy fine-tuned models for production

---

---

## 🎓 **Oracle Database 23ai – AI Vector Search & Select AI**

### 🧩 **1. AI Vector Search**

**Overview:**

* Built-in vector search capabilities within Oracle Database 23ai
* Supports **structured and unstructured data** (JSON, XML, graph, spatial, text, relational, vectors)
* Powers **generative AI pipelines** with your enterprise data

**Key Features:**

1. **Database-native vector embeddings**

   * `VECTOR` datatype to store embeddings
   * SQL functions for **similarity search** (`VECTOR_EMBEDDING`, `VECTOR_DISTANCE`)
2. **Model Integration**

   * Load ONNX models (e.g., `resnet_50`) for vector generation
   * Supports querying images, text, or other embeddings
3. **Vector Search in SQL**

   * Integrate embeddings into queries to find top matches
   * Works seamlessly with **joins** for normalized enterprise data
4. **Vector Indexes**

   * Improve performance and control accuracy
   * `TARGET ACCURACY` clause for approximate search
   * Options for **in-memory** (INMEMORY NEIGHBOR GRAPH) or partitions (NEIGHBOR PARTITIONS)

**Use Case Example:**

* Match candidate resumes to job positions based on preferred cities using **five lines of SQL**
* Combine relational, document, and vector data in a single query

**Gen AI Integration:**

* Embeddings + AI Vector Search → fully process **Gen AI pipelines**
* Integrates with frameworks like **LangChain** and **LlamaIndex**
* Enables semantic search, summarization, and RAG-style applications

---

### 🧩 **2. Select AI – Natural Language Queries**

**Overview:**

* Allows **natural language queries** against Oracle Autonomous Database
* Leverages LLMs to **translate questions into SQL**
* No need to know table structure or SQL syntax

**Key Features:**

1. **Query Generation**

   * Input question in plain English → Select AI generates SQL
   * Example: “Top 10 streamed movies” → SQL executed and results returned
2. **Integration with Apps**

   * Works with **APEX apps**, interactive reports, and dashboards
   * Can refine queries iteratively using natural language
3. **Pluggability**

   * Use OCI Generative AI, Cohere, OpenAI, or Llama models
   * Configure **AI profiles** to define schemas, tables, and models
4. **Security & Compliance**

   * Data remains in your tenancy
   * No data exposure to external LLMs

**Workflow Example:**

1. Ask natural language question → “Top customer segments for George Clooney movies”
2. AI profile constructs prompt using database metadata
3. LLM generates SQL → executed in database → results returned to app or SQL tool

**Benefits:**

* Simplifies app development with AI-powered insights
* Enables **enterprise-grade, secure, and scalable AI queries**
* Future-ready for **new or fine-tuned models**

---

### 🏁 **Key Takeaways**

* **AI Vector Search**: Semantic similarity search, embeddings, SQL integration, enterprise-ready
* **Select AI**: Natural language to SQL, pluggable LLMs, secure & app-integrated
* Both work seamlessly in Oracle Database 23ai to **power Gen AI pipelines**
* Supports relational, document, and vector data in **one converged solution**

---






