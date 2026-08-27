# 金口訣 — web 版

大六壬金口訣起課工具的 web 建置產出。

- App：<https://magicsmallbear.github.io/jinkoujue-web/>
- 隱私權政策：<https://magicsmallbear.github.io/jinkoujue-web/privacy.html>

## 這個倉庫是什麼

**只放建置產出，不是原始碼倉庫。** 內容由 Expo 專案以

```bash
npx expo export --platform web
```

產生，原始碼在另一個私有倉庫。手改這裡的檔案會在下次匯出時被覆蓋。

`.nojekyll` 不可刪 —— GitHub Pages 的 Jekyll 會略過底線開頭的目錄，
刪掉它 `_expo/` 底下的 JS bundle 會 404。

## 使用前請注意

起課結果**尚未完成外部校對**。引擎的 37 筆 golden 案例中，7 筆已對照
《六壬神課金口訣古本》卷之上的起課例逐項校對，其餘 30 筆的期望值仍是引擎
自己的快照 —— 也就是說，測試全綠只代表「沒有改壞」，不代表「算得對」。

課鈐斷辭與歌訣為古籍原文照錄；白話與導讀均為本專案自撰，非出自任何定本，
在介面上都已標明。
