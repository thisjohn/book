# 使用 Java 的 Future/Promise API 來撰寫非同步程式

## 長時間

- IO
- network
- encry/decry
- image process
- ...

## Think about...

如果有許多 task, 都要在背景執行...

- 一個等一個: callback hell
- 全部包在同一個: 不利組合 再利用
- 想要 2 個任務的結果: join?

不要再用這種古老的寫法 Thread!?

## Future

- 控制權在 caller 身上。有拿到 Future
- future.get() 仍然需要檢查。浪費一個 thread?

## CompletableFuture (Java 8)
## Good good

- event driven
- easy to compose
- 控制權傳回給呼叫者
- 滅少 thread 浪費

## Android

- Guava ListenableFuture
- RxJava
- bolts-android
- lambda

