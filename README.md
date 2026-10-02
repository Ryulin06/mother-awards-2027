# 模範母親互動網站（Supabase 版）

## 頁面
- `mobile.html`：給民眾掃 QR Code，只看互動頁。
- `screen.html`：現場大螢幕，只播放影片＋即時祝福跑馬燈。
- `admin.html`：工作人員登入後上傳／管理影片、隱藏留言。
- `config.js`：Supabase Project URL 與 publishable key。

## 已連接的 Supabase
- `awards`：60 位獲獎者資料。
- `wishes`：手機留言；已啟用 Realtime。
- `videos`：影片播放清單；已啟用 Realtime。
- Storage bucket：`event-videos`。

## 使用前最後一步
在 Supabase Authentication 建立工作人員帳號（Email + Password），再用該帳號登入 `admin.html`。
目前影片管理權限提供給 `authenticated` 使用者；正式公開活動前，建議再限制成指定管理員帳號。

## 部署
整個資料夾可直接部署到 GitHub Pages / Netlify / Vercel 等靜態網站服務。
QR Code 請指向 `/mobile.html`，現場電腦開 `/screen.html`，工作人員開 `/admin.html`。
