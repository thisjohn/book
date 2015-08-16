# 從 backbone 進化成 React
by Austin Huang

##

畫面美觀 vs. 速度夠不夠快

## Version 1: backbone.js

- ViewManager: Trigger event notfication
- One click will trigger too many event notification

        grep "on:coscup" // so terrible

- inheritant + mixin + events + so free = 只有作者懂
- 文件 其實難以描述複雜的 event pub/sub, 自己看 code 或直接問比較快

## Version 2: react.js + backbone.js

- 新舊版同時運作 oh no
- JSX vs. template
    - React lifecycle (東西只能有一個流向，不能交互流)
    - 統一的目錄結構
- 用目錄切割 backbone 及 react
- 未來直接刪除 backbone
- 禁止在 react 使用 backbone 相關檔案
    - 改寫成本極高
    - 未來無法順利刪除 backbone

- Router 是 backbone 及 react 唯一的交集
- 聚合取代繼承

- flux ---> fluxxor

避免用 event + jQuery 實作

## Version 3: react.js + flux.js

- 調整 module import 的方式

## Take out

- 整理目錄
- 切割頁面, 搞定 routing
- 共用元件

