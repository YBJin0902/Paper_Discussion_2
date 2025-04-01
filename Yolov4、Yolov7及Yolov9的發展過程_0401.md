# Yolov4、Yolov7 及 Yolov9 的發展過程

### 設計物件偵測系統需考量的基本議題
1. Network architecture
2. Feature integration method
3. Detection method
4. Loss function
5. Label assignment method
6. Training method

</br>

### 設計的考量及策略
必須是 lightweight（輕量），效率要 快又準。</br>

可適用於各類平台：
1. Cloud
2. Local（如 Notebook）
3. Edge（如手機）

必須先調查現有的 State-of-the-art 物件偵測系統。

</br>

### Partial Residual Network 的變化
* 目的：減少運算與參數、維持連接、增加梯度組合
* 經過多層卷積與殘差連接的設計，用以優化網路的輸出與學習效率

</br>

### Layer-level 與 Stage-level 比較
一個完整的 stage 是從 backbone 組織不同層級資訊以完成任務。</br>

用於如：
* Small object detection
* Large object detection
在一個 stage 中的 gradient flow 是有意義的

</br>

### Motivation: YOLOv4 → YOLOv9
YOLOv4~v7：透過 gradient flow 學習多樣且一致的特徵！！</br>

YOLOv9：
* 最佳化 forward 與 backward path
* 解決 information bottleneck 問題