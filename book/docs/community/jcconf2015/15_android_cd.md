# 持續交付在 Android 

CD (Delivery) = CI (Integration) + CTA (Test Automation) + CD (Deployment)

**C = Continuous*

- CD - 打破 Dev 和 Ops 的牆?
- 持續交付：某件事很痛苦，就一直做它
    - 交付很痛苦，所以就用自動化交付每天做

## Practices

- Continuous integration
- Commit stage testing
- Acceptance stage testing
- Automatic deployment

## Android CI

- Jenkins
    - How to test all OS?
- Debug vs Release
    - Unit test: debug build
    - Acceptance test: release build

## Android Commit State Testing

- Android Unit Test + [Roboletric](http://robolectric.org/) + [Mockito](http://mockito.org/)
    - Code review 確認 是不是真的有做
- NOOOOO sleep
- Model-View-Presenter
    - Activity/Fragment code 愈少愈好
    - 把邏輯放到一個或多個 Presenter classes
- 80%+ coverage
- (static analytics, lint 全開)

## Android Acceptance stage testing

- [Espresso](http://developer.android.com/intl/zh-tw/tools/testing-support-library/index.html#Espresso) + [Cucumber](https://cucumber.io/) Android
- Smoke test
- 穩定度 (UI automation test)
    - 1% 失敗率 * 100 次 test = 64% 失敗率
    - 每次都要過!!!!!
    - 要超級穩定
- 速度非常重要
    - 太久要如何 CD
- 自動化測試和產品 code 同樣重要
- 詳細的 log

## 測試金字塔

1. UI (10%)
1. Service (20%)
1. Unit / Component (70%)
    - 大部分 應該要用 unit test

## Pipeline 紀律

- Test 失敗: Severity 1 defect 所有人都要去解決它
- CD 前要先在 local 跑過測試
- CD 後要確定 commit stage 過了才能做別的事
- code build/test fail
    - 15 分鐘解決 不行就 revert
- build/test fail 就鎖住 source control

## 重要觀念

- Pipeline 紀律很重要，但很難達成
- 沒有所謂 CD 負責人，每個人都要參與
- 人 > 流程 > 工具
- 持續有力的高層
- 絕非幾個月可以達成
    - coverage 上來後，才會明顯
