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

#### Rules

* 메세지 작성에는 [**Conventional Commits**](https://www.conventionalcommits.org/ko/v1.0.0/#%ea%b7%9c%ea%b2%a9)을 따른다.
* 제목과 본문을 빈 행으로 구분한다.
* 제목은 50글자 이내로 제한한다.
* 제목의 첫 글자는 대문자로 작성한다.
* 제목 끝에는 마침표를 넣지 않는다.
* 제목은 명령문으로 사용하며 과거형을 사용하지 않는다.
* 본문의 각 행은 72글자 내로 제한한다. 72자가 넘어가면 문단을 나누는 것이 좋다.
* 어떻게 보다는 무엇과 왜를 설명한다.



#### Frame

```
type: Subject
body
footer(issue tracker id를 작성할 때 사용한다.) 
```



#### Type

* feat: 새로운 기능과 관련된 것을 의미한다.
* fix: 오류와 같은 것을 수정했을 때 사용한다.
* docs: 문서와 관련하여 수정한 부분이 있을 때 사용한다.
* style: 코드의 변화와 관련없는 포맷이나 세미콜론을 놓친 것과 같은 부분들을 의미한다.
* refactor: 코드의 리팩토링을 의미한다.
* test: test를 추가하거나 수정했을 때를 의미한다.
* chore: build와 관련된 부분, 패키지 매니저 설정 등 여러가지 production code와 무관한 부분 들을 의미한다. 말 그대로 자질구레한 일들이다.



| Summary(required) | 분류: 핵심 내용 요약                                                                       |
| ----------------- | ---------------------------------------------------------------------------------- |
| Description       | <ul><li>작성시간</li><li>요약</li><li>상세 수정사항(분류: 코드/설정/버그/문서/주석/리소스 등의 내용) 작성</li></ul> |

| \[Fix] 적 AI 패턴 관련 버그                                                                                                                                                                                                                                                                                                                                                      |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>(2026-01-13 10:20)<br>문제: 스매쉬 애니메이션 중에는 hitbox가 활성화되어야 하는데 ~한 이유로 hitbox를 얻지 못해 null reference 발생<br>해결: 대시 상태 체크를 함정 충돌 체크보다 먼저 실행하도록 순서 변경</p><p></p><p>[Balance] 'BossAHealth' 5000 → 3000으로 조정<br>[Balance] 'BossBHealth' 4000 → 3200으로 조정<br>[Audio] 폭발 사운드 볼륨 조정<br>[UI] 보스 체력 UI 추가<br>[Refactor] BossA 클래스의 Smash() 코드 수정<br>[Test] 전투 시스템 유닛 테스트 추가</p> |



</details>





