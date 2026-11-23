# 04. 提示詞增強（Prompt Augmentation）
- **Ingest 來源**：Source 4 — Anthropic / Google *Prompt Engineering & Grounding* 官方指南
- **核心任務**：將「使用者原始問題」與「[[03-embedding-vectordb]] 撈回的 Top-K 文件片段」組裝成結構化 Prompt。
- **標準 System Prompt 模板要素**：
  1. **角色與邊界限制**：明確要求模型「僅根據以下提供的參考資料回答」。
  2. **拒答機制（Fallback）**：若參考資料中找不到答案，必須回答「根據現有資料無法確認」，禁止自行猜測。
  3. **來源標註要求**：要求模型在句末標註引用自哪一個文件片段（例如 `[來源 1]`）。
- **關聯筆記**：此設計直接決定 [[05-hallucination-eval]] 中的幻覺抑制效果。
