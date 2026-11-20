# 中史溫習加油站

一個適合 GitHub Pages 的靜態網站，包含秦漢、魏晉南北朝及隋唐的默書和選擇題練習。網站不需安裝套件或執行建置程序。

## 發布到 GitHub Pages

1. 在 GitHub 建立儲存庫。
2. 解壓資源包，把**資料夾內的所有檔案與 `assets` 資料夾**上載到儲存庫根目錄；`index.html` 應與 `README.md` 在同一層。
3. 在儲存庫頁面點選 **Settings → Pages**。
4. 在 **Build and deployment → Source** 選擇 **Deploy from a branch**，然後選擇 `main` 分支及 `/(root)` 資料夾，按 **Save**。如果你的預設分支名稱不同，選擇實際存放檔案的分支。
5. 等候部署完成，回到 **Settings → Pages**，使用頁面顯示的網址開啟網站。

GitHub 官方說明：[設定 GitHub Pages 發布來源](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)。

## 在自己電腦預覽

在此資料夾開啟終端機，執行以下指令，再在瀏覽器開啟 `http://localhost:8000/`：

```sh
python3 -m http.server 8000
```

按 `Ctrl+C` 停止伺服器。

## 登入密碼及資料存取

現有示範登入密碼是 `dse2027`。密碼檢查在瀏覽器內執行，密碼及題庫都包含在網站檔案中；任何訪客都可透過檢視原始碼取得，**不構成真正的存取保護**。GitHub Pages 若設為公開，網頁、題目、答案和圖片也可被公眾讀取。請確認教材及圖片有適當的發布權限，並不要把個人資料或私人密碼放進這些檔案。

若日後需要真正限制學生登入、保護題庫或跨裝置保存答題紀錄，需要另外建立後端及帳戶驗證系統。現有的登入狀態只保存在瀏覽器工作階段；默書及 MC 作答不會上傳或跨裝置保存。

## 主要檔案

- `index.html`：首頁、登入、單元導覽及版面樣式。
- `mc-data.js`：各課選擇題、選項與答案；`mc.js` 負責選擇題互動。
- `qin-data.js`、`qin.js`：秦始皇默書內容及互動。
- `lessons-data.js`、`lessons.js`：其他課題默書內容及互動。
- `assets/history-characters.png`：平台人物及書本圖示。

甲部的清單元尚未提供默書內容；乙部及婦女史為待補充單元。題目與參考答案應在公開發布前按教學需要覆核。
