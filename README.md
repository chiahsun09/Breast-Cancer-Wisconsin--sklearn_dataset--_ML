Breast Cancer Wisconsin使用sklearn_dataset 資料做機器學習

Breast Cancer Wisconsin (sklearn_dataset) _ML_結論.jpynb 
內容包含:

1.資料探索分析
2.使用Autosklearn來做模型選擇判斷
3.GridSearchCV做超參數選擇
4.過取樣資料集測試
5.使用隨機森林,RFECV,LinerarSVC來挑選主要特徵
6.結論:

特徵降為5個,與原先30個特徵去跑,準確率和召回率有降一些,但還是有90%以上。
一開始看的heapmap有極強的正向關係,但後續被被程式所捨棄,代表降維可擇一即可。


影響最大的特徵為:

mean concave points	凹縫（輪廓的凹部分）平均值

radius error 半徑（點中心到邊緣的距離）標準差

worst radius 半徑（點中心到邊緣的距離）最大值

worst texture 文理（灰度值的標準差）最大值

worst concave points 凹縫（輪廓的凹部分）最大值


當用所有元素下去跑準確度會較高，但在需由使用者填入資料的情況下，
使用者需要輸入資料越少,對使用介面越友善。

基於準確率為可容許的程度下，用這5個元素下去作預測APP。

ps.要在LocalHost跑streamlit app,請參考另一個檔案
Run streamlit on Colab without Ngrok(LocalTunnel) .ipynb
內含測試資料集iris和Brease cancer

 