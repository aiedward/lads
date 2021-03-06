---
title    : Linguistic Analysis and Data Science
subtitle : lecture 08
author   : 謝舒凱 Graduate Institute of Linguistics, NTU
mode     : selfcontained # {standalone, draft}
url      : {lib: "../../libraries", assets: "../../assets"}
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
lecnum   : "03"
widgets     : [bootstrap, quiz, interactive, mathjax]  # {mathjax, shiny, bootstrap}
ext_widgets: {rCharts: [libraries/widgets/nvd3]}
knit     : slidify::knit2slides
bibliography: /Users/shukai/LOPE_LexInfo/BIB/corpus.bib
github      : {user: loperntu, repo: lads}


--- bg:#FFFAF0
## 大綱

1. __**Statistics and Machine Learning 101**__
2. Text classification using `RTextTools`



---bg:#FFFAF0
## Review


- Preparing / Preprocessing text and data. Text is unstructured or partially structured data that must be prepared for analysis. We extract features from text. We define measures. Quantitative data are often messy or missing. They may require transformation prior to analysis. Data preparation consumes much of a data scientist’s time.

- Exploratory data analysis and Infographics (data visualization for the purpose of discovery. We look for groups in data, find outliers, identify common dimensions, patterns, and trends.)

- __**Prediction models**__ (Regression; Classification and Clustering; ) and __**Evaluations**__  (Recommender systems, collaborative filtering, association rules, optimization methods based on linguistic heuristics, as well as a myriad of methods for regression, classification, and clustering fall under the rubric of **machine learning**).


---
## 統計


<img style = 'border: 1px solid;' width = 70%; src='./assets/img/tm_sta.png'></img>



---
## 文本統計 (Textual Statistics)

- 文本統計學的知識
- 相似與關聯為例





---
## 機器學習

- AI 的一個子領域。（參見林軒田老師的線上課程）
- 監督式 supervised vs. 非監督式 unsupervised
  - 可以用中文斷詞問題來想
  - [圖解法入門](http://www.r2d3.us/visual-intro-to-machine-learning-part-1/)：基本概念與決策樹



---
## 機器學習：效能評估的基本量度

- Recall 
- Precision 
- F-score

<http://www.cnblogs.com/bluepoint2009/archive/2012/09/18/precision-recall-f_measures.html>

---
## Annotation and Feature Engineering 

- Study of recorded human communication
- Summary and quantitative analysis of communicated messages
- Researcher looks for patterns/themes in text; <span style="color:green; font-weight:bold">develops `code frame` to categorize text.</span>
- Essentially, variables are extracted from text: Based on scientific method; establishes objectivity via inter-coder reliability.



---
## Annotation and Feature Engineering: Pros and Cons

優點
- flexible; theoretically-motivated annotation/code frame effrots
- can apply to texts, speech, video, etc.
- 可以用來解決一般機器學習系統 high precision low recall 的問題。把潛在的語意與情緒發掘出來。

缺點
- manually intensive
- thus can be expensive



---
## 手工標記資料  

- 最簡單可以用 **Excel** 來做：
  - One (or more) column(s) for text data； One column for topic label (as `gold standard`)
  - 通常至少有多於 3000 份標好的文件。

- 大型的專案要考慮到永續、相容、交換等問題，建議使用標記系統。
  - 語料庫和語言處理社群 `GATE`  
  - 質性研究社群 `CAT (Coding Analysis Toolkit)`
  - [lopetator](http://lopen.linguistics.ntu.edu.tw:8001/lope.anno/)

- labeling 和 annotation 的差異之後再談。

---
## 機器學習程式實作基本流程

- [`create_matrix`] Import your hand-coded data into R
- [`create_corpus`] 把「不相關」的資料移除，建立訓練語料 (training dataset) 與測試語料 (test data)
- [`train model(s)`] Choose machine learning algorithm(s) to train a model
- [`build classification model(s)`] Test on the (out-of-sample) test data; establish accuracy criteria 了解成效。
- [`apply classification model(s)`] Use model to classify novel data
- [`create analytics`] 把自動分錯的資料找出來 Manually label data that do not meet accuracy criteria


--- bg:#FFFAF0

1. Statistics and Machine Learning 101
2. __**Text classification using `RTextTools`**__



--- 
## 文本分類

- `RTextTools` 可自動化某些標記工作，與監督式文本自動分類。簡單，但是有記憶體問題，中文支援有問題。
- "One-stop-shop for conducting supervised machine learning with textual data" 邊看[這篇](http://journal.r-project.org/archive/2013-1/collingwood-jurka-boydstun-etal.pdf)邊做看看. [參考程式範例](week9_RTextTools_congress.R)




---
## Kaggle for Midterm.Mini-Hackathon

- Kaggle: the home of data science [連結](kaggle.Rmd)
- 本週自己再看看 kaggle 怎麼運作。 


