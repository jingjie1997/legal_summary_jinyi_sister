# 惡意散布不實資訊事件｜法律爭點與求償整理

單頁靜態網站，整理一起「向 Cosplay 比賽主辦方散布不實通緝犯資訊與個資」事件所涉及的刑事責任、民事求償方式，以及對造為未成年人時的特殊處理程序。另附一份民事起訴狀範本供下載。

> 內容為一般法律資訊整理，非正式法律意見；實際個案請諮詢執業律師。

## 技術棧

| 項目 | 使用 |
| --- | --- |
| 標記語言 | HTML5（單一檔案 `legal_summary_jinyi_sister.html`） |
| 樣式 | 原生 CSS，內嵌於 `<style>`；CSS 變數管理配色、Flexbox + Grid 版面、`@media` RWD 斷點 |
| JavaScript | 無 |
| 字型 | 系統字型堆疊（Noto Sans/Serif TC、PingFang TC、Microsoft JhengHei 等），無外部字型載入 |
| 建置工具 | 無，不需編譯 |
| 相依套件 | 無 |
| 部署 | GitHub Pages（`.nojekyll` 關閉 Jekyll 處理，靜態檔案原樣提供） |
| 語系 | 正體中文（`lang="zh-Hant"`、UTF-8） |

## 檔案結構

```
.
├── legal_summary_jinyi_sister.html   # 主頁面（結構 + 樣式全部內嵌）
├── 民事起訴狀_範本.docx              # 起訴狀範本，頁面內提供下載
├── .nojekyll                         # 停用 GitHub Pages 的 Jekyll 建置
└── README.md
```

頁面「相關文件」區塊以相對路徑連結 `.docx`，並帶 `download` 屬性，點擊即直接下載。兩個檔案須置於同一層。

## 本機預覽

直接以瀏覽器開啟 `legal_summary_jinyi_sister.html` 即可；或起一個簡易伺服器：

```bash
python -m http.server 8000
# 開啟 http://localhost:8000/legal_summary_jinyi_sister.html
```

## 部署（GitHub Pages）

```bash
git init
git add .
git commit -m "Add legal summary page and complaint template"
git branch -M main
git remote add origin https://github.com/<帳號>/<repo>.git
git push -u origin main
```

接著於 repo 的 **Settings → Pages → Source** 選 `Deploy from a branch`，分支 `main`、資料夾 `/ (root)`，等候部署完成。

網址：`https://<帳號>.github.io/<repo>/legal_summary_jinyi_sister.html`
