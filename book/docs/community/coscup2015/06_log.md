# 快快樂樂管理 Log
by edwardc

Logstash + Cloud Logging

## Log

- 會自己長大
- 儲存最小成本
- 不需要時垃圾，需要是黃金

- 資料少時
    - zip
    - grep
- 資料大時
    - ...

##

- splunk
    - 好貴
- ELK 
    - Elasticsearch: warehouse
    - Logstash: parsing
    - Kibana: front-end
- server 一直加
    - 精美的架構 + 精美的帳單

## Google Cloud Logging

- 儲存便宜但匯出 (to *BigQuery*) 要收費?
- 只接受 *GCE* / *GAE*
- 架一台 *GCE* (*fluentd*) 轉
- 5TB/day, 120MB/s with n1-highmen-2 (13 GB Ram) * 10
- 直接裝 google-fluentd, 轉的那台都省了

