# 🔬🤖 Scientific RAG Chatbot with Web Mining  

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)  
![Jupyter](https://img.shields.io/badge/Notebook-Jupyter-orange)  
![Libraries](https://img.shields.io/badge/Libraries-BeautifulSoup4%2C%20scikit--learn%2C%20transformers%2C%20gensim%2C%20NLTK%2C%20SpaCy-green)  

## 📌 Project Overview  
This project developed a **Retrieval-Augmented Generation (RAG) chatbot** built on a custom knowledge base of scientific articles. The pipeline began with **ethical web mining** of over 60 articles from *ScienceDaily*, followed by **preprocessing** and **LDA topic modeling** to extract key themes. The final chatbot integrates **document retrieval (TF-IDF)** with **generative AI (GPT-2)** to provide context-grounded, domain-specific answers.  

---

## 🚀 Key Features  
- **End-to-End Data Pipeline** → From data acquisition (web mining) to deployment (interactive chatbot).  
- **Topic Analysis** → Uses *Latent Dirichlet Allocation (LDA)* with pyLDAvis visualization.  
- **RAG Architecture** → Two-step system: retrieve relevant text, then generate fact-grounded responses.  
- **Interactive CLI** → Users can query the knowledge base directly in the terminal.  

---

## 🛠️ Techniques & Tools  

| Category            | Technique                         | Library/Model                  | Description |
|---------------------|-----------------------------------|--------------------------------|-------------|
| **Web Mining**      | Web Scraping + Ethical Delays     | Beautiful Soup, Requests       | Collected article text and links from ScienceDaily. |
| **NLP Preprocessing** | Tokenization, Stopword Removal   | NLTK, SpaCy                    | Cleaned and prepared raw text for modeling. |
| **Feature Engineering** | TF-IDF Vectorization            | Scikit-learn (TfidfVectorizer) | Transformed documents into semantic vectors for retrieval. |
| **Unsupervised Learning** | Topic Modeling                 | Gensim (LDA), pyLDAvis         | Extracted hidden themes from the article corpus. |
| **Generative AI**   | Retrieval-Augmented Generation    | Hugging Face Transformers (GPT-2) | Combined retrieved context with a generative model for Q&A. |

---
📊 **Results & Insights**

- **Corpus Summary:** ~60 articles from *ScienceDaily* across topics like AI, medicine, and climate science.  
- **Topic Modeling Output:** LDA revealed 5 dominant themes (e.g., *AI & Ethics*, *Medical Research*, *Environmental Studies*).  
- **Chatbot Accuracy:** Responses are contextually grounded to retrieved documents, reducing hallucinations vs standalone GPT-2.  
- **Visualization:** *pyLDAvis* dashboard provides interactive exploration of topic clusters.

---

💬 **Example Queries**

| User Query | Example Response |
|---|---|
| “How is AI used in medicine?” | “According to a *ScienceDaily* article, AI models assist in detecting disease patterns and improving diagnostic accuracy…” |
| “What are recent discoveries about climate change?” | “The retrieved articles discuss melting ice rates and carbon monitoring innovations published in 2024…” |

---

🧩 **Project Architecture**

1. **Data Collection:** Ethical web mining using `requests` + `BeautifulSoup` with delay timers to respect server policies.  
2. **Text Preprocessing:** Lemmatization, token filtering, and stopword removal with `NLTK` and `SpaCy`.  
3. **Vectorization & Topic Modeling:** TF-IDF and LDA (via `Gensim`) to extract latent topics and semantic structures.  
4. **Retrieval System:** TF-IDF similarity search to rank and retrieve most relevant text chunks.  
5. **Generation System:** GPT-2 model fine-tuned on domain-specific data to produce context-aware responses.  
6. **Chatbot Interface:** Command-line interface allowing dynamic user interaction and retrieval-augmented generation.

---

📈 **Future Improvements**

- Integrate **FAISS** or **BM25** for faster, more accurate document retrieval.  
- Replace GPT-2 with **Llama 3** or **Flan-T5** for higher factual consistency.  
- Add a **Streamlit** web interface for user-friendly interaction.  
- Expand dataset to **multiple scientific sources** for broader domain coverage.

---
