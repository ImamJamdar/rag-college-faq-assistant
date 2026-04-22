# 🚀 RAG-Based College/University FAQ Assistant using LangGraph with Human-in-the-Loop (HITL)

## 📌 Overview

This project presents a **Retrieval-Augmented Generation (RAG)** based Customer Support Assistant designed to answer user queries using a PDF knowledge base. The system enhances traditional chatbot capabilities by combining **semantic search (retrieval)** with **LLM-based response generation**.

It also integrates:

* 🧠 **LangGraph** for workflow orchestration
* 🔁 **Conditional Routing Logic**
* 👨‍💻 **Human-in-the-Loop (HITL)** for reliability

---

## 🎯 Key Features

* 📄 Processes PDF knowledge base
* 🔍 Retrieves relevant information using embeddings
* 🤖 Generates context-aware answers using LLM
* 🔀 Uses LangGraph for dynamic workflow control
* 🚨 Escalates complex queries via HITL
* ⚡ Modular and scalable design

---

## 🏗️ System Architecture

The system consists of the following major components:

* **User Interface** – Accepts user queries
* **Document Loader** – Loads and processes PDF
* **Chunking Module** – Splits text into smaller chunks
* **Embedding Model** – Converts text into vectors
* **Vector Database (ChromaDB)** – Stores embeddings
* **Retriever** – Fetches relevant chunks
* **LLM (FLAN-T5)** – Generates responses
* **LangGraph Workflow Engine** – Controls execution
* **Routing Logic** – Decides AUTO vs HITL
* **HITL Module** – Handles complex queries

---

## 🔄 Workflow

1. User submits a query
2. Query is processed using LangGraph
3. Relevant chunks are retrieved from ChromaDB
4. Context is passed to the LLM
5. LLM generates a response
6. Routing logic evaluates confidence
7. If confidence is low → HITL triggered
8. Final response is returned to the user

---

## 🧠 Technologies Used

| Component   | Technology            |
| ----------- | --------------------- |
| Language    | Python                |
| LLM         | FLAN-T5 (HuggingFace) |
| Embeddings  | Sentence Transformers |
| Vector DB   | ChromaDB              |
| Framework   | LangChain + LangGraph |
| Environment | Google Colab          |

---

## 📂 Project Structure

```
RAG_Project/
│
├── RAG_LangGraph_Project.ipynb   # Main implementation
├── college_support.pdf           # Knowledge base
├── HLD_RAG_Project.pdf           # High-Level Design
├── LLD_RAG_Project.pdf           # Low-Level Design
├── Technical_Documentation.pdf   # Detailed documentation
└── README.md                     # Project overview
```

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the repository

```
git clone <your-repo-link>
cd RAG_Project
```

### 2️⃣ Install dependencies

```
pip install langchain langchain-community langgraph chromadb sentence-transformers transformers pypdf
```

### 3️⃣ Run the notebook

Open in Google Colab or Jupyter Notebook:

```
RAG_LangGraph_Project.ipynb
```

---

## ▶️ Usage

Example query:

```
What is minimum attendance?
```

Example output:

```
Students must maintain a minimum of 75% attendance.
```

---

## 🔀 Conditional Routing

The system uses confidence-based routing:

* ✅ **Auto Mode** → Direct response from LLM
* 🚨 **HITL Mode** → Escalation to human

---

## 👨‍💻 Human-in-the-Loop (HITL)

HITL is triggered when:

* Low confidence
* Missing context
* Complex query

It ensures:

* ✔ Higher accuracy
* ✔ Better reliability
* ✔ Improved user trust

---

## 🧪 Testing

The system is tested with:

* Normal queries
* Edge cases
* Unknown queries (HITL)

---

## ⚠️ Challenges & Trade-offs

* Accuracy vs Speed
* Chunk size vs Context
* Automation vs Reliability
* Cost vs Performance

---

## 🚀 Future Enhancements

* Multi-document support
* Conversational memory
* Real-time deployment
* Feedback learning system
* Advanced LLM integration

---

## 🏁 Conclusion

This project demonstrates how **RAG + LangGraph + HITL** can be combined to build an intelligent, scalable, and reliable AI system for real-world applications such as customer support.

⭐ If you found this project useful, consider giving it a star!

