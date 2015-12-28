# Immutable Infrastructure：觀念與實作

在虛擬化及雲端時代，“immutable infrastructure” 也成為新一代的顯學。

在資源及流程的充分配合下，這將會大大簡化系統的複雜度，穩定性也會大大提升

@@: 赤壁賦 Entropy 化學 熵 物理 亂度 生物 有絲分裂 醫學 白血病
@@: 電腦是世界的一個成份 電腦界 電腦也是在物理界

    變 vs. 不變

    自其變而觀之...

In OOP and FP, an immutable object is an object whose state cannot be modified after it is created.

        String s = "ABC";
        s.toLowerCase(); // s is still "ABC"
        // s is immutable

不要去碰原來的東西。另外再開一個比較好處理

@@: 舉有夠多例子 唷

## What is immutable infrastructure?

- re-create images each time you change a line of code
- prevent (or track) modifications of running images

## Why not immutable infra?

- Cost可能太高 
- DevOps maturity level: 流程不順的話

## 母體: image

- VM image
    - 肥大
- docker image
    - 不安全. 共用 Host OS
- container per VM
- Unikernel image: library operating system
    - boxfuse

## 增生: new intance

## 替換: deplyment

- Docker ecosystem is easier yo~
- continuous delivery
- livelessons continuous delivery by jez humbie

## 自動化: DevOps

- jenkins
- ansible
- circleCi, travisCi, ...

## References

- [slide](http://www.slideshare.net/williamyeh/immutable-infrastructure-55828718)
