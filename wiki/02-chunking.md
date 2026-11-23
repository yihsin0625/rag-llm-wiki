# 02. 文本切分（Chunking）策略
- **Ingest 來源**：Source 2 — LangChain / LlamaIndex *Text Splitting & Chunking Strategies* 技術文件
- **為什麼需要切分**：原始文件（如 PDF 手冊）動輒數萬字，直接塞入 LLM 會超出 Context Window 限制，且雜訊過多會稀釋檢索精準度。
- **常見切分方式**：
  - **固定字元/Token 切分（Fixed-size Chunking）**：例如每 500 字切一塊，實作簡單但可能切斷完整句子。
  - **遞迴字元切分（Recursive Character Splitting）**：優先依照段落（`\n\n`）、換行（`\n`）、句號切分，保留語意完整性。
- **關鍵參數 Chunk Overlap（重疊視窗）**：相鄰兩塊保留 10%～20% 重疊內容（例如 500 字搭配 50 字重疊），避免關鍵上下文剛好在切分邊界被切斷。
- **關聯筆記**：切分後的片段將進入 [[03-embedding-vectordb]] 進行向量化。
