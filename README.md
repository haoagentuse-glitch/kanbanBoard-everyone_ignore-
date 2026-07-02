# 團隊進度看板（docs/ = GitHub Pages 網站根目錄）

- **工作分配.xlsx** — 唯一資料來源。7 人（A–G）三週工作分配、甘特圖、人力配置。改進度就改這個。
- **index.html** — 一頁式看板。**甘特圖為主**（左），**右欄為對應 TODO 明細**（條列式）。點甘特任一列 ↔ 右欄明細會互相對應高亮。上方可用 A–G 篩選（G＝你）。
- **.nojekyll** — 讓 GitHub Pages 原樣提供靜態檔（勿刪）。

## 本機使用

用瀏覽器開 `index.html` → 點右上「重新載入 Excel」選 `工作分配.xlsx`（file:// 需手選一次，會記住）。改 Excel 存檔後重新載入即同步。

## 部署 GitHub Pages（一次設定）

本資料夾即網站根目錄。設定：

1. 先把變更推上去：
   ```
   git add docs .gitignore
   git commit -m "add team progress board (gantt + todo)"
   git push origin main
   ```
2. GitHub 倉庫 → **Settings → Pages**。
3. **Build and deployment → Source** 選 **Deploy from a branch**。
4. Branch 選 **main**、資料夾選 **/docs**，按 **Save**。
5. 等 1–2 分鐘，網址：
   **https://our-best-project.github.io/Stock-information-platform/**

部署後（https 環境）頁面會**自動載入**同資料夾的 `工作分配.xlsx`，免手選。之後每次 `git push` 更新 xlsx，Pages 會自動重新發佈。

## 代號

A 後端/基礎設施｜B 爬蟲｜C 向量化/去重｜D LLM｜E 評分/籌碼｜F 前端｜**G＝你（統籌/merge/架構掌握，不寫程式）**
