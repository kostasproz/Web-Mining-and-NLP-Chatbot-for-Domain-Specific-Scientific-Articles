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

## ⚙️ Installation & Setup  

This project uses **Python 3.10+**.  

### 1. Clone the Repository  
```bash
git clone https://github.com/your-username/scientific-rag-chatbot.git
cd scientific-rag-chatbot
