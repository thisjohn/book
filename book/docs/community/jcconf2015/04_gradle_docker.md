# 動手玩 Java 專案建置工具：以 Gradle 與 Docker 為例

## Docker toolbox

- `machine`
- `compose`: simply docker commands
- `swarm`: cluster

## Geb - [http://www.gebish.org/](http://www.gebish.org/)

- UAT test
- for web-based project
- use Groovy

## Gradle

- Install `sdkman`, Groovy enVironment Manager - [http://sdkman.io/](http://sdkman.io/)

        $ get.sdkman.io | bash
        $ source "$HOME/.sdkman/bin/sdkman-init.sh"

- Install `gradle`

        $ sdk install gradle 2.9

## Tests

1. Unit tests (Package, Library)
1. Integration tests (Application server)
1. GUI tests (e2e test)

## Testing with Jenkins CI

- daily build
- code committed
- pull request
- before staging: QA
- before release: production
- trigger manually

## References

- [hackpad](https://hackpad.com/JCConf-Taiwan-2015-Workshop-lKcJEMyjraR)
- [sample](http://github.com/TrunkWorkshop/jcconf-2015-java-docker)
