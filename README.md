# Jimmy 的 Web App 導覽

一個以「導覽站」為根目錄的靜態個人專案集合。根頁面（`index.html`）是
**Navigator**：以卡片集中列出所有 web app 專案，支援搜尋、分類與狀態篩選。

## 導覽站功能

- 卡片顯示：專案名稱、簡介、技術堆疊、狀態（已上線／開發中）、連結
- 即時搜尋（名稱／簡介／技術）＋ 分類／狀態篩選 ＋ 一鍵重設
- 深淺色主題、響應式（桌面／平板／手機）、列印樣式
- 純靜態、零依賴、單檔案 HTML

## 專案結構

```
index.html          導覽站（Navigator）
projects.json       ★ 專案清單 — 新增/修改專案只需編輯這個檔案
todo/index.html     待辦清單 Todo List 應用
```

## 新增一個專案

只改 `projects.json` 的 `projects` 陣列，加一個物件：

```jsonc
{
  "id": "my-app",              // 唯一識別碼
  "name": "專案名稱",           // 卡片標題
  "description": "一兩句簡介",  // 卡片內文
  "tech": ["HTML", "CSS", "JavaScript"], // 技術堆疊 chips
  "category": "工具",           // 分類（自動產生篩選鈕）
  "status": "live",            // "live" 已上線 / "dev" 開發中 / 其他自訂
  "url": "/my-app/",           // 本站內路徑或完整 http(s) 連結；null = 尚未發布
  "external": false            // 外部連結填 true（會新分頁開啟）
}
```

把該應用的 `index.html` 放到 `url` 所指路徑（例如 `my-app/index.html`），
push 後 GitHub Actions 自動重新部署，導覽站即出現新卡片。

## 部署

`.github/workflows/deploy.yml` 在每次 push 到 `main` 自動建置並部署到
GitHub Pages（Actions 來源）。

> 公開網址：https://cmjyeung2016.github.io/HermesAgent10102026/
