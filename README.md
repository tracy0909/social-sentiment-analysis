# social-sentiment-analysis

> 使用 NLP 技術分析 PTT 社群輿論與情緒變化
<br>

## 專案說明

本系統以 PTT 八卦版「三峽車禍事件」為案例，透過自然語言處理技術，整合資料蒐集、文本前處理、斷詞、特徵擷取與情緒分析等模組，建立一套完整之中文文本分析流程。系統針對社群文章內容進行語意處理與特徵分析，萃取關鍵詞與主題資訊，並結合情緒分析結果，進一步觀察輿論隨時間之變化趨勢，以掌握社群對事件之討論焦點與情緒演變。
<br><br>

## 系統架構

```text
PTT Data
   ↓
Data Collection
   ↓
Preprocessing (CKIP)
   ↓
Feature Extraction
   ↓
Analysis Module
   ├─ Keyword Analysis
   ├─ Topic Modeling
   ├─ Sentiment Analysis
   ↓
Visualization
```

## 模組說明

### 1. 資料蒐集

本模組負責自 PTT 八卦版蒐集與本研究主題相關之文章資料，透過關鍵字「三峽車禍」、「交通事故」進行篩選，資料蒐集期間為 2025/5/15 至 2025/6/10，共取得約 1216 篇文本資料，作為後續分析基礎。


### 2. 前處理模組 Preprocessing

針對原始文本進行清理與語言處理，以提升資料品質與分析準確度。主要包含中文斷詞（CKIP）、停用詞移除（Stopwords）、詞性標註（POS Tagging）及命名實體辨識（NER），將非結構化文本轉換為可分析之語言單位。


### 3. 特徵處理 Feature Extraction

本模組將處理後之文本轉換為結構化特徵，包含詞頻統計（Term Frequency）、關鍵詞擷取與語意特徵整理，並建立適用於後續分析之資料表示形式，以支援不同分析方法之應用。


### 4. 分析模組

本模組負責對文本資料進行多面向分析，包含關鍵詞分析、主題建模與情緒分析，以全面理解社群討論內容與變化趨勢。

- **關鍵詞分析 Keyword Analysis**  
  透過詞頻統計方法辨識高頻詞彙，進一步分析社群討論焦點，例如車禍事件、駕駛責任與醫療處理等議題。

- **主題模型 Topic Modeling**  
  透過主題建模技術將文本分群，萃取潛在語意主題，以辨識不同討論面向，如高齡駕駛、政策制度及媒體回應等。

- **情緒分析 Sentiment Analysis**  
  使用 SnowNLP 對文本進行正負向情緒判斷，並計算每日平均情緒分數，分析輿論情緒隨時間之變化趨勢。


### 5. 視覺化

將分析結果以圖表方式呈現，包含文字雲（WordCloud）、主題分布圖、情緒趨勢圖及詞彙統計圖等，使分析結果更具可讀性與解釋性，並利於觀察整體輿論變化。

---

## 使用技術

* Python
* CKIP（斷詞 / NER / POS）
* SnowNLP（情緒分析）
* Pandas（資料處理）
* Matplotlib（資料視覺化）
* WordCloud

---

## 分析結果

* 討論高峰出現在 5/20，關鍵議題集中於：
  * 高齡駕駛與駕照制度
  * 車禍責任歸屬
  * 政府與媒體回應
* 情緒趨勢由初期明顯負向，隨時間逐漸趨於中性

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

透過詞頻分析（LIWC）、主題模型（Topic Modeling）與情緒分析（SnowNLP），發現事件於 5/20 達到輿論高峰，且討論內容主要集中於高齡駕駛與責任歸屬等議題。隨著時間推進，情緒分析結果顯示整體情緒由初期的負向逐漸轉為中性，而主題模型亦反映討論重心由情緒性反應轉向制度與實務層面的議題，包括駕照制度、媒體與政治回應，以及醫療處理效率等。

整體而言，透過上述分析方法可觀察到社群輿論由短期情緒宣洩，逐步轉為較理性且聚焦公共議題討論的變化趨勢。

