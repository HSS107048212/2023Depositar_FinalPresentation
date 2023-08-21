# Welcome to Jupyter Book

美好的時光總是令人覺得迅速又短暫，Depositar兩個月實習的充實生活即將進入尾聲。

其中，七月是教育訓練：Ubuntu、DMP、Github、QGIS、Qfield、OpenStreetMap、Culture landscape...每週紮實的教材與作業，讓我們即便從零開始，都能妥妥的學會基礎運用。

而「以維基資料註記的資源的敘述、探索、呈現」是在七月底與莊老師討論後選擇（6個題目）的專題方向，又或者說是專題的「概念」，至於怎麼做？甚至要從什麼角度理解這個題目？都令當時的我感受迷茫。
因此，閱讀更多的Wikidata介紹資料，並且更深入的理解「Wikidata之於Depositar」的特色之後，我發覺到「別的資料管理平台具備的功能，但可能現階段的Depositar還沒有出現的功能」於是想著先朝這個方向做做看...
以下是我先做的「背景脈絡」整理，進而發展的「程式實作」：
* 背景脈絡：
    * 「Wikidata是什麼？Wikidata關鍵字有什麼資訊？」從自由協作的結構化數據看。
    * 資料管理平台的機會點： 三個資料管理平台 X 四種使用場景體驗、比較與發現。
* 程式實作：
    * 運用Cosine Similarity計算Wikidata item的Property、Value、en-label發展關鍵字推薦模式——以Depositar為場域
    * 雙層社群網絡應用於Wikidata關鍵字發展Depositar資料集推薦系統
    * DMP視角下，基於CKAN機制的Depositar資料集與Wikidata關鍵字的資訊儀表板

透過上述「程式實作」的描述，運算從關鍵字的「Property、Value、en-label」運算相似度，再延伸到資料集，其實這種Bottom-up的方式因為要遍歷每一個細節，所以運算時長將近3個鐘頭，才可以算完「資料庫內的關鍵字」與「資料庫內的資料集」的相似度。
後來，經由莊老師建議，改從Top-down的視角，也就是直接從「資料集」的視角出發，蒐集單一特徵，進行相似度運算。實作之後，這樣的方法居然只耗時1分鐘就運算結束，真的是巨幅差異。

* 程式實作
    * 以「類別資料」視角，運用Wikidata關鍵字的Property實現餘弦相似度推薦Depositar資料集。


```{tableofcontents}
```
