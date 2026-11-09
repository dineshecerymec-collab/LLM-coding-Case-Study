# README — Canada IMF Financial Stability Analysis

## Project Overview
This project develops an LLM-based analytical pipeline to extract, evaluate, and visualize economic and financial stability information from the IMF's *Canada: 2023 Article IV Consultation* (Country Report No. 23/286).

## Tools and Technologies
- **Language:** Python (Google Colab)
- **LLMs:** Gemini Flash Lite and Gemini Flash
- **PDF Processing:** PyMuPDF
- **RAG:** Sentence Transformers (all-MiniLM-L6-v2) and FAISS
- **Data Analysis:** Pandas and NumPy
- **Visualization:** Matplotlib

## Implementation
The project consists of four tasks and one optional extension:

1. **PDF Processing:** Text extraction, cleaning, token-based chunking, section summarization, and LLM evaluation.
2. **Financial Analysis:** Seven-theme classification, numerical indicator extraction, JSON validation, and identification of economic strengths and vulnerabilities.
3. **RAG:** Local semantic embeddings, FAISS retrieval, evidence-grounded question answering, and faithfulness evaluation.
4. **Dashboard:** Data transformation using `pd.melt()` and a four-panel financial stability dashboard.
5. **Extension:** Multi-Query RAG benchmarking against baseline retrieval.

## Key Results
- 23 sections summarized and evaluated.
- Six financial indicators successfully extracted.
- 287 evidence windows indexed using FAISS.
- Four-panel dashboard exported at 320 DPI.
- Multi-Query RAG improved completeness from 3.8/5 to 5.0/5, maintaining faithfulness at 5.0/5.

## Execution Instructions
1. Open the project notebook in Google Colab.
2. Upload the Canada IMF PDF and configure the `GEMINI_API_KEY` in Colab Secrets.
3. Run the notebook cells sequentially (maximum 15 cells).
4. Access the generated JSON files, evaluation results, visualizations, and FAISS index in `Canada_IMF_Outputs`.

## Output Files
The final archive, `Canada_IMF_Final_All_Tasks.zip`, contains the generated analytical outputs, dashboard figures, RAG results, and benchmark comparisons.

## Reference
International Monetary Fund (2023). *Canada: 2023 Article IV Consultation—Press Release and Staff Report*. IMF Country Report No. 23/286.
