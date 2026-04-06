# social-sentiment-analysis

> 使用 NLP 技術分析 PTT 社群輿論與情緒變化

---

## 專案說明
主要針對 PTT 八卦版「三峽車禍事件」進行社群媒體分析，透過自然語言處理（NLP）技術，分析網路輿論的討論內容與情緒變化趨勢。資料蒐集期間為 2025/5/15 至 2025/6/10，共分析 1216 篇文章。

---

## 專案目標
- 分析社群平台對重大事件的討論內容  
- 觀察情緒隨時間的變化趨勢  
- 找出關鍵詞與主要討論主題  
- 建立完整中文文本分析流程  

---

## 使用技術
- Python  
- CKIP（中文斷詞 / NER / POS）  
- SnowNLP（情緒分析）  
- Pandas  
- Matplotlib  
- WordCloud  

---

## 分析流程

### 1. 資料蒐集
- 平台：PTT 八卦版  
- 關鍵字：三峽車禍、交通事故  
- 時間區間：2025/5/15 ～ 2025/6/10  

### 2. 資料前處理
- 中文斷詞（CKIP）  
- 去除停用詞（stopwords）  
- 詞性標註（POS）  
- 命名實體辨識（NER）  

### 3. 分析方法
- 詞頻分析（LIWC）  
- 主題模型（Topic Modeling）  
- 情緒分析（正向 / 負向）  
- 時間序列分析（每日情緒變化）  

---

## 分析結果

### 關鍵詞分析
高頻詞集中於「車禍」、「駕駛」、「事故」、「醫院」等，顯示討論主要圍繞事件本身、責任歸屬與後續處理情況。

### 主題分析
透過主題模型可觀察到討論內容主要分布於幾個面向：
- 高齡駕駛與駕照制度  
- 車禍事件經過與現場情況  
- 政府與媒體回應  
- 傷者與醫療資源  

### 情緒分析
整體情緒在事件初期呈現明顯負向，隨時間逐漸趨於中性，顯示討論熱度與情緒強度同步下降。

---

## 分析圖表

### 文字雲
<img alt="image" src="https://github.com/user-attachments/assets/f9d5e153-81c2-4c72-b92c-e1b8cffab60c" width="50%" />

### 主題建模
主題1（駕駛、高齡、換照、70歲）、主題2（三峽、車禍、現場、學生、完整）、主題3（天堂、身體、老翁、詐騙、賴清德）、主題4（肇事、發生、78、開車、完整）、主題5（家屬、醫院、侯友宜、北市、傷者）
<img src="https://github.com/user-attachments/assets/bc5b5a8a-06c6-43e0-a47e-1f9fd0b835b8" width="90%" />

### 正負向緒詞每日出現趨勢
<img alt="image" src="https://github.com/user-attachments/assets/149ad563-bdec-42a8-b94c-4eca5f612cb1" width="50%" />

### 每日平均情緒趨勢
<img alt="image" src="https://github.com/user-attachments/assets/60ea3447-9126-4432-b076-e85432d8c4fe" width="50%" />

### 正負向緒詞彙統計
<img alt="image" src="https://github.com/user-attachments/assets/921bd182-d873-4df1-b5c9-9724eb943856" width="70%" />

### 每日情緒文章量趨勢
<img alt="image" src="https://github.com/user-attachments/assets/a4895baa-8f46-486a-904a-92844a6b937a" width="70%" />

---

## 總結

透過詞頻分析（LIWC）、主題模型（Topic Modeling）與情緒分析（SnowNLP），本研究發現事件於 5/20 達到輿論高峰，且討論內容主要集中於高齡駕駛與責任歸屬等議題。隨著時間推進，情緒分析結果顯示整體情緒由初期的負向逐漸轉為中性，而主題模型亦反映討論重心由情緒性反應轉向制度與實務層面的議題，包括駕照制度、媒體與政治回應，以及醫療處理效率等。

整體而言，透過上述分析方法可觀察到社群輿論由短期情緒宣洩，逐步轉為較理性且聚焦公共議題討論的變化趨勢。
