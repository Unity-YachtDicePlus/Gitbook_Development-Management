---
noRobotsIndex: true
layout:
  width: wide
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: false
  metadata:
    visible: true
---

# Git Flow 전략

#### GitFlow가 무엇인지?

#### 다른 전략과의 차이점은?

#### GitFlow 사용하는 이유

#### GitFlow 전략





main -> 배포전용\
develop -> main에서 뻗어나온 개발 흐름용\
feature/ -> 기능 개발용\
release -> develop에서 만족했으면 release 만들어서 쭉 테스트하고 main, develop에 각각에 합침\
hotfix -> 배포하고 급한 버그 발견했을 때 main에서 뻗어나와 진행. 그리고 다시 main, develop에 합쳐주기



항상 유지되는 브랜치: main, develop\
일정 기간 유지되는 브랜치: feature, release, hotfix

<figure><img src="../../.gitbook/assets/image.png" alt="" width="188"><figcaption></figcaption></figure>



