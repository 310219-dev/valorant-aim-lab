# 角度實驗室

Valorant 靈感的瀏覽器瞄準訓練原型，包含 WASD 主觀移動、急停點射、可調靜止靶停留時間、轉點反應與預瞄清角練習模式。此專案為獨立練習工具，並非 Riot Games 官方產品，也不會操作遊戲客戶端。

- 線上試玩：[角度實驗室](https://310219-dev.github.io/valorant-aim-lab/)
- GitHub：[310219-dev/valorant-aim-lab](https://github.com/310219-dev/valorant-aim-lab)

## 操作

- 準心跟隨滑鼠；定點急停與轉點反應模式可使用 WASD 做主觀移動，場景與靶子會相對視角位移，讓靶子相對準心改變位置。放開按鍵並等待慣性停止，或同時按下同軸反方向鍵（A+D／W+S）抵消移動後再點靶；移動中射擊會記為未命中。
- 「靜止靶停留」設定可調整靶子消失時間；開啟移動靶時使用固定移動靶時限。

## 本機預覽

直接在瀏覽器開啟 `index.html` 即可。網頁不需要建置步驟。

## 發布

推送到 `main` 分支時，GitHub Actions 會將靜態頁面發布到 GitHub Pages。也可以從 Actions 頁面手動執行 `Deploy to GitHub Pages`。
