# 角度實驗室：願景與路線圖

## 願景

打造一個易於開啟的 Valorant 靈感瞄準訓練網頁，讓玩家練習頭線、第一發反應、轉點與清角順序。以獨立靜態網站運作，透過 GitHub Actions 發布到 GitHub Pages。

## 範圍與決策

- 初始討論多次標註「chat only」；當時希望以聊天互動為主。之後明確改為建立 GitHub 專案並透過 Actions 和 Pages 發布，目前以**網頁版**為主線。
- 反應時間以瀏覽器本機計時；不操作或連接 Valorant 客戶端。
- 本專案為獨立練習工具，非 Riot Games 官方產品。

## 目前狀態

- **原型：** `index.html` 已完成，包含定點急停、轉點反應、預瞄角度三種模式與基本數據面板。
- **部署：** `.github/workflows/pages.yml` 已建立；Pages source 已設為 GitHub Actions，最新 workflow 已成功。
- **GitHub：** 公開 repository [310219-dev/valorant-aim-lab](https://github.com/310219-dev/valorant-aim-lab) 已包含首頁、README、workflow 與本計畫。
- **Pages：** [角度實驗室](https://310219-dev.github.io/valorant-aim-lab/) 已公開並確認可載入。
- **本機 Git：** 本機 `main` 有 commits，遠端 repository 由網頁提交建立；尚未設定 remote 或同步歷史。

## 已完成

- [x] 確立 Valorant 反應、預瞄與清角訓練方向。
- [x] 製作瀏覽器單頁原型與基本回饋介面。
- [x] 建立公開 GitHub repository。
- [x] 將首頁與 README 上傳到遠端 `main`，README 已附線上試玩網址。
- [x] 建立 GitHub Actions Pages workflow，並確認部署成功。
- [x] 將願景、範圍、狀態與路線圖納入本檔。
- [x] 記錄初始「chat only」偏好及後續轉為網頁版的決策。

## 剩餘路線圖

### Git 同步

- [ ] 設定本機 `origin`，同步本機與遠端 Git 歷史，讓後續本機推送可直接使用。

### 訓練體驗迭代

- [ ] 試玩各模式並修正流程或顯示問題。
- [ ] 擴充預瞄場景、角度變化與教練提示。
- [ ] 依玩家回饋調整難度與回合統計。

## 驗收條件

- GitHub repository 包含網站原始檔、部署 workflow 及本計畫。
- 推送到 `main` 後，GitHub Actions 能完成 Pages 部署。
- Pages 網址可公開開啟並操作訓練模式。

## 發布網址

- Repository: https://github.com/310219-dev/valorant-aim-lab
- GitHub Pages: https://310219-dev.github.io/valorant-aim-lab/
