# Tournament Approval Prototypes

排行榜活動簽核功能的可點擊原型，共兩份。單一 HTML 檔、無後端、無建置流程，所有狀態變化都在瀏覽器端模擬，重新整理即回到初始狀態。兩份都可切換 English／繁體中文。

**入口頁：** https://igs-abbiehsieh.github.io/ranking-approval-prototype/

| | 對應畫面 | 直接連結 |
|---|---|---|
| **V1** | Activity Setting（活動列表頁） | [ranking-approval-prototype.html](https://igs-abbiehsieh.github.io/ranking-approval-prototype/ranking-approval-prototype.html) |
| **V2** | Simple Ranking Setting（活動設定頁） | [ranking-setting-approval-v2.html](https://igs-abbiehsieh.github.io/ranking-approval-prototype/ranking-setting-approval-v2.html) |

---

## V1 — 活動列表上簽核

活動設定送出後（Approval Status = Unsigned），Action 欄新增兩顆按鈕：

| 路徑 | 按鈕 | 結果 |
|---|---|---|
| A. 自行舉辦 | Confirm & Approve（同意生效） | 免責聲明 → 同意並送出 → 系統自動核准 → Approved |
| B. 提交審查 | Submit for Review（提交審查） | 提交說明 → 送出 → Pending Review → 待 JILI.US 人工審核 |

| Approval Status | Modify / Delete | Confirm & Approve | Submit for Review |
|---|---|---|---|
| Unsigned | 可操作 | 顯示 | 顯示 |
| Pending Review | 不可操作 | 隱藏 | 隱藏 |
| Approved | 不可操作 | 隱藏 | 隱藏 |

操作方式：第 1 列是 Unsigned，兩條路徑都可以走一次；第 2、3 列預設為 Pending Review／Approved，用來看鎖定後的樣子。狀態旁的 info 圖示會開啟簽核紀錄。走完路徑 B 後，表格下方出現 JILI.US 審查通知卡片，可用審核方身分核准。

---

## V2 — 設定頁三種送出方式

設定頁底部按鈕由 `Confirm｜Cancel` 改為：

`Cancel（取消）` ｜ `Save Draft（儲存草稿）` ｜ `Submit for Review（提交審查）` ｜ `Agree & Approve（同意簽核）`

| 按鈕 | 功能 | 送出後 |
|---|---|---|
| Save Draft | 只儲存設定，不進行審核 | 狀態維持 Draft（草稿），可繼續修改 |
| Submit for Review | 申請與 JILI.US 共同舉辦、共同分擔獎池 | Pending Review，設定鎖定，JILI.US 收到通知 |
| Agree & Approve | 營運商自行承擔獎池與責任 | 同意免責聲明後系統自動 Approved，設定鎖定 |

兩個彈窗都會先列出活動設定（活動名稱、遊戲、規則、起訖時間、**時區**、總得獎名額、總獎池）再顯示說明文案。時區跟著右上角 GMT 選單動態帶入，不是固定 GMT+8。

三種送出方式按下確定後，都會接到 Activity Setting 活動列表，顯示剛設定的那一列：

| 送出方式 | 狀態 | Modify / Delete |
|---|---|---|
| 儲存草稿 | 草稿 Draft | 亮燈，按 Modify 回到設定頁繼續改 |
| 提交審查 | 等待審查 | 灰階 |
| 同意簽核 | 已核准 | 灰階 |

可操作的部分：Event Games 可搜尋／篩選 Slot、Fish／加入移除；Prize Settings 可增列、複製、刪除，Winner Count、Value、Total Winners、Total Cost 即時重算，並帶進彈窗摘要與列表那一列。狀態旁 info 圖示開啟簽核紀錄（Event ID、Agent ID、操作帳號、簽核時間、起訖時間、時區、獎池、簽核時設定內容、免責同意紀錄）。

---

## 本機開啟

下載對應的 HTML 檔，雙擊即可。唯一連外的資源是 Google 字型（介面字體與圖示），離線時會自動退回系統字型，功能不受影響。
