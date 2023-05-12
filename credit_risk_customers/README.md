# credit_risk_customers
## 選用模型:邏輯斯迴歸、貝式分類器、K近鄰法、決策樹 XGBOOST
```
Model: LogisticRegression
Accuracy: 0.725
                precision    recall  f1-score   support

         0.0       0.56      0.31      0.40        59
         1.0       0.76      0.90      0.82       141

    accuracy                           0.73       200
   macro avg       0.66      0.60      0.61       200
weighted avg       0.70      0.72      0.70       200
```
--------------------
```
Model: GaussianNB
Accuracy: 0.72
              precision    recall  f1-score   support

         0.0       0.52      0.61      0.56        59
         1.0       0.82      0.77      0.79       141

    accuracy                           0.72       200
   macro avg       0.67      0.69      0.68       200
weighted avg       0.74      0.72      0.73       200
```
--------------------
```
Model: KNeighborsClassifier
Accuracy: 0.73
              precision    recall  f1-score   support

         0.0       0.56      0.39      0.46        59
         1.0       0.77      0.87      0.82       141

    accuracy                           0.73       200
   macro avg       0.67      0.63      0.64       200
weighted avg       0.71      0.73      0.71       200
```
--------------------
```
Model: DecisionTreeClassifier
Accuracy: 0.65
              precision    recall  f1-score   support

         0.0       0.41      0.41      0.41        59
         1.0       0.75      0.75      0.75       141

    accuracy                           0.65       200
   macro avg       0.58      0.58      0.58       200
weighted avg       0.65      0.65      0.65       200
```
--------------------
```
Model: XGBClassifier
Accuracy: 0.8
              precision    recall  f1-score   support

         0.0       0.70      0.56      0.62        59
         1.0       0.83      0.90      0.86       141

    accuracy                           0.80       200
   macro avg       0.77      0.73      0.74       200
weighted avg       0.79      0.80      0.79       200
```
--------------------
[========]


## 最終選定模型XGBOOST
前面可以看出，模型準確率大約可以到達0.8
我們模型對於**信用良好**的預測準確率相當好，RECALL達到0.90
但信用不佳的只有0.56
這邊利用**調整權重**的方法，讓信用不良的擁有較大的權重。
調整後
雖然整體準確率降到0.78，但對於信用不良的**準確度有大幅上升**，
但我認為這運用在**風險模型**上可能還是不太適合，畢竟信用不佳的對象我們應該不希望會輕易的被我們判斷為信用良好。
```
Test set classification report:
              precision    recall  f1-score   support

         0.0       0.62      0.64      0.63        59
         1.0       0.85      0.84      0.84       141
```
```
Test Metrics: Accuracy = 0.78
Recall = 0.8368794326241135
Precision = 0.8489208633093526
F1-Score = 0.8428571428571429
```

