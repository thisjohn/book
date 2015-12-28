# 阿里 JVM 的工作方向

改造 JVM

- 在不同的 BU 間共享資源 - 虛擬化的技術

T4 -  Base on LxC 的虛擬技術

- session-based GC

web request 結束後。整個 slab，就用完了?
不用一個一個檢查才是...

- 全自動異步化
    - Thread pool (X) - thread
    - Async (O) - coroutine

線程的切換，很花資源。異步化才能有效滅少IO？
代碼小是沒差, 建議用協程(coroutine)去寫

ref. [coroutine 入門](https://www.ptt.cc/bbs/GameDesign/M.1340896795.A.F29.html)

- 反序列化優化

- JIT Warm-up

Optimization profile save/load

- ZDebugger

- Profiling Support

CPU, memory, disk I/O, network I/O
