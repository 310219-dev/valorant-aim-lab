# 角度實驗室：願景與路線圖

## 願景

打造一個易於開啟的 Valorant 靈感瞄準訓練網頁，讓玩家練習頭線、第一發反應、轉點與清角順序。以獨立靜態網站運作，透過 GitHub Actions 發布到 GitHub Pages。

## 範圍與決策

- 初始討論多次標註「chat only」；這表示當時希望以聊天互動為主。後續需求明確改為建立 GitHub 專案並透過 GitHub Actions 與 Pages 發布，因此目前以**網頁版**為主線。
- 反應時間以瀏覽器本機計時；不會操作或連接 Valorant 客戶端。
- 本專案為獨立練習工具，非 Riot Games 官方產品。

## 目前狀態

- **產品原型：** `index.html` 已完成，包含定點急停、轉點反應、預瞄角度三種模式，基本數據面板、目標數量與移動設定。
- **文件：** `README.md` 已新增本機預覽及發布說明。
- **部署設定：** `.github/workflows/pages.yml` 已新增，設定推送 `main` 或手動執行時發布 GitHub Pages。
- **Git：** 本機 repository 在 `main` 分支已有 commit；尚未設定遠端，GitHub 網頁提交的歷史與本機不同。
- **GitHub：** 公開 repository [310219-dev/valorant-aim-lab](https://github.com/310219-dev/valorant-aim-lab) 已建立。首頁、README 和 workflow 已放在遠端 `main`。
- **Pages：** Workflow 已觸發；Pages 設定及公開部署仍待確認。

## 已完成

- [x] 確立 Valorant 靈感的反應、預瞄與清角訓練方向。
- [x] 製作可在瀏覽器開啟的單頁訓練原型。
- [x] 加入反應趨勢、命中率等基本回饋介面。
- [x] 建立專案 README。
- [x] 建立 GitHub Actions Pages workflow。
- [x] 建立公開 GitHub repository，並上傳首頁與 README。
- [x] 記錄純聊天的初始偏好及後續轉為網頁版的範圍更新。

## 剩餘路線圖

### 1. 同步 Git

- [ ] 同步本機與遠端 Git 歷史，讓後續本機推送可直接使用。

### 2. 發布到 GitHub Pages

- [ ] 確認 repository 的 Pages source 使用 GitHub Actions。
- [ ] 確認 Actions workflow 成功完成部署。
- [ ] 開啟 Pages 公開網址，確認頁面可載入及互動。
- [ ] 將 repository 與 Pages 網址補回 README。

### 3. 迭代訓練體驗

- [ ] 試玩各模式，修正流程或顯示問題。
- [ ] 擴充預瞄場景、角度變化與教練提示。
- [ ] 視回饋調整難度與回合統計。

## 驗收條件

- GitHub repository 包含網站原始檔、部署 workflow 及本計畫。
- 每次推送到 `main` 後，GitHub Actions 能完成 Pages 部署。
- Pages 網址可公開開啟並可操作訓練模式。
