# 工程 AI 出圖系統 PWA

自動生成高品質 AI 工程繪圖提示詞的 Progressive Web App。

## 部署到 GitHub Pages

### 步驟 1 — 建立 Repository

1. 登入 GitHub，點選右上角 **+** → **New repository**
2. Repository name 輸入：`engineering-drawing`（或自訂名稱）
3. 設為 **Public**（GitHub Pages 免費版須為公開）
4. 不要勾選 Initialize，直接點 **Create repository**

### 步驟 2 — 上傳所有檔案

將本 zip 解壓後，把 **所有檔案與資料夾** 推送到 `main` branch：

```bash
cd 工程繪圖-pwa
git init
git add .
git commit -m "Initial PWA deployment"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/engineering-drawing.git
git push -u origin main
```

### 步驟 3 — 啟用 GitHub Pages

1. 進入 Repository → **Settings** → **Pages**
2. Source 選擇 **GitHub Actions**
3. 儲存後，GitHub Actions 會自動執行 `deploy.yml`

### 步驟 4 — 確認部署

Actions 頁面出現綠色勾勾後，網址為：
```
https://YOUR_USERNAME.github.io/engineering-drawing/
```

## PWA 安裝說明

| 平台 | 安裝方式 |
|------|---------|
| Android Chrome | 網址列下方出現「新增到主畫面」橫幅，點選即可 |
| iOS Safari | 點選分享圖示 → 「加入主畫面」 |
| PC Chrome/Edge | 網址列右側出現安裝圖示，點選安裝 |

## 檔案結構

```
工程繪圖-pwa/
├── index.html          # 主應用程式
├── manifest.json       # PWA 設定檔
├── sw.js               # Service Worker（離線支援）
├── icon.png            # 原始圖示
├── icon-192.png        # PWA 圖示 192×192
├── icon-512.png        # PWA 圖示 512×512
└── .github/
    └── workflows/
        └── deploy.yml  # GitHub Actions 自動部署
```
