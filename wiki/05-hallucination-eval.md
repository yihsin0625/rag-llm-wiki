# 05. 幻覺抑制（Grounding）與基礎評估
- **Ingest 來源**：Source 5 — RAGAS *Automated Evaluation of Retrieval Augmented Generation* 技術白皮書
- **為什麼 RAG 仍可能出錯**：常見原因包含「檢索階段沒撈到正確段落（Retrieval Failure）」或「模型忽略參考資料自行發揮（Generation Hallucination）」。
- **新手必知的兩個核心評估指標（RAGAS 基礎）**：
  - **忠實度（Faithfulness）**：生成的答案是否完全忠於檢索出來的參考資料，沒有無中生有？
  - **答案相關性（Answer Relevance）**：生成的答案是否有正面回應使用者的問題？
- **關聯筆記**：完整流程回顧請見 [[01-rag-overview]]。
