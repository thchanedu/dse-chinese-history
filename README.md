# 中史溫習加油站

本資源包為現有預覽版的靜態網站，包含默書溫習、MC 挑戰、隋唐皇帝措施配對遊戲，以及秦漢歷屆試題。無需安裝套件或建置。

## 更新現有 GitHub 儲存庫

1. 把 ZIP 解壓。打開解壓後的資料夾，確認當中能直接看到 `index.html`、`assets` 資料夾及其他 `.js` 檔案。
2. 開啟 GitHub 上的 `dse-chinese-history` 儲存庫，按 **Add file → Upload files**。
3. 把解壓後資料夾**裏面的檔案和 `assets` 資料夾**上載至儲存庫根目錄；不要把 ZIP 直接上載，也不要把整個解壓資料夾再包一層。GitHub 提示同名檔案時，以上載的新版本取代。
4. 按 **Commit changes** 儲存。如果儲存庫有保護分支，請依 GitHub 的提示使用其他分支及合併流程。
5. 在 **Settings → Pages** 確認 **Source** 為 **Deploy from a branch**，分支為 `main`（或你的實際預設分支），資料夾為 `/(root)`，並按 **Save**。
6. 等待部署完成，再在 **Settings → Pages** 點開網站網址。如果看到舊版，重新整理網頁。

`.nojekyll` 是 GitHub Pages 的隱藏設定檔，使用命令列或支援顯示隱藏檔案的方式上載即可；此網站沒有需要 Jekyll 處理的內容。GitHub Pages 會從所選分支和資料夾發布。

## 電腦預覽

在此資料夾開啟終端機，執行 `python3 -m http.server 8000`，然後在瀏覽器開啟 `http://localhost:8000/`；按 `Ctrl+C` 結束。

## 重要設定與存取

- 網站登入密碼為 `dse2027`。此示範密碼在前端程式中，無法真正保護內容；知道連結的人可查看網站原始碼中的密碼、題目及答案。
- 網站包含歷屆試題原 PDF 及其頁面圖片。若使用公開 GitHub 儲存庫或公開 GitHub Pages，訪客可以存取這些檔案。公開發布前請確認相關內容及圖片的使用權限。
- 現有登入狀態及作答內容不會跨裝置保存；歷屆試題的試寫內容在重新整理後會清除。
- 「清」單元暫時不能進入；必修乙部、選修單元六及其他朝代的歷屆試題待補充。

## 檔案說明

- `index.html`：網站頁面、樣式、登入及單元導覽。
- `mc.js`、`mc-data.js`：選擇題操作與題庫。
- `qin.js`、`qin-data.js`：秦始皇默書溫習。
- `lessons.js`、`lessons-data.js`：其他課題默書溫習。
- `past-papers.js`、`assets/papers/`：歷屆試題導覽及原始資料。
- `emperor-match.js`：隋唐皇帝措施配對挑戰，支援觸控拖曳與點選。
- `assets/history-characters.png`：人物及書本圖示。
