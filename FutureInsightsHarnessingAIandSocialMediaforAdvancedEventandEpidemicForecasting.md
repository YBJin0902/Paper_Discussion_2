# Future Insights：Harnessing AI and Social Media for Advanced Event and Epidemic Forecasting


## 一、研究計畫簡介：IARPA 的 OSI 計畫

**OSI（Open-Source Indicators）開放源指標計畫**由 IARPA 推動，目的是發展一套可持續、全自動分析公開資料的方法，來**預測與偵測社會群體層級的重大事件**。
這些事件包括：

* 政治危機（Political crises）
* 人道災難
* 大規模暴力、暴動（Mass violence, riots）
* 疾病爆發（Disease outbreaks）
* 經濟不穩、資源短缺
* 自然災害回應

此計畫著重於從 **公開資料（publicly available data）** 中擷取趨勢，並試圖 **提前預警（anticipate）** 相關事件。

---

## 二、預測系統的評估與指標

預測模型的評估方式如下：

* 預測結果會 **自動傳送給評估者**，過程不需要人工介入（human-in-the-loop）
* 評估由獨立第三方機構 **MITRE** 執行
* 使用的標準為 **GSR（Gold Standard Report）**，來自具影響力媒體的報導
* 評估指標包括：

  1. 預測品質（Quality）：0～4 分
  2. 領先時間（Lead time）：提前預警的程度
  3. 召回率（Recall）
  4. 精確率（Precision）
  5. 預測機率的可靠性（Probability/Reliability）

---

## 三、Lead Time 領先時間計算方式

領先時間的衡量方式如下：

* **Forecast Date（t1）**：預測發布時間
* **Event Date（t2）**：實際事件發生日期
* **Predicted Event Date（t3）**：模型預測的事件日期
* **Reported Date（t4）**：媒體首次報導時間

例子：
若預測於 3 月 3 日送出（t1），事件於 3 月 9 日報導（t4），則領先時間分數 = t4 - t1 = **6 天**

---

## 四、品質評估要素（Aspects of Quality）

品質評分包含四項：

* **日期分數**（Date Score）：事件預測日與實際事件日的差距
* **主題分數**（Population/Event Type）：事件類型、參與人群是否一致
* **地點分數**（Location Score）：預測與實際地點的吻合度
* **總體品質分數**：加總上述分數後，作為預測可靠性的量化依據

---

## 五、挑選資料來源的六大考量（6 V’s）

在選擇資料來源時，需考量以下六大指標：

1. **Volume（資料量）**
2. **Velocity（更新速度）**
3. **Variety（資料多樣性）**
4. **Veracity（真實性與可信度）**
5. **Value（資訊價值）**
6. **Visualization（可視化能力）**

---

## 六、價值評估：多指標定位分析

在地理資訊推論上，透過多種指標交叉比對，包括：

* **作者位置**（Author location）
* **文件中提及地點**（Mentioned places）
* **報導地點**（Reported location）
* **事件地點**（Event location）

例如，一則來自 Twitter 的貼文顯示作者位於美國維吉尼亞州的杜勒斯機場，文中則提到即將前往台灣雲林參加活動，即可推斷活動的潛在發生地。

---

## 七、示範應用：群眾抗議預測（Civil Unrest Forecasting）

使用多個模型進行預測，包括：

* **資料來源**：Tor、RSS、Twitter、Facebook、新聞、GDELT 資料庫等
* **動態關鍵字擴展**：自動擷取新興熱門詞彙
* **抗議活動識別**：例如罷工訊息偵測
* **階層回歸模型（Cascade Regression）**：追蹤網路招募與擴散路徑
* **體量模型（Volume-based Model）**：使用 LASSO 方法分析異常詞彙激增
* **基線模型（Baseline Model）**：以歷史 GSR 事件為對照進行評分與匹配

---

## 八、流感疫情預測模型（Flu Forecasting）

### 模型目標：

* 利用社群媒體資料來模擬流感疫情的擴散與演化
* 運用疾病傳播機制，建立即時線上模型

### 架構簡介：

模型分為多層次損失函數（Loss Function）：

1. **監督式損失（Supervised Loss）**：健康狀態 vs. 語意層模型
2. **雙空間不一致損失（Bispace Inconsistency Loss）**：模擬世界與社群媒體世界的偏差
3. **時間樣式損失（Temporal Pattern Loss）**：捕捉時間序列異常
4. **傳染期損失（Infectious Period Loss）**：預測傳染期長短的準確性

目標為最小化總損失函數：
`min ℒ = ℒA + ℒB + ℒC + ℒD`

---

## 九、結論與未來應用

本報告展示了 AI 模型如何融合開放資料、社群媒體、新聞與歷史事件，以提升對社會動盪、公共衛生事件的預測能力。透過：

* 高回召率的模型融合設計
* 自動化事件時間與地點比對機制
* 質量與領先性的多維評估指標
* 應用於抗議預測與流感預警的真實案例

這些技術展示了 AI 在**公共安全與健康領域預警系統中的潛力**，未來可應用於政府決策、災害應對與流行病控制等多元場景。
