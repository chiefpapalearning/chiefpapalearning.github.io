# rich-notes

智富主理人（ChiefPaPa / Rich Cheung）的公開筆記 / LM 網頁。GitHub Pages 免費代管。

**帳號**：`chiefpapalearning`（CPP 與 Rich 共用，與 Olivia 個人帳號 `Hsuan199` 分開）
**Repo 名必須是** `chiefpapalearning.github.io` ← 跟帳號同名，網址才會少一層

網址格式：
```
https://chiefpapalearning.github.io/<主理人>/<資料夾名>/
```
目前這份：`https://chiefpapalearning.github.io/rich/ai-5steps/`

---

## 資料夾長怎樣

```
chiefpapalearning.github.io/
  assets/                    ← 素材只放這裡，不要搬也不要改名
    rich/                      Rich 的橫幅、簽名
      banner.png
      signature.jpg
    cpp/                       CPP 的（之後放）
  rich/
    ai-5steps/
      index.html               一篇 LM = 一個資料夾 + 一個 index.html
  cpp/                       （之後）
```

**兩層都會出現在網址**：`/<主理人>/<資料夾名>/`
資料夾名取短、英文小寫、連字號，不要放日期（日期記檔案裡就好）。

**為什麼素材要集中**：每份 LM 都指向 `../../assets/<主理人>/` 的同一份圖。
橫幅哪天換新版，改 `assets/` 裡那一個檔案，所有 LM 一起更新。

**為什麼素材要共用**：每份新 LM 都指向 `../assets/` 的同一份圖。
橫幅哪天換新版，改 `assets/` 裡那一個檔案，所有 LM 一起更新。

---

## 要出新的一份 LM

1. 複製 `rich/ai-5steps/` 整個資料夾，放到該主理人底下，改名成新的短英文名（會變成網址）
2. 編輯裡面的 `index.html`（換標題、內文、prompt）
3. 圖的路徑保持 `../../assets/<主理人>/...` 不要動
4. 上傳到 GitHub → 網址自動生成

**做 CPP 的第一份時**：先把 CPP 的橫幅／簽名放進 `assets/cpp/`，
然後在 `cpp/` 底下建資料夾，圖路徑指向 `../../assets/cpp/...`。
⚠️ CPP 的色票與 Rich 不同（CPP carousel 是深色主題、production 金是 `#E7C766` 不是 `#F3CE6A`），
改版前先讀品牌規則主檔，不要沿用 Rich 的值。

---

## 品牌色（別自己配，這是官方值）

來源：`歐歐本地/1. Project🌳/1.1 智富/品牌/智富品牌知識Hub/品牌/carousel-design.md`
（那份文件鏡像自 `colors_and_type.css`，那才是唯一值真相源）

| 用途 | 色碼 |
|------|------|
| 主藍（標題、內文、按鈕底） | `#0A2751` |
| 金（裝飾、標籤底）⚠️ 出圖用這個 | `#F3CE6A` |
| guide 金 ⚠️ 只給展示，**不要**拿來出圖 | `#FFE48F` |
| 淺底 | `#F4F7FE` |

**規範裡的兩條硬規則**：
- 淺底一律用深色字，標題用 `#0A2751`
- 標籤 = **金底藍字**（不是藍底金字）

⚠️ 金色在白底上對比只有 1.52:1，**不能拿來當文字**，只能當底色或線條。

### 不是官方色的兩個值

`index.html` 裡另有兩個我調過明度的色，色票裡沒有：

- `--rule: #DCE5F3` — 官方 rule `#4C78B8` 太搶眼，淡化後當髮絲線
- `--muted: #63788F` — 官方 muted `#9FB0C4` 在白底只有 2.21:1 看不清楚，加深到 4.55:1

要改回官方值的話，注意上面的對比度問題。

---

## 簽名圖的特殊處理

`signature.jpg` 原圖 1920×1080，但墨跡實際只在 `x520–1418 / y340–692`，
四周有大量空白。CSS 用一個「視窗」把白邊裁掉（`.sig` / `.sig img`），
**圖檔本身沒有被修改**。

換簽名圖的話，那幾個百分比要重新算，算法寫在 `index.html` 的 CSS 註解裡。

---

## 注意

- repo 必須是 **Public**，GitHub Pages 免費版才會生效 → 內容等於公開，任何人有網址就看得到
- 內文文字若有更動，屬對外文案，走原本的閘門流程
