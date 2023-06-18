---
title: "연도별 포스팅 아카이브 생성하기"
categories: jekyll-blog
tag: [연도별 포스팅]
typora-root-url: ../
author_profile: false
sidebar:
  nav: "counts"
search: true
---

# 연도별 아카이브 생성하기

- 파일 복사

  - test.\_pages.year-archive.md > \_pages.year-archive.md

    ```markdown
    ## <!-- year-archive.md -->

    title: "Posts by Year"
    permalink: /year-archive/
    layout: posts
    author_profile: true

    ---
    ```

- 위 파일을 적절한 경로에 추가하는 것만으로 연도별 포스팅 분류가 가능하다.

  - blog-url/year-archive 에 접속해서 확인할 수 있다.

- 블로그 상단 nav에 연도별 아카이브 메뉴 생성하기

  - \_data.navigation.html 편집으로 우측 상단 네비게이션에 매우 쉽게 메뉴를 추가할 수 있다.

    ![posts-by-year-menu](/images/2023-06-18-make-posting-archives-by-year/posts-by-year-menu.png){: .image-width-half}

# 연도별 아카이브 그리드

- 연도별 포스팅을 그리드 형태로 표현하여 한눈에 비교가 쉽도록 표현하는 방식이며 지킬 블로그에 적용하는 방법은 연도별 아키이브를 생성하는 방법과 거의 동일하다. year-archive-grid.md 를 사용하는 것만 다르다.
