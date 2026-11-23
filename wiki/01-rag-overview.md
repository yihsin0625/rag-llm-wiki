# 01. RAG 核心概念與三階段架構
- **Ingest 來源**：Source 1 — Lewis et al. (2020) *Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks* 導讀摘要
- **核心定義**：RAG（Retrieval-Augmented Generation，檢索增強生成）是一種結合「外部知識庫檢索」與「大型語言模型（LLM）生成」的架構。
- **生活化類比**：傳統 LLM 回答問題像**「閉書考試」**，只能憑訓練時的記憶作答，容易忘記或瞎編；RAG 則像**「開書考試」**，先翻閱指定參考書找到段落，再根據內容寫出答案。
- **三階段流程**：
  1. **索引（Indexing）**：將外部文件切分並轉為向量存入資料庫（詳見 [[02-chunking]]、[[03-embedding-vectordb]]）。
  2. **檢索（Retrieval）**：將使用者問題轉為向量，找出最相關的 $K$ 個文件片段。
  3. **生成（Generation）**：將問題與檢索到的片段組合成提示詞交給 LLM 生成回答（詳見 [[04-prompt-augmentation]]）。
