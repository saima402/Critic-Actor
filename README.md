
**Critic-Actor Framework for Lexical Ambiguity Resolution in Large Language Models:** 

This repository contains the implementation of our proposed Critic-Actor framework for lexical ambiguity detection and resolution in Large Language Models (LLMs).
The framework is designed to identify lexically ambiguous user queries and iteratively rewrite them into clearer, semantically equivalent queries before they are processed by LLMs.

The proposed framework consists of two components:

**1. Actor LLM**
Detects whether a query is lexically ambiguous and produces an ambiguity label and lastly estimates confidence.

**2. Critic LLM**
Rewrites ambiguous queries and preserves the original semantic intent and lastly returns a confidence score for the rewritten query.

**Features**

- Semantic query rewriting using LLMs via the Groq API.
- Semantic similarity evaluation using Sentence Transformers.
- Automatic computation of:
  - Average Semantic Similarity (ASS)
  - Rewrite Accuracy (RA)
  - Average Rewrite Confidence (ARC)
  - Rewrite Failure Rate (RFR)
- Export of rewritten queries and evaluation results to Excel.


**Requirements**

- Python 3.10+

- Install dependencies:

- pip install groq pandas openpyxl sentence-transformers scikit-learn


**Embedding Model**

- all-MiniLM-L6-v2
- Used for semantic similarity computation.

 

**Running the Notebook**

1. Obtain a Groq API key.
2. Replace
python
os.environ["GROQ_API_KEY"] = "YOUR_API_KEY"

with your own API key.

3. Run the notebook.
4. Upload the Excel file of dataset.
5. The notebook rewrites ambiguous queries and exports the final results.
