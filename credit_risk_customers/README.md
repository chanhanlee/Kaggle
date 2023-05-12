# credit_risk_customers
##前面先簡單敘述型統計、特徵圖表->模型建立
### 模型流程圖 Flowchart

```flow
st=>start: 模型選取
op=>operation: 特徵處理、超參數調整
cond=>condition: 驗證結果是否洽當
e=>end: 最終模型

st->op->cond->
cond(yes)->e
cond(no)->op
```

