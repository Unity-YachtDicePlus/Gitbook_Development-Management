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

# Github Flow 전략

## Github Flow

*   하나의 흐름(main)을 중심으로 곁가지(기능 추가, 테스트, 디버깅 등)가 생겼다가 없어지는 간단한 워크플로우


* 다른 전략들(Git Flow 등)에 비해 흐름이 단순하고 규칙도 적기 때문에 개인 프로젝트나 소규모 팀에 적합하다.
* 복잡한 브랜치 관리 대신, <mark style="color:red;">통합 과정에서 생기는 의존성이나 충돌 같은 핵심 문제에 집중</mark>할 수 있다.





## 규칙

<details>

<summary>Main 브랜치는 직접 수정하지 않는다.</summary>

의도: 직접 수정할 경우 Merge 해야하는 브랜치들과 충돌할 확률이 높아진다.



* 단, main 브랜치에서 파생된 브랜치가 없는 경우 일부 수정이 가능하다.
  * 폴더 구조 / 파일 이름 변경 가능
  * 그 외에 불가능

</details>

<details>

<summary>작업은 항상 새로운 브랜치로 작업한다.</summary>

의도: 행동과 기능을 분리해서 영역이 다름을 시각화하기 위함이다.



* 새로운 브랜치는 주로 Main 브랜치에서 파생된다.
* Main 브랜치에서 파생된 브랜치에서 테스트용으로 다시 파생되는 경우 마지막에'/Sub' 라는 단어를 붙여준다.&#x20;
  * ex) 'feature/network' / 'feature/network/sub'&#x20;
  * sub 브랜치는 Merge하지 말고 삭제한다. 필요한 기능을 feature에 새로 작성
* 작업이 끝난 브랜치는 반드시 PR, Merge하고 삭제한다.

</details>

<details>

<summary>Backup 브랜치로 main 브랜치를 주기적으로 백업한다.</summary>

의도: main 브랜치가 유일하므로 상황을 대비하기 위함

</details>

<details>

<summary>브랜치의 이름은 명료하고 구분되게 짓는다.</summary>



</details>

<details>

<summary>기능을 만들고 테스트한 후, Main 브랜치에 Pull Request를 통해 Merge한다.</summary>



</details>

<details>

<summary>Commit 메세지는 상세하게 작성한다.</summary>



</details>





