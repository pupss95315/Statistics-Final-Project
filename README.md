# 各國健康照護狀況與新冠肺炎確診病例數關聯

### 研究問題
新冠肺炎確診率是否與該國健康照護體制的完善度有關聯；若兩者之間有關聯，是否可以用多變數回歸模型分析。

### 假說
健康照護制度越完善之國家，國內確診病例數較少。

(高比例的人均健康支出、高醫護人員占比、高疫苗接種率、高 HDI 之國家，有較低的確診率)

### 研究方法
#### 1. 盛行率定義與範圍
* 由於時間考量，盛行率僅考慮確診率，不考慮死亡率與篩檢率
* 僅取在所有資料集都有出現的國家與地區，最後只保留 109 個國家或地區
* 由於刪除部份資料，此報告可能存在代表性誤差
#### 2. 資料集描述
* 健康照護衡量標準：各國健康支出、醫護人員比例、HDI 等數值
* 新冠肺炎盛行率：政府通報之確診率
* 使用 Kaggle 上的資料搭配 WHO 的資料
* 詳細資訊見參考資料
#### 3. 資料視覺化
* box plot
* scatter plot
#### 4. 迴歸分析
* 單變數
* 多變數
#### 5. 假設檢定
均假設 $\alpha = 0.5$

### 變數
1. 人均衛生支出（USD）
2. 人均衛生支出（使用平均購買力校正，國際元）
3. 每千人有幾個醫師（醫生密度） 
4. 每千人有幾個護士和助產士（護理士密度）
5. 每十萬人有幾個專科手術人員（專科手術人員密度）
6. 國家／地區 HDI 數值
7. 卡介苗施打率（%）
8. 預期壽命
9. 預期就學年限
10. 平均就學年限
11. 人均國民總收入
12. Latitude: 地理緯度（°）
13. Density: 平均人口密度
14. 人口中位數
15. 都市人口比例（%）
### 結論
* HDI、專科手術人員密度與醫生密度為相關係數前三高的變數
* 卡介苗施打率與確診率無相關
* 目前 Model 能達到 Adjusted R^2 = 0.376，有 9 個變數無法通過 t-test，有潛在多重共線性問題
### 參考資料
* Devakumar kp，A brief comparative study of epidemics，上網日期：2020.05.20，https://www.kaggle.com/imdevskp/a-brief-comparative-study-of-epidemics/input。
* SRK，Novel Corona Virus 2019 Dataset，上網日期：2020.05.20，https://www.kaggle.com/sudalairajkumar/novel-corona-virus-2019-dataset?select=time_series_covid_19_confirmed.csv。
* Dan Evans，World Bank WDI 2.12 - Health Systems，上網日期：2020.05.20，https://www.kaggle.com/danevans/world-bank-wdi-212-health-systems。
* WHO，WHO vaccine-preventable diseases: monitoring system. 2019 global summary，上網日期：2020.05.20，https://apps.who.int/immunization_monitoring/globalsummary/countries?countrycriteria%5Bcountry%5D%5B%5D=AFG。
* UNDP，Human Development Reports，Table 1. Human Development Index and its components，上網日期：2020.05.20，http://hdr.undp.org/en/composite/HDI。
* Tanu N Prabhu，Population by Country - 2020，上網日期：2020.05.20，https://www.kaggle.com/tanuprabhu/population-by-country-2020。

Github page 網址 : https://pupss95315.github.io/Statistics-Final-Project/
