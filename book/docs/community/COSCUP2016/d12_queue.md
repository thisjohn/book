# Queue

## Some...

- celery
- RabbitMQ
- Resque
- ...

## Hello Resque!

- Job

    描述 worker 執行的方式，由一個 class 封裝而成 *(setUp, perform, tearDown)*

- Worker

    執行已經定義好的 job

- Queue

- Scheduler

    搬運 job 到 worker

## 問題

- Q 不同環境要不同的設定檔
    - php-resque-pool: only one *yaml config*

- Q Redis 作 backend
- Q resque-pool 是白名單
    - *

