---
title: "포스트 왼쪽 영역 확장, TOC 스타일 수정하기"
Categories: blog, css
Tag: [blog, Jekyll, css]
typora-root-url: ../
author_profile: false
sidebar:
  nav: "docs"
search: true
---

# 1. 포스트 왼쪽 영역 확장하기

- 크롬 개발자 도구를 활용한 CSS 스타일링 수정 방법의 한 가지 사례

- 크롬 개발자 도구를 활용해서 포스팅 본문의 태그 영역 확인: page\_\_inner-wrap

  ![page__inner-wrap](/images/2023-06-03-extent-sidebar-sectionand-toc-styling/page__inner-wrap.png)

- vcs에서 파일 찾기(shift +cmd + F)로 해당 태그를 검색해보면 태그가 사용된 파일 검색 결과를 얻을 수 있다.

  ```css
  .page {
    @include breakpoint($large) {
      float: right;
      width: calc(100% - #{$right-sidebar-width-narrow});
      padding-right: $right-sidebar-width-narrow;
    }

    @include breakpoint($x-large) {
      width: calc(100% - #{$right-sidebar-width});
      padding-right: $right-sidebar-width;
    }

    .page__inner-wrap {
      float: left;
      margin-top: 1em;
      margin-left: 0;
      margin-right: 0;
      width: 100%;
      clear: both;
  ```

  실제론 page 태그의 css styling에서 $right-sidebar-width-narrow 변수를 사용하여 너비를 정의하고 있음을 알 수 있다.

  $right-sidebar-width-narrow 변수를 지우거나 변수 정의를 수정해서 포스팅 너비를 원하는 수준으로 맞추면 된다.

  $right-sidebar-width-narrow 변수는 \_variables.scss 파일에 200px로 정의되어 있었다.

- 사이드바를 제거할 경우 포스팅의 YAML front matter 영역에서 사이드바 사용에 대한 정의도 삭제한다.

  ```yaml
  sidebar:
    nav: "docs"
  ```

# 2. Table of contents 스타일 수정하기

- 먼저 front matter에서 toc 설정을 몇 가지 추가

  ```yaml
  toc_sticky: true # 페이지를 스크롤해도 toc 위치가 고정되도록 하는 설정
  toc_label: 목차 # toc 명칭을 "목차"로 수정
  toc_icon: "fa-regular fa-utensils" # fontawesome에서 원하는 icon을 찾아 적용
  ```

- 위 변경 사항을 문서 작성할 때마다 매번 복사붙여넣기 하기는 번거로우므로 default setting에 추가한다.

- \_config.yml 파일 수정

  ```yaml
  # Defaults
  defaults:
    # _posts
    - scope:
        path: ""
        type: posts
      values:
        layout: single
        author_profile: true
        read_time: true
        comments: true
        share: true
        related: true
        show_date: true

  date_format: "%Y-%m-%d"
  ```
