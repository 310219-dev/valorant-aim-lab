# 角度實驗室：願景與路線圖

## 願景

打造一個易於開啟的 Valorant 靈感瞄準訓練網頁，讓玩家練習頭線、第一發反應、轉點與清角順序。以獨立靜態網站運作，透過 GitHub Actions 發布到 GitHub Pages。

## 範圍與決策

- 初始討論多次標註「chat only」；當時希望以聊天互動為主。之後明確改為建立 GitHub 專案並透過 Actions 和 Pages 發布，目前以**網頁版**為主線。
- 反應時間以瀏覽器本機計時；不操作或連接 Valorant 客戶端。
- 本專案為獨立練習工具，非 Riot Games 官方產品。

## 目前狀態

- **最新迭代：** 暫停續練保留目標、動畫、倒數與場景位移；預瞄提供四段資料驅動角度順序。

- **原型：** `index.html` 已完成，包含定點急停、轉點反應、預瞄角度三種模式、WASD 主觀移動、急停判定、靜止靶停留時間設定與基本數據面板。
- **部署：** `.github/workflows/pages.yml` 已建立；Pages source 已設為 GitHub Actions，最新 workflow 已成功。
- **GitHub：** 公開 repository [310219-dev/valorant-aim-lab](https://github.com/310219-dev/valorant-aim-lab) 已包含首頁、README、workflow 與本計畫。
- **Pages：** [角度實驗室](https://310219-dev.github.io/valorant-aim-lab/) 已公開並確認可載入。
- **本機 Git：** `main` 已追蹤 `origin/main`，本機與遠端歷史同步；原本的本機提交保存在 `local-pre-github-sync` 分支。

## 已完成

- [x] 確立 Valorant 反應、預瞄與清角訓練方向。
- [x] 製作瀏覽器單頁原型與基本回饋介面。
- [x] 建立公開 GitHub repository。
- [x] 將首頁與 README 上傳到遠端 `main`，README 已附線上試玩網址。
- [x] 建立 GitHub Actions Pages workflow，並確認部署成功。
- [x] 將願景、範圍、狀態與路線圖納入本檔。
- [x] 設定本機 `origin`，同步本機 `main` 與遠端 `origin/main`。
- [x] 記錄初始「chat only」偏好及後續轉為網頁版的決策。
- [x] 加入 WASD 主觀移動與慣性急停；場景和靶子在同一世界座標層移動，靶子會相對準心改變位置；移動中射擊列為未命中；同軸反方向鍵（A+D／W+S）會立即抵消移動，可作為急停。
- [x] 準心跟隨滑鼠並加入 0.5× 至 2.0× 靈敏度倍率（1.0× 為一比一）；以虛擬準心位置判定命中。
- [x] 加入靜止靶停留時間選項（0.8 至 5 秒），讓玩家自行調整消失頻率。
- [x] 修正靶子切換時舊逾時 callback 誤刪新靶子的競態，並用多輪近逾時點擊模擬確認靶子不會提前消失。
- [x] 反向鍵同軸相抵時立即停止，確保急停後可命中判定。
- [x] 加入可調滑鼠靈敏度，並以準心位置判斷點射命中。
- [x] 修正暫停後按「繼續訓練」會清空統計的問題；續練保留本輪數據。
- [x] 急停時等到殘餘速度歸零才解除移動／不可射擊狀態。
- [x] 預瞄模式揭露近角與遠角目標，命中／錯過後再進入下一角度。

## 剩餘路線圖

### 訓練體驗迭代

- [x] 手動試玩各模式並修正流程或顯示問題；確認定點、轉點可啟動，預瞄近角清除後會進入遠角提示。
- [x] 擴充預瞄角度順序與教練提示，加入四個可輪替的近／遠／深位目標。
- [ ] 收集玩家試玩回饋，再調整難度與回合統計（決策建議見 `knowledge/decision.md`）。
- [x] 暫停時保留當前目標、動畫、倒數與場景位移；續練還原快照，重設或切換模式則丟棄。

## 驗收條件

- GitHub repository 包含網站原始檔、部署 workflow 及本計畫。
- 推送到 `main` 後，GitHub Actions 能完成 Pages 部署。
- Pages 網址可公開開啟並操作訓練模式。

## 發布網址

- Repository: https://github.com/310219-dev/valorant-aim-lab
- GitHub Pages: https://310219-dev.github.io/valorant-aim-lab/
