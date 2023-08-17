# 7月第四週
## July 24
* 完成OpenStreetMap 課前準備
* 檢索新竹市的大學
```overpass=
[out:json];
area["name"="新竹市"]->.boundaryarea;

(
  // 檢索所有大學
  node(area.boundaryarea)["amenity"="university"]; //無
  way(area.boundaryarea)["amenity"="university"]; //藍
  relation(area.boundaryarea)["amenity"="university"]; //紅
  

);

out center;

```
![](https://hackmd.io/_uploads/rJYaVuo93.jpg)


* 檢索 國立新竹教育大學

![](https://hackmd.io/_uploads/HJ6Fv_sc2.jpg)



* 檢索臺~~台~~北市的大學
```overpass=
[out:json];
area["name"="臺北市"]->.boundaryarea;

(
  // 檢索所有大學
  node(area.boundaryarea)["amenity"="university"]; 
  way(area.boundaryarea)["amenity"="university"]; 
  relation(area.boundaryarea)["amenity"="university"]; 
  

);

out center;

```
![](https://hackmd.io/_uploads/rkSLNuj5h.jpg)

* 使用QuickOSM在QGIS
![](https://hackmd.io/_uploads/BkvdIqoch.jpg)
    * Access denied: Forbidden: Map tiles are restricted to Wikimedia & affiliated sites only.  See https://wikitech.wikimedia.org/wiki/Maps/External_usage if you believe your usage supports the Movement. 

* 修改一個wikidata，以共享單車（bike-sharing system）為例
![](https://hackmd.io/_uploads/ByDgBisq2.jpg)
* 完成Wikidata 課前準備
* 觀看《chap4 4 橡皮伸縮法影像定位》


## July 25
* 觀看《chap4 7 影像轉換KML,KMZ套疊Google Earth》
    ==影片中提供轉換成KML的程式是**Windows**才能用==
* 觀看《chap5 1 向量資料圖徵融合》
    * **面資料：縣市邊界**
        * Before:
        ![](https://hackmd.io/_uploads/BkYfPonq2.jpg)
        * 操作：
            * 目的：僅保留縣市的行政疆界，而不是鄉鎮市區的疆界
            ![](https://hackmd.io/_uploads/Bk_cvih9h.jpg)
            * 操作：
                1. Vector
                2. Geoprocessing tool
                3. Dissovle
                4. Dissolved file : countyname
        * After:
        ![](https://hackmd.io/_uploads/ryQEPo3qn.jpg)


    * **線資料：MRT**
        * 使用QGIS內建的function expression進行資料欄位合併：
        ![](https://hackmd.io/_uploads/SygIP335h.jpg)
        * 依照合併完成的categories進行呈現
        ![](https://hackmd.io/_uploads/BJoXth353.jpg)
        ![](https://hackmd.io/_uploads/SyBdKn293.jpg)
* 觀看《chap5 2 向量資料環域分析》
    * **MRT**
    ![](https://hackmd.io/_uploads/HkFjsh35n.jpg)

    > 根據研究目的，設定dissolve result。
    ![](https://hackmd.io/_uploads/H19xnn2cn.jpg)

    > 根據研究目的，調整properties呈現方式。
    ![](https://hackmd.io/_uploads/SkWw33hqh.jpg)

    > 假設不同捷運站不同buffer
    ![](https://hackmd.io/_uploads/BJW4Thnqh.jpg)
    ![](https://hackmd.io/_uploads/HJuDT33c2.jpg)
    ![](https://hackmd.io/_uploads/SJlja32q3.jpg)

    > 依照不同捷運路線，分成不同顏色呈現
    ![](https://hackmd.io/_uploads/HyChyah9h.jpg)
    ![](https://hackmd.io/_uploads/HySwkp35n.jpg)

    * **面的環域**
    ==需要先將CRS坐標換成3826==
    ![](https://hackmd.io/_uploads/Hk7OW63c3.jpg)
    ![](https://hackmd.io/_uploads/BJtYWph52.jpg)



    * **多圈環域Multi-ring buffer (constant distance)**
    從Processing 選擇 tool 搜尋buffer，選擇Multi-ring buffer
    ![](https://hackmd.io/_uploads/SJzE7pnc2.jpg)
    ![](https://hackmd.io/_uploads/BJL9Epnq2.jpg)

    * **單邊環域Single sided buffer**
    從Processing 選擇 tool 搜尋buffer，選擇Single sided buffer
    ![](https://hackmd.io/_uploads/H1dqrT392.jpg)
    ![](https://hackmd.io/_uploads/S1mUrpn52.jpg)

* 觀看《chap5 3 向量資料套疊分析 Intersection》
==請留意「屬性資料」的變化==
輕軌捷運站
![](https://hackmd.io/_uploads/ByTZlZTc2.jpg)
輕軌路線
![](https://hackmd.io/_uploads/r19Xg-p5n.jpg)

* Intersection
![](https://hackmd.io/_uploads/HJ69e-p92.jpg)

* Eliminate selected polygons
    * Largest Area 與鄰近最大面積的行政區合併
    ![](https://hackmd.io/_uploads/rJi4Ub653.jpg)
    ![](https://hackmd.io/_uploads/SkTmuWT93.jpg)
    * Smallest Area 與鄰近最小面積的行政區合併
    ![](https://hackmd.io/_uploads/HJIxdbT52.jpg)
    * Largest common boundry 與最長接壤的行政區合併
    ![](https://hackmd.io/_uploads/S1b6_-ach.jpg)
* 參加人社中心組內會議


## July 26
* 製作[進度報告投影片](https://docs.google.com/presentation/d/1oGli2EMp6JpXtW5HknmrgzmGytq1TLXCE8a8ibzThE0/edit?usp=sharing)
* 觀看《chap5 4 案例統整練習：高雄市境內旅館、民宿、捷運站周邊的餐廳》
    ![](https://hackmd.io/_uploads/rkihdkAcn.jpg)
    * Merge兩個資料「國際旅館」、「民宿」需要注意是「相同的CRS系統」。不過測試時使用不同CRS似乎也順利產出圖片。
    ![](https://hackmd.io/_uploads/S1D7gl09h.jpg)
    * 透過「空間範圍」選取出「高雄境內」的「旅館」
    ![](https://hackmd.io/_uploads/SJoXMlC92.jpg)
    ![](https://hackmd.io/_uploads/SkfwmeA92.jpg)
    * 透過union產生「旅館與捷運」的篩選範圍
    ![](https://hackmd.io/_uploads/rkIR_gA92.jpg)
    ![](https://hackmd.io/_uploads/H1oxSgC5n.jpg)
    ![](https://hackmd.io/_uploads/Sy3EKgR92.jpg)
    * 透過「空間範圍」選取出「篩選範圍」的「餐廳」
    ![](https://hackmd.io/_uploads/BkpjweR5h.jpg)
* 參加OpenStreetMap教育訓練課程
* 參加「實習專題交流」
    * 用自己的話進行提案
    * 有幾個demo圖片、流程，以及成果
    * 從成果來說，我們可以怎麼做？
    * 期末報告要用Jupterbook來呈現depositar的資料可以透過Wikidata的關鍵字來呈現出來。
        * 互動的網頁。
        * 將整份專案放在Depositar上面給大家交接。


## July 27
* 完成Qfield作業
* 參加Wikidata教育訓練
* 完成OpenStreetMap作業


## July 28
* 完成Wikidata作業（除QuickStatement)
* 製作提案簡報
* 運用Python成功串接Depositar API，並輸入Wikidata API進行Qid與label的整理


## Addtional Helpers from Google

### OpenStreetMap
* [【岳世界】OSM開放街圖簡略操作教學分享](https://hiking.biji.co/index.php?q=review&act=info&review_id=5280)

### Geopandas
* [30天精通GIS資料分析-使用Python 系列](https://ithelp.ithome.com.tw/users/20107816/ironman/1797)
* [Geopandas](https://geopandas.org/en/stable/getting_started/install.html)
* [ImportError: No module named 'geopy' ipython-notebook](https://stackoverflow.com/questions/36064495/importerror-no-module-named-geopy-ipython-notebook)


### Overpass Turbo
* [以飲水地圖為例子 Overpass Turbo 查詢教學](https://www.youtube.com/watch?v=IPgqmNclMNg&ab_channel=OpenStreetMap%E5%8F%B0%E7%81%A3)
    * 了解Overapss的語法
    * 了解圖層如何呈現


### GIS
* [中央研究院：GIS應用支援工具集](https://gis.rchss.sinica.edu.tw/ISTIS/tools/)
