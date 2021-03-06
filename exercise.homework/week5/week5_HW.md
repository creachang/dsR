---
title: "Week5: Homework"
author: "姓名 / 學號 / 系所 /"
output: html_notebook
---

# 作業一 (100 pt)
### (個人作業)

> 安裝、載入與觀察以下資料，回答接下來的問題。


```r
# install 'LanguageR'
library(languageR)
ncol(english)
nrow(english)
# list observed variables and observations (words)
colnames(english)
rownames(english)

# view / edit data (caution: this will modify the 
# data frame (via Data editor); no undo available!) 
# fix(english)

# it's safer to store the modified data frame in 
# a different variable
# e2 <- edit(english)

# show individual observations (by row number of subject name)
english[1:5,]
english[c(1,3,7),]

# this might help the proper display (can write into .Rprofile as initial setup, 
# check ?Startup)
options(width=65, digits=2)

# observations for a single variable form a 
# vector (numeric or factor)
english$Word
english$WrittenFrequency

# combine vectors of identical length into new data set
eng1 <- data.frame(word=english$Word, pos=english$WordCategory, frequency=english$WrittenFrequency)

eng1[1:10,]

# if all vectors are variables from a single
# data set, we can use the following command to preserve row names
eng2 <- english[, c("Word", "WordCategory", "WrittenFrequency")]
eng2[1:10,]
```


> 問題：將 `eng2` 中 `WrittenFrequency` 小於 1 的詞抽取出來，連同該詞頻率儲存成一個 csv 檔案（檔名為 `low-words.csv`）。



------


# 作業二 (20pt) 自己的問卷自己分析
### (團體作業)
  
- 自製問卷 (typeform 或 google doc) 與內容，存成 csv 檔。
- 讀入 R，用你們學到的東西進行 (各種) 探索與分析。 

------

# Datacamp :
- [Intermediate-R](https://www.datacamp.com/courses/intermediate-r)
- [Writing functions](https://www.datacamp.com/courses/writing-functions-in-r)
