# 銀行客戶流失
資料來源:Kaggle
------------
Acknowledgements

As we know, it is much more expensive to sign in a new client than keeping an existing one.

It is advantageous for banks to know what leads a client towards the decision to leave the company.

Churn prevention allows companies to develop loyalty programs and retention campaigns to keep as many customers as possible

------------
### 1.DATA Preprocessing & 敘述性統計 & 視覺化
無缺值，進行單熱編碼，一些感興趣的特徵敘述性統計及繪圖

### 2.模型建立->模型選取
SVM、邏輯斯迴歸、決策樹、XGBOOST進行比較，最後選擇決策樹
因模型準確率都夠高，在此情形下 我選擇解釋性較佳的決策樹

從重要特徵篩選及最後決策樹流程圖可以看出，***有客訴過的客戶***相當大程度影響之後會不會離開，

因此銀行如能搶在客戶客訴前先解決客戶的問題，減少客戶的客訴比例，相信可以很大程度將客戶留住。

在***沒客訴過的客人***中，則以***信用卡的積點***、與***銀行來往的年限***最有關。

從這裡也可看出為何各家銀行都積極推廣信用卡業務，因為當客人使用本家的信用卡的積點越多則越不容易離開這家銀行。



