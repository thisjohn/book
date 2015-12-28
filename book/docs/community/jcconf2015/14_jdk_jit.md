# JDK8 JIT 行為和效能分析

當系統增長時, VM 就是系統效能, 安全性, ...的瓶頸

## JVM

- Execute bytecode first
- Interpretation -> Profiling -> Dynamic Compilation (JIT) -> Deoptimization

## JIT

Just-in-time compiler

## OSR, on-stack replacement

## Template based interpreter

- HotSpot
- InterpreterMacroAssembler

- JITWatch

##

- Inline
- Escape analysis
- Performance tuning
