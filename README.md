# RAGInRecruitement
This project demonstrates a simple AI-driven job description and resume matching system using Llama-2-7b, GPT-J embeddings, FAISS, and SageMaker.

# Notebook:
 
Features:

- Loads job descriptions and resumes from local directories.
- Uses GPT-J embeddings for generating vector representations of resumes and job descriptions.
- Implements FAISS for efficient similarity-based search.
- Generates context-aware responses using Llama-2-7b.

recruiter-assist-RAG.ipynb - Six key components

a. Document Loading and Splitting: Load resumes and job descriptions from local directories using DirectoryLoader, and split them into manageable chunks with RecursiveCharacterTextSplitter.

b. Embedding Generation: Use GPT-J 6B model (via Amazon SageMaker on instance ml.g4dn.2xlarge) to generate semantic embeddings for resumes and job descriptions.

c. FAISS Vector Store: Store embeddings in FAISS for fast similarity search and efficient retrieval.

d. Search and Retrieval: Generate query embeddings and retrieve the most relevant job descriptions and candidate resumes using FAISS.

e. Prompt Template: Create a template that feeds the retrieved context into the Llama-2-7b model for candidate-job fit analysis.

f. Deployment and Inference: Deploy Llama-2-7b through SageMaker JumpStart, send the prompt, and receive a candidate fitment recommendation or summary.


Make the following changes to have this notebook work on your document of interest 
  - Add your resume and job description files in the respective directories (`./resumes/` and `./job_descriptions/`). 

