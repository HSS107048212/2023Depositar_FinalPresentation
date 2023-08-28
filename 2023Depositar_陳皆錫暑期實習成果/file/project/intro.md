# 以維基資料註記的資源的敘述、探索、呈現
WikidataCon 2023 https://pretalx.com/wikidatacon2023/

## 1. 運用Cosine Similarity計算Wikidata關鍵字Qids' Pids、Qids、en-label發展關鍵字推薦模式——以Depositar為例
* 專案說明：0802提案投影片 https://docs.google.com/presentation/d/11zfsz9IAYfXCh_A1UzYefOqR3pf3FXzvs9PRRD4S4Og/edit#slide=id.p
* GitHub https://github.com/HSS107048212/2023Depositar_WikidataItem_CosineSimilarity

## 2. 雙層社群網絡應用於Wikidata關鍵字發展Depositar資料集推薦系統
* 資料管理平台的機會點： 三個資料管理平台 X 四種使用場景體驗、比較與發現。 https://docs.google.com/presentation/d/1HnGY1g91t-_Zegbjyjh-g2EH8Bm-e11lBC-tduLWoVw/edit?usp=sharing
    * 國網中心資料集平台 https://scidm.nchc.org.tw/dataset/cdc-aagstable-19cov
    * 政府資料公開平台 https://data.gov.tw/
    * Depositar https://data.depositar.io/en/
* Github https://github.com/HSS107048212/2023Depositar_Datasets_RecommmandationSystem
* 0816進度說明投影片 https://docs.google.com/presentation/d/1Zw4TNZis1Ye2jPXekkpSOQdrP2YiCrCdVgI8NV_cvOA/edit#slide=id.p

## 3. DMP視角下，基於CKAN機制的Depositar資料集與Wikidata關鍵字的資訊儀表板
* Github https://github.com/HSS107048212/2023Depositar_Dashboard_Hvplot
* 0816進度說明投影片 https://docs.google.com/presentation/d/1Zw4TNZis1Ye2jPXekkpSOQdrP2YiCrCdVgI8NV_cvOA/edit#slide=id.p

## 4. 以「類別資料」視角，運用Wikidata關鍵字的Property實現餘弦相似度推薦Depositar資料集
* Github https://github.com/HSS107048212/2023Depositar_Catagorical_RecommmandationSystem

## 5. JupyterBook呈現2023中研院Depositar實習成果
* Github https://github.com/HSS107048212/2023Depositar_FinalPresentation
* 線上網頁 https://hss107048212.github.io/2023Depositar_FinalPresentation/intro.html

## 專題建議：
* 使用「時間複雜度」去顯示說明，而不是以「150分鐘版本」進行說明。
* 如果Wikidata的填寫者不同，那麼讀取的資料就不同，所以可以Depositar導入。
* 「後分類」對管理者的啟發是什麼？
    * 後分類（post-classification）指的是在查詢後將檢索結果進行分類和呈現的過程。它根據時間、來源、作者等屬性將檢索結果進行分類，幫助使用者更好地導覽和決定下一步動作。一種應用方法是使用「標籤樹」框架，該框架通過組織關鍵詞並賦予其明確的屬性（如名稱、地點、時間）來增強結果的呈現和使用者理解。這是管理和簡化大量檢索結果的工具，使使用者更輕鬆地與檢索到的信息互動和利用。
    * 「檢索後分類」 (post-query classification) 指的是，對 R(q) 進行分類，並將分類的結果呈現給使用者，讓使用者決定接下來要做什麼動作？