# Binance API查询
 在binance API 现货交易查询2023-01-01至2023-03-15 BTC 4小时级别（一根k线代表4小时）的交易数据，开盘/收盘/最高价/最低价/交易量，并计算当价格有效涨/跌破MA20 （20根k线柱-4小时一根）的24小时内最大涨跌幅及收盘涨跌幅。

1，MA20 计算方式可查询google  
2，有效涨跌的定义：当价格涨/跌破MA20 后的24 小时内收盘价没有回到MA20 下方/上方  
3，API 文档 https://binance-docs.github.io/apidocs/spot/en/#spot-account-trade  

任务：  
1，获取该时段内开盘/收盘/最高价/最低价/交易量 五个指标的数据(task_1.csv)  
2，统计时间段内共有多少次涨破或跌破4小时级别MA20，有多少次有效涨破或跌破(task_2.txt)  
3，计算每次有效涨/跌破MA20后的最大涨跌幅及收盘涨跌幅(task_3.csv)
代码以及图表(task.ipynb)  

定义：  
最大涨跌幅：在涨破MA20后的24小时内，价格的最高价相对于涨破时的收盘价的涨幅。如果是跌破，则是最低价相对于跌破时收盘价的跌幅。  
收盘涨跌幅：在涨破/跌破MA20后的24小时后的收盘价相对于涨破/跌破时的收盘价的涨跌幅。
