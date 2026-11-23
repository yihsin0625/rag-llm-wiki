# 03. 向量嵌入（Embedding）與向量資料庫
- **Ingest 來源**：Source 3 — HuggingFace & Pinecone *What are Vector Embeddings?* 入門指南
- **向量嵌入（Embedding）**：透過 Embedding 模型（如 `text-embedding-3-small` 或 `bge-m3`），將文字轉換成一串高維度數字陣列（向量），讓語意相近的句子在數學空間中距離更近。
- **關鍵字搜尋 vs 語意搜尋**：
  - 傳統關鍵字搜尋（BM25）：「手機沒電」找不到「行動電話耗盡電力」（字面不同）。
  - 向量語意搜尋：兩者向量夾角極小（餘弦相似度 Cosine Similarity 高），能精準命中。
- **向量資料庫（Vector DB）**：專門儲存向量並提供高速近似最近鄰搜尋（ANN）的工具，如 Chroma、FAISS、Pinecone、Qdrant。
- **關聯筆記**：前置步驟為 [[02-chunking]]，檢索結果將傳遞至 [[04-prompt-augmentation]]。
