# FinX – Loan Agreement Intelligence Using NLP

**Subject:** Natural Language Processing (NLP)
**Project Type:** NLP-Based Application
**GitHub Repository:** https://github.com/VishveshSharma2005/FinX-NLP

## 1. Introduction

FinX is an NLP-based application designed to help users understand complex loan agreements. Loan agreements often contain lengthy legal terms, prepayment conditions, penalties, lock-in periods, and other important information that may be difficult for borrowers to understand.

FinX allows users to upload a loan agreement in PDF or Word format and ask questions in natural language. The system retrieves relevant information from the document and generates answers supported by references to specific clauses, pages, or applicable RBI regulations.

The main objective of this project is to apply Natural Language Processing techniques to extract, process, retrieve, and understand information from financial and legal documents.

## 2. Problem Statement

Loan agreements contain large amounts of unstructured text, making it difficult for users to locate specific information quickly. Manually reading these documents is time-consuming, while general-purpose chatbots may provide inaccurate or unsupported answers.

Therefore, an NLP-based system is required to process loan documents, retrieve relevant information, and provide understandable answers with supporting evidence.

## 3. Objectives

* To process and extract text from PDF and Word documents.
* To apply text preprocessing and document segmentation techniques.
* To convert text into numerical representations for information retrieval.
* To retrieve relevant clauses based on user questions.
* To use pretrained language models for natural language question answering.
* To generate answers supported by document references.
* To deploy the application through a web interface and REST API.

## 4. NLP Concepts Used

### 4.1 Text Preprocessing

Text is extracted from uploaded documents and processed into smaller, meaningful units. Document parsing and clause segmentation help organize lengthy agreements into searchable sections.

Text normalization and cleaning can help prepare extracted content for subsequent NLP operations.

### 4.2 Text Vectorization and Embeddings

FinX uses **BGE-small embeddings** to represent text as numerical vectors. These representations help the system identify clauses that are semantically related to a user's question, even when the wording is different.

The project also uses **BM25**, a keyword-based retrieval technique, alongside semantic search to improve the retrieval of relevant information.

### 4.3 Semantic Search and Information Retrieval

When a user submits a question, FinX searches the indexed loan agreement and relevant regulatory documents to identify useful passages.

Hybrid retrieval combines keyword-based matching and semantic similarity. An applicability filter considers factors such as loan type, lender category, and effective date when selecting relevant regulatory information.

### 4.4 Pretrained Language Models

FinX supports the integration of a pretrained language model, NVIDIA Nemotron, to generate natural-language responses from retrieved evidence.

The language model receives relevant document passages and generates answers based on the available information. The application also supports a fallback mode when the external model is unavailable.

### 4.5 Text Generation and Question Answering

The application uses a Retrieval-Augmented Generation (RAG) approach.

In RAG, the system first retrieves relevant information from a document collection and then uses that information to generate an answer. This reduces reliance on the language model's general knowledge and makes responses more closely connected to the uploaded document.

### 4.6 Information Extraction and Citation Verification

FinX identifies relevant clauses and associates generated answers with supporting sources. A verification mechanism checks generated statements and numerical details against their cited evidence.

If sufficient supporting evidence is unavailable, the application can display an appropriate fallback response instead of presenting an unsupported answer as a fact.

## 5. Working of the System

The project follows these steps:

1. **Document Upload:** The user uploads a loan agreement in PDF or Word format.
2. **Text Extraction:** Text is extracted using document-parsing tools, with OCR support for scanned PDFs.
3. **Document Segmentation:** The extracted content is divided into individual clauses and sections.
4. **Vectorization and Indexing:** Text embeddings are generated, and searchable document indexes are created.
5. **Question Processing:** The user enters a question in natural language.
6. **Information Retrieval:** Hybrid search retrieves relevant clauses and regulatory passages.
7. **Answer Generation:** The system generates a response using the retrieved evidence and an optional pretrained language model.
8. **Answer Verification:** Citations and numerical claims are checked against the supporting sources.
9. **Response Display:** The user receives an answer with references or a fallback response when sufficient evidence is unavailable.

## 6. Technologies Used

| Technology        | Purpose                                                  |
| ----------------- | -------------------------------------------------------- |
| Python            | Core programming language                                |
| FastAPI           | Backend development and REST API                         |
| PyMuPDF           | PDF text extraction                                      |
| Tesseract OCR     | Text extraction from scanned documents                   |
| python-docx       | Word document processing                                 |
| BGE-small         | Text embeddings                                          |
| BM25              | Keyword-based information retrieval                      |
| NumPy and SQLite  | Vector operations and local indexing                     |
| NVIDIA Nemotron   | Optional pretrained language model for answer generation |
| Next.js and React | Web application interface                                |
| TypeScript        | Frontend development                                     |
| Pytest            | Software testing                                         |

## 7. Applications

* Understanding loan agreements.
* Finding prepayment conditions and penalties.
* Identifying lock-in periods and other important clauses.
* Searching financial and legal documents using natural language.
* Retrieving relevant regulatory information.
* Supporting document-based question answering.

## 8. Advantages

* Reduces the time required to search lengthy documents.
* Allows users to ask questions in natural language.
* Combines keyword matching with semantic search.
* Provides clause-level references for supporting evidence.
* Helps reduce unsupported or misleading answers through evidence verification.
* Supports both PDF and Word documents.
* Can operate locally without an external language model API key, using its built-in fallback mode.

## 9. Limitations and Future Scope

The accuracy of the system depends on document quality, retrieval performance, and the availability of relevant source material.

Future improvements may include:

* Sentiment analysis and document classification.
* Multilingual support for Hindi and Gujarati.
* Voice-based interaction.
* Automated loan-cost calculations.
* Improved retrieval using reranking models.
* Comparison of multiple loan agreements.
* Enhanced evaluation using larger document collections.

## 10. Conclusion

FinX demonstrates how Natural Language Processing can be applied to a practical financial problem. It combines document preprocessing, text embeddings, information retrieval, pretrained language models, and text generation to make loan agreements easier to understand.

The project shows how NLP techniques can transform unstructured text into useful information and support evidence-based decision-making. It also highlights the importance of source verification when applying language models to financial and legal documents.

## 11. References

1. Robertson, S. and Zaragoza, H. (2009). *The Probabilistic Relevance Framework: BM25 and Beyond.*
2. Devlin, J., Chang, M.-W., Lee, K. and Toutanova, K. (2019). *BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding.*
3. Lewis, P. et al. (2020). *Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks.*
4. Reimers, N. and Gurevych, I. (2019). *Sentence-BERT: Sentence Embeddings using Siamese BERT-Networks.*
5. Hugging Face Documentation: https://huggingface.co/docs
6. FastAPI Documentation: https://fastapi.tiangolo.com/
7. Project Repository: https://github.com/VishveshSharma2005/FinX-NLP
