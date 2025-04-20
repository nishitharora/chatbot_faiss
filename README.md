# 🧠 Nutrient Information Chatbot

This project is a Question-Answering (QA) chatbot built using the [Haystack](https://haystack.deepset.ai/) framework. It answers natural language questions about nutrients based on a structured dataset. It uses a combination of FAISS for semantic search and a pre-trained language model for extractive QA.

FAISS (Facebook AI Similarity Search) is a library used for efficient similarity search, which is essential for retrieval-based models.


## 📁 Project Structure

## 🧩 How It Works

1. **Load Dataset**  
   The script reads a CSV file containing nutrient data (`Nutrient`, `%`, and optional `Category` columns).

2. **Create Haystack Documents**  
   Each row is converted into a structured document with metadata.

3. **Semantic Search with FAISS**  
   FAISS is used to store and search documents based on vector embeddings generated using `all-MiniLM-L6-v2`.

4. **Extractive QA with FARMReader**  
   The pipeline uses `deepset/roberta-base-squad2` to extract answers from the most relevant documents.

5. **Interactive Chatbot**  
   A terminal-based interface allows users to ask questions like:
   - *"What is the percentage of Vitamin C?"*
   - *"Tell me about iron."*

🧹 Cleanup
The FAISS index files are deleted after each run by default. If you'd like to persist the index, you can comment out the cleanup lines at the end of nutrient_chatbot.py.



📄 License
This project is open-source and available under the MIT License.

Made with 💡 by Nishith Arora







