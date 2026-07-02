# 團隊進度看板

線上網址：**https://haoagentuse-glitch.github.io/kanbanBoard-everyone_ignore-/**

- **工作分配.xlsx** — 唯一資料來源。7 人三週工作分配、甘特圖、人力配置。改進度就改這個，成員名單、職責、篩選標籤全部由這份 Excel 自動帶出（不寫死）。
- **index.html** — 一頁式看板。**甘特圖為主**（左），**右欄為對應 TODO 明細**（條列式）。點甘特任一列 ↔ 右欄明細會互相對應高亮。上方篩選標籤依「人力配置」分頁的成員自動產生。
- **.nojekyll** — 讓 GitHub Pages 原樣提供靜態檔（勿刪）。

## 本機使用

用瀏覽器開 `index.html` → 點右上「重新載入 Excel」選 `工作分配.xlsx`（file:// 需手選一次，會記住上次內容）。改 Excel 存檔後重新載入即同步。

## 部署 GitHub Pages（一次設定）

本資料夾即網站根目錄。設定：

1. 先把變更推上去：
   ```
   git add .
   git commit -m "update board: names data-driven + T07 schedule"
   git push origin main
   ```
2. GitHub 倉庫 → **Settings → Pages**。
3. **Build and deployment → Source** 選 **Deploy from a branch**。
4. Branch 選 **main**、資料夾選 **/(root)**，按 **Save**。
5. 等 1–2 分鐘，網址：
   **https://haoagentuse-glitch.github.io/kanbanBoard-everyone_ignore-/**

部署後（https 環境）頁面會**自動載入**同資料夾的 `工作分配.xlsx`，免手選。之後每次 `git push` 更新 xlsx，Pages 會自動重新發佈。

## 成員與分工

Nash 後端／基礎設施｜Arku 資料來源／爬蟲｜Timyo 向量化／去重｜MMJSUN LLM 摘要／分類｜Bright 評分／籌碼｜Jenny 前端／UX｜Haoche 統籌／merge／架構掌握

> 分工以「人力配置」分頁為準，此處僅為速覽；改 Excel 後看板自動同步。
