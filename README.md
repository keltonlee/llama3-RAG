# llama3-RAG

## Approach
In this Retrieval-Augmented Generation (RAG) task, I used LangChain to implement the following steps:

1. Document the knowledge base data and set up an embedding model to facilitate data retrieval by the LLM.

2. Activate the Ollama server to use LLaMA 3.1.


3. Define a prompt template to regulate the LLM's responses.

4. Configure LangChain's RetrievalQA to enable the LLM to retrieve data from the knowledge base.

5. Implement a classification function that allows the LLM to perform N inferences and select the most frequent answer. The goal of this approach is to increase stability and improve accuracy.

## Results
<img width="771" alt="截圖 2024-09-09 下午11 51 10" src="https://github.com/user-attachments/assets/ca3e3469-9e03-473e-a450-ce01064947fb">

## Potential shortcomings
1. When the knowledge base data increases, it’s possible that the use of LangChain's CharacterTextSplitter for splitting the text may cause the LLM to fail in understanding the context within the knowledge base, leading to incorrect results.
   
2. The input query might contain some extra spaces, unusual characters, or strange grammar, which could prevent the LLM from producing an accurate inference result.

## Potential improvements and optimizations
1. Design an automated pipeline that dynamically adjusts the chunk and overlap size as the knowledge base data changes.

2. Perform preprocessing on the input query to remove abnormal spaces and symbols.

3. Optimize the LLM's prompt through prompt engineering techniques (e.g., expert prompting, few-shot inference, chain-of-thoughts, etc.).
