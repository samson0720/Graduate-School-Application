# 116 學年度碩士班甄試 申請資料

韓欣澄 Hsin-Cheng Han｜國立中央大學 資訊工程學系

## 檔案

| 檔案 | 內容 | 編譯器 |
| --- | --- | --- |
| `autobiography.tex` | 自傳（Personal Statement） | XeLaTeX |
| `portfolio.tex` | 專題與經歷佐證資料（其他有利審查資料） | XeLaTeX |
| `resume.tex` | 簡歷（單頁） | XeLaTeX |
| `figures/` | `portfolio.tex` 引用的圖片 | — |
| `photos/photo.jpg` | `resume.tex` 引用的大頭照 | — |
| `CHECKLIST.md` | 送出前待補與待確認事項（含三份文件間的矛盾） | — |

## 編譯

三份文件都必須用 **XeLaTeX**（使用 `fontspec` / `xeCJK`）。在 Overleaf 請於
`Menu → Compiler` 選 `XeLaTeX`。

```bash
xelatex autobiography.tex
xelatex portfolio.tex
xelatex resume.tex
```

字型：中文優先使用標楷體（DFKai-SB / BiauKai / TW-Kai），英文 Times New Roman；
找不到時會自動退回 Liberation Serif 與 AR PL UKai TW，不會編譯失敗。

## 圖片

`portfolio.tex` 用 `\safeimg` 引用圖片，**檔案不存在時會顯示紅字「【圖片待補】」佔位框，
不會中斷編譯**。需要放進 `figures/` 的檔案：

```
katch_arch.png  katch_ui1.png  katch_ui2.png  katch_award.jpg
grasp_arch.png  grasp_ui1.png  grasp_ui2.png  grasp_photo.jpg
esg_pipeline.png  esg_result.png
greenepass_arch.png  greenepass_ui1.png  greenepass_award.jpg
netapp_arch.png  netapp_ui1.png
tt_pipeline.png  tt_result.png
hlb_arch.png  hlb_ui1.png  hlb_expo.jpg
```

實習與服務經歷已改用與專題相同的卡片樣式（`\expcard`），欄位包含 `arch` / `shotA` /
`shotB` / `photo`，同樣用 `\safeimg` 引用；目前尚未指定圖片，缺圖時會顯示佔位框。

## 待補事項

紅字 `【待補：…】` 是尚未確認的欄位，**送出前必須清空**。
完整清單見 [`CHECKLIST.md`](CHECKLIST.md)。

```bash
grep -n 'todo{' portfolio.tex
```
