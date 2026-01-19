---
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

# 용어 정리

<details>

<summary>cd(change directory)</summary>

* 해당경로로 디렉토리 변경
* cd G:\dev\Github\Unity\YachtDicePlus\
  `G:\dev\Github\Unity\YachtDicePlus` 경로로 디렉토리 변경

</details>

<details>

<summary>git branch</summary>

브랜치 목록 나열

</details>

<details>

<summary>git checkout -b 새브랜치명</summary>

* 새로운 브랜치를 생성하고 이동
* 또는 `git switch -c 새브랜치명`
* 새 브랜치 생성만: `git branch 새브랜치명`

</details>

<details>

<summary>git pull</summary>

원격 저장소의 데이터를 로컬 저장소에 최신화

</details>

<details>

<summary>git add . </summary>

* 모든 작업 사항을 스테이지에 추가
* 파일명으로 추가 가능: git add README.md

</details>

<details>

<summary>git status</summary>

* 로컬 작업 공간의 상태 확인

</details>

<details>

<summary>git commit</summary>



</details>

<details>

<summary>git reset</summary>

스테이징 파일 전체 취소

</details>

<details>

<summary>git restore . &#x26;&#x26; git clean -fdx</summary>

1. git status -s (현재 상태)
2. git reset (스테이징 취소)
3. git restore . (수정된 파일을 **마지막 커밋 상태로 덮어쓰기** (실제 삭제 효과))
4. git clean -n (미리보기)
5. git clean -fdx (untracked 완전 삭제)
6. git status (최종 확인)

</details>

