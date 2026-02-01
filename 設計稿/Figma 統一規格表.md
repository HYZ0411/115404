# Figma 統一規格表（Design Spec）

## 字體設計（Typography）

| 用途 | Font family | Weight | Size | Color | Opacity |
|---|---|---|---|---|---|
| 標題（Title） | Lexend | Bold | 35px | #000000 | 100% |
| 副標題（Subtitle） | Lexend | Bold | 22px | #626262 | 100% |
| 內文（Body） | Lexend | Medium | 16px | #000000 | 100% |
| 說明（Caption/Hint） | Lexend | Regular | 14px | #737373 | 100% |

## 卡片預設設計（Card Default）

| 項目 | 規格 |
|---|---|
| 尺寸 | W：依照需求調整；H：依照需求調整 |
| Fill（底色） | #FFFFFF（100%） |
| Appearance | Opacity：100%；Corner radius：24 |
| Stroke | Color：#E6E6E6（50%）；Position：Center；Width：1px |
| Effects（Drop shadow） | Position：x=6, y=6；Blur：10；Spread：0；Color：#000000（25%） |

## 訓練按鈕（Training Button）

| 項目 | 規格 |
|---|---|
| 尺寸 | W 353 × H 48 |
| Appearance | Corner radius：24 |
| Effects（Drop shadow） | Position：x=6, y=6；Blur：10；Spread：0；Color：#000000（25%） |

### 狀態樣式 (Interaction States)

| 按鈕類型 | 狀態 (State) | Fill (底色) | Text (文字) |
|---|---|---|---|
| **開始 (Start)** | 未按下 (Normal) | #14CE75 (100%) | Lexend Bold 16px; #FFFFFF |
| | **按下 (Pressed)** | **#083620 (100%)** | **Lexend Bold 16px; #737373** |
| **結束 (End)** | 未按下 (Normal) | #FF0000 (100%) | Lexend Bold 16px; #FFFFFF |
| | **按下 (Pressed)** | **#360707 (100%)** | **Lexend Bold 16px; #737373** |

## 繼續按鈕（Continue Button）

| 狀態 | 尺寸 | Fill（底色） | Effects（Drop shadow） | Text（文字） |
|---|---:|---|---|---|
| 未解鎖（Locked） | W 353 × H 48 | #737373（100%） | Position：x=0, y=4；Blur：4；Spread：0；Color：#000000（25%） | Lexend Bold 16px；#FFFFFF（100%） |
| 已解鎖（Unlocked） | W 353 × H 48 | #2289FF（100%） | Position：x=0, y=4；Blur：4；Spread：0；Color：#000000（25%） | Lexend Bold 16px；#FFFFFF（100%） |

## 長方形按鈕（Rectangle Button）

| 項目 | 規格 |
|---|---|
| 尺寸 | W 353 × H 140 |
| Appearance | Corner radius：24 |
| Stroke | Color：#E6E6E6（50%）；Position：Inside；Width：1px |
| Effects（Drop shadow） | Position：x=6, y=6；Blur：10；Spread：0；Color：#000000（25%） |
| 文字規格 | 內文：同 Body 樣式；說明：同 Caption 樣式 |
| 內容圖片 | 依實際內容配置 |

### 狀態樣式

| 狀態 | Fill（底色） | 備註 |
|---|---|---|
| 未選擇 | #FFFFFF（100%） | |
| 已選擇 / 按下 | #737373（100%） | 內容/文字建議轉為 #FFFFFF |

## 小按鈕（Small Icon Button）

| 項目 | 規格 |
|---|---|
| 尺寸 | W 48 × H 48 |
| Appearance | Opacity：100%；Corner radius：16 |
| Effects（Drop shadow） | Position：x=6, y=6；Blur：10；Spread：0；Color：#000000（25%） |

### 狀態樣式 (Interaction States)

| 狀態 (State) | Fill (底色) | Content/Icon (內容顏色) | Stroke (邊框) |
|---|---|---|---|
| 未按下 (Normal) | #F5F5F5 | #000000 | #E6E6E6 (50%) |
| **按下 (Pressed)** | **#737373** | **#FFFFFF** | **#E6E6E6 (50%)** |

## 切換按鈕（Toggle Button）

| 項目 | 規格 |
|---|---|
| 尺寸 | W 93 × H 35 |
| Appearance | Corner radius：24 |
| Fill（底色） | #D9D9D9（100%） |
| Text（文字） | Lexend Medium 24px；#000000（100%） |
| Effects（Drop shadow） | Position：x=6, y=6；Blur：10；Spread：0；Color：#000000（25%） |

## 文案與標點符號規範（Content & Punctuation）

| 符號類型 | 規範 | 範例 |
|---|---|---|
| **冒號** | 全形 `：` | 尺寸：W 353 |
| **括號** | 半形 `()` | (未解鎖) |
| **句點、逗號** | 全形 `。` `，` | 這裡有說明，請參考。 |
