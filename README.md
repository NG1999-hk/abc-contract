# ABC 銷售合同生成器

純前端單檔網頁，用嚟快速生成英文銷售合同（香港法律），並直接輸出 Word `.docx`。

## 特點

- **免伺服器**：雙擊 `index.html` 即用，唔需要上網、唔需要 API key
- **合同正文英文**，**網站介面繁體中文**
- **輸出真 Word `.docx`**（用 OOXML 產生，唔係 HTML 改名）
- **日期用日曆揀**、**價錢只接受數字**、**「within X days」全部係輸入欄**
- **船務條款**：Incoterms（EXW / FCA / FOB / CFR / CIF / DAP / DDP / **FOC**）＋ 自動 7 條條文 ＋ FOC 專屬條文
- **資料只留喺瀏覽器**（localStorage），唔會上傳任何地方

## 檔案

```
index.html    ← 全部功能（單檔，約 819 行）
README.md     ← 本說明
docs/協作指引.md ← 兩人一齊編輯嘅步驟
```

## 本機使用

1. 雙擊 `index.html`（用 Chrome / Edge 開）
2. 填寫買賣雙方、貨品、金額、付款、交貨、船務條款
3. 按「下載 Word (.docx)」或「列印／存 PDF」

## 上線（Cloudflare Pages，免費）

1. 推上 GitHub（private repo 都可以）
2. Cloudflare Dashboard → Workers & Pages → Create → Pages → Connect to Git
3. 揀呢個 repo → Framework preset: **None** → Build command: **留空** → Output directory: **/**
4. Deploy → 網址會係 `https://<專案名>.pages.dev`

## 注意

- 合同內容法律責任由使用者自負；本工具唔構成法律意見
- 未填寫嘅欄位會顯示 `To be provided`，**唔會自動猜測內容**
