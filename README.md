# HoYoLAB 像素畫產生器

網址：https://twl-benchen.github.io/hoyolab-pixel-art/

把自己的畫轉成像素風格的網頁工具。只有一個 `index.html`，不用安裝任何東西，所有處理都在瀏覽器本機完成，圖片不會上傳。

## 功能

- 選圖、拖曳或 Ctrl+V 貼上圖片
- 調整寬度(格數)，高度依比例自動計算
- 三種縮小取色方式：平均、取最多的顏色、取中心點
- 減色 (k-means，0 到 64 色) 與抖色 (Floyd-Steinberg)
- 飽和度、透明門檻 (去背圖用)
- 色盤顯示，點色塊複製色碼
- 下載 1 到 32 倍放大的清晰 PNG
- HoYoLAB 色塊模式：轉成一格一字的色塊文字，模擬手機 App 白縫預覽，一鍵複製貼上

## 放上 GitHub Pages

1. 在 GitHub 建一個新的 repo，例如 `hoyolab-pixel-art`
2. 把 `index.html` 和 `README.md` 上傳到 repo 根目錄
3. 到 repo 的 Settings > Pages，Source 選 `Deploy from a branch`，Branch 選 `main`，資料夾選 `/ (root)`，按 Save
4. 等一兩分鐘，網址會是 `https://<你的帳號>.github.io/hoyolab-pixel-art/`

## HoYoLAB 模式

以電腦版顯示為準，手機 App 不另外適配。電腦版編輯器實測各字號一行最多的格數：

| 字號 | 12px | 14px (預設) | 18px | 22px | 24px | 32px |
|---|---|---|---|---|---|---|
| 一行格數 | 66 | 57 | 44 | 36 | 33 | 24 |

使用步驟：在編輯器按 Enter 換新行，貼上，全選剛貼上的色塊，用工具列把字號改成工具裡選的大小。

行與行之間有白縫，無法用樣式去除 (段落行高、色塊墊高等寫法都會被編輯器過濾)，工具會把圖上下壓扁來補償比例。
