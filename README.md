# Leaderboard Approval Flow — Prototype

排行榜活動「廠商自主簽核」功能的可點擊原型。單一 HTML 檔，無後端、無建置流程，所有狀態變化都在瀏覽器端模擬。

**開啟原型：** https://igs-abbiehsieh.github.io/ranking-approval-prototype/

## 這個原型演示什麼

活動設定送出後（Approval Status = Unsigned），Action 欄新增兩顆按鈕，對應兩條簽核路徑：

| 路徑 | 按鈕 | 結果 |
|---|---|---|
| A. 自行舉辦 | Confirm & Approve（同意生效） | 顯示免責聲明 → 同意並送出 → 系統自動核准 → Approved |
| B. 提交審查 | Submit for Review（提交審查） | 顯示提交說明 → 送出 → Pending Review → 待 JILI.US 人工審核 |

按鈕顯示規則：

| Approval Status | Modify / Delete | Confirm & Approve | Submit for Review |
|---|---|---|---|
| Unsigned | 可操作 | 顯示 | 顯示 |
| Pending Review | 不可操作 | 隱藏 | 隱藏 |
| Approved | 不可操作 | 隱藏 | 隱藏 |

## 操作方式

- 表格第 1 列是 Unsigned，兩條路徑都可以走一次。
- 第 2、3 列預設為 Pending Review／Approved，用來看鎖定後的樣子。
- 狀態旁的 info 圖示會開啟簽核紀錄（操作帳號、操作時間、同意紀錄、審核結果）。
- 走完路徑 B 後，表格下方會出現 JILI.US 審查通知卡片，上面有一顆模擬按鈕可以用審核方身分核准，走完 Pending Review → Approved。
- 右上角語言選單切換 English／繁體中文，所有新增文案兩版都有。
- 右下角有操作說明和「重設原型」。

## 本機開啟

下載 `ranking-approval-prototype.html`，雙擊即可。唯一連外的資源是 Google 字型（介面字體與圖示），離線時會自動退回系統字型，功能不受影響。
