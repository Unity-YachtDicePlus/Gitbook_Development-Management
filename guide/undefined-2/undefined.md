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

# Git Commit Message 규칙

#### 규칙 작성 의도

* 프로젝트가 진행될수록 브랜치의 수와 커밋 횟수가 많아져 복잡해지는 상황을 감소시키기 위함
* 이전 프로젝트에서의 미숙함으로 규칙이 제대로 이행되지 않았기 때문에 숙련도를 높이고 피드백하기 위함.
* 충돌 발생 경우를 줄이기 위함.
* 협업 방식을 체계적으로 구조화하는 연습을 하기 위함.



## Rules

* 메세지 작성에는 [**Conventional Commits**](https://www.conventionalcommits.org/ko/v1.0.0/#%ea%b7%9c%ea%b2%a9)을 따른다.
* 제목과 본문을 빈 행으로 구분한다.
* 제목은 50글자 이내로 제한한다.
* 제목의 첫 글자는 대문자로 작성한다.
* 제목 끝에는 마침표를 넣지 않는다.
* 제목은 명령문으로 사용하며 과거형을 사용하지 않는다.
* 본문의 각 행은 72글자 내로 제한한다. 72자가 넘어가면 문단을 나누는 것이 좋다.
* 어떻게 보다는 무엇과 왜를 설명한다.



## Frame

```
# commit message template
# 제목은 'type: 제목' 형태로 작성합니다.
# 본문과 푸터는 선택 사항 입니다.
#######제목#######

#######본문(작성시간 포함)#######

#######푸터#######

##################
# Feat: 기능의 수정, 변경, 추가
# Fix : 버그 수정
# Docs : 문서 수정
# Style : 기능에 영향이 없는 코드 스타일 변경
# Design : UI 변경
# Test : 테스트의 추가, 수정
# Refactor : 코드의 리팩토링
# Chore : 그 외 자질구레한 일들
# Add : 파일 추가
# Remove : 파일 삭제
# Rename : 파일 이름 변경
##################
```



