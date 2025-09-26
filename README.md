# AI Powered Market Intelligence

This project allows you to upload your dataset, generate insights and recommendations, and interactively query your data using AI.

## Dataset

- **Source:** Google Play Store
- **Raw Data:** `googleplaystore.csv`
- **Cleaned Data:** `cleaned_googleplaystore.csv`  
  The cleaning and formatting steps are documented in [googleStoreData.ipynb](googleStoreData.ipynb)
  For a summary of changes made to the dataset, do refer to [datasetCleaning.md](datasetCleaning.md).


## RAG Pipeline

We use a Retrieval-Augmented Generation (RAG) pipeline with:
- HuggingFace embeddings
- Gemini LLM
- FAISS vector store
- The cleaned dataset: `cleaned_googleplaystore.csv`

### Outputs

- **Insights:** [app_insights.json](app_insights.json)
- **Recommendations:** [recommendations.json](recommendations.json)

The main code for generating these outputs is in [insights.ipynb](insights.ipynb) and [insights.py](insights.py). 
For the best experience, run [insights.ipynb](insights.ipynb).

## Chatbot

You can query the insights or dataset using a chatbot, also built with the RAG pipeline.  
See [chatSystem.ipynb](chatSystem.ipynb) (recommended) or [chatsystem.py](chatsystem.py) for implementation.