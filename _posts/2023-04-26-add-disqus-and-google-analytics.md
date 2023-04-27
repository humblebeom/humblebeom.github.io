---
layout: single
title:  "댓글기능(Disqus), Google Ananlytics 추가"
typora-root-url: ../
---

# 1. 댓글기능 추가하기

- 개략적인 가이드는 링크 참조 https://mmistakes.github.io/minimal-mistakes/docs/configuration/#comments
- utterance(https://utteranc.es/) 깔끔하고 좋아보임. 추후 적용 검토!

## 1.1. DISQUS 회원가입

- 구글 계정으로 가입 및 로그인

## 1.2.  DISQUS 세팅

- settings > Getting Started >  Add Disqus to Site

<img src="/images/2023-04-26-add-disqus-and-google-analytics/create_a_new_site.png" alt="create_a_new_site" style="zoom: 50%;" />

- 과금모델 선택화면에서 하단에 무료사용 선택 가능

## 1.3. _configure.yml 수정

- Defaults > values > comments:  true

- comments 항목의 세부 내용 편집

  ```yaml
  comments
  	provider: "disqus"
  	disqus:
  	  shortname: {$shortname} # disqus와 연동한 내 웹사이트의 shortname은 disqus의 admin 메뉴에서 확인 가능
  ```

## 1.4. 댓글기능 반영 확인

- localhost 에선 반영되지 않음
- git commit & push 실행
- 브라우저에서 내 깃헙블로그에 접속. 아직 반영이 안된 경우 새로고침하면 Disqus 연동 inform이 나타나며 댓글 기능 사용이 가능해짐

## 1.5 댓글 관리

- disqus의 admin 페이지에서 관리
- 무료버전인 경우에도 간단한 Analytics 기능 제공

# 2. Google Analytics 추가하기

- 개략적인 가이드는 링크 참조(https://mmistakes.github.io/minimal-mistakes/docs/configuration/#analytics)

