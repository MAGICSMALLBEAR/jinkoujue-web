# 金口訣 — web 版

大六壬金口訣起課工具的 web 建置產出。

- App：<https://magicsmallbear.github.io/jinkoujue-web/>
- 隱私權政策：<https://magicsmallbear.github.io/jinkoujue-web/privacy.html>

## 可安裝離線使用

本站是 PWA：瀏覽器選「加到主畫面／安裝」後可離線起課 —— 引擎與曆法全在前端，
斷網不影響排盤。離線快取由 `sw.js` 管理，清單依每次匯出的實際檔名與內容雜湊生成，
新版上線時 service worker 會自動更替並清除舊快取。

## 這個倉庫是什麼

**只放建置產出，不是原始碼倉庫。** 內容由 Expo 專案以

```bash
npx expo export --platform web
```

產生，原始碼在另一個私有倉庫。手改這裡的檔案會在下次匯出時被覆蓋。

`.nojekyll` 不可刪 —— GitHub Pages 的 Jekyll 會略過底線開頭的目錄，
刪掉它 `_expo/` 底下的 JS bundle 會 404。

`privacy.html` **自 2026-09-01 起亦為產出物** —— 政策原文在來源專案的
`docs/隱私權政策.md`，HTML 版放在 `public/`，兩份的同步由來源專案的測試鎖住。
改政策請改那邊，不要改這裡。

`sw.js` 與 `manifest.json` 亦為產出物：前者由 `scripts/generateServiceWorker.ts`
依當次匯出生成，後者來自來源專案的 `public/`。兩張圖示中，`pwa-maskable.png`
的線稿收在遮罩安全區（約 61%）內，不可與 `pwa-icon.png` 對調。

## 使用前請注意

起課結果**尚未完成外部校對**。引擎的 37 筆 golden 案例中，7 筆已對照
《六壬神課金口訣古本》卷之上的起課例逐項校對，其餘 30 筆的期望值仍是引擎
自己的快照 —— 也就是說，測試全綠只代表「沒有改壞」，不代表「算得對」。

課鈐斷辭與歌訣為古籍原文照錄；白話與導讀均為本專案自撰，非出自任何定本，
在介面上都已標明。
