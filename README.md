# Simpson-Classification
---
## Predict the Characters in the Simpsons
### 資料描述
使用資料從 The Simpsons 影集中擷取出來的照片
* About 1000 images per character
* Pictures are under various size , scenes
* not necessarily centered in each image and colud sometimes be with or cropped from other characters

### 要求
* 最差是隨便猜，此時的 CategoryAccuracy = 0.05
* 最好是全對：CategoryAccuracy = 1.00
### Submission File
對於每一個 ID 必須預測一個 character 的名稱，該文件包含標題，格式如下：
	
|      ID        |    character   			|
| -------------  | ------------- 			|
|       1        | abraham_grampa_simpson 	|
|       2        | apu_nahasapeemapetilon	|
|       3        | bart_simpson  			|
|       4        | charles_montgomery_burns |
|       5        | chief_wiggum  			|
|       6        | comic_book_guy   		|
|       7        | edna_krabappel  			|
|       8        | homer_simpson    		|
|       9        | kent_brockman  			|
|       10       | krusty_the_clown   		|
|       11       | lenny_leonard  			|
|       12       | lisa_simpson    			|
|       13       | marge_simpson  			|
|       14       | mayor_quimby   			|
|       15       | milhouse_van_houten   	|
|       16       | moe_szyslak   			|
|       17       | ned_flanders  			|
|       18       | nelson_muntz   			|
|       19       | principal_skinner  		|
|       20       | sideshow_bob    			|

### 檔案介紹
* 執行 train 檔
```
    terminal  >> python train.py
```
產生 dataset.h5 與 labels.h5 檔案，如已經執行產生後要再執行一次，將 save 改False、load 改 True
```
 get_read_main('./characters/',save=False, load=True)
```
* 執行 test 檔，會產生 predict.csv 此為預測資料
```
 terminal >> python test.py
```
* Confusion matrix.ipnb 內容為混淆矩陣圖，內部有一些位置會有相似情況而導致顏色較黯淡，代表我們的 model 對那兩個 Label 分辨還是不準確

![image](https://github.com/YochLin/Simpson-Classification/blob/master/%E6%B7%B7%E6%B7%86%E7%9F%A9%E9%99%A3%E5%9C%96-Simpson.JPG)

### 整體流程圖
![image](https://github.com/YochLin/Simpson-Classification/blob/master/%E6%B5%81%E7%A8%8B%E5%9C%96.jpg)

### Reference
* [Simpson](https://medium.com/alex-attia-blog/the-simpsons-character-recognition-using-keras-d8e1796eae36)
* [Simpson - Kaggle](https://www.kaggle.com/alexattia/the-simpsons-characters-dataset)

