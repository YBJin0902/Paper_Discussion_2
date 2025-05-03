# The_complexity_of_strong_conflict_free_Vertex_connection_k_colorability

## 研究方法與定位

| 類別     | 特性          | 方法        |
| ------ | ----------- | --------- |
| 數學家    | 關心問題是否有解    | 數學證明      |
| 計算機科學家 | 關注理論運算與解的性質 | 數學證明 / 分析 |
| 計算機工程師 | 提出可行解決方案並實作 | 模擬 / 實驗驗證 |

</br>

## 科學方法介紹
1. Observation：觀察現象、提出問題
2. Hypothesis：提出解釋現象的假設
3. Experiment：進行實驗驗證假設是否成立
4. Analysis & Conclusion：分析並得出結論

</br>

## 問題定義：圖著色與連通問題
Graph Coloring</br>
定義：將圖中每個頂點分配顏色，使得任意相鄰的兩點顏色不同。</br>
數學式：對任意邊 (𝑢,𝑣)，需滿足 𝑓(𝑢)≠𝑓(𝑣)</br>

</br>

## Conflict-free Connection Coloring Problem
定義：對於任意兩點，存在一條路徑，其中有 某一種顏色的邊或頂點只出現一次。</br>
問題：是否存在一個 k-著色，使得所有點對間都存在此路徑？</br>

</br>

## 強衝突自由連通問題（Strong CF Coloring）
Shortest conflict-free path：符合上述條件，且為最短路徑。</br>

問題：對任意 𝐺 和整數 𝑘，是否存在 k-著色，使得任兩點之間存在強衝突自由最短路？</br>
推導：𝑠𝑐𝑓𝑐(𝑃𝑛)=1+𝑠𝑐𝑓𝑐(𝑃⌈𝑛/2⌉)=⌈log2𝑛⌉</br>

</br>

## 計算複雜度結果（NP-Hard）
透過從 3-SAT 問題 進行 reduction</br>
定理：3-svfc 問題在 3-colorable 圖上為 NP-Hard</br>

</br>