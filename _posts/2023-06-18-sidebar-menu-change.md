---
title: "사이드바에 카테고리 & 태그 숫자 카운트와 함께 추가하기"
categories: jekyll-blog
tag: [posting count,]
typora-root-url: ../
author_profile: false
sidebar:
  nav: "counts"
search: true
---

# 사이드바 메뉴

## As Is

포스팅 페이지에서 사이드바 설정은 다음과 같았다.

- root._data.navigation.yml

  ```yaml
  ...
  docs:
    - title: "대목차1"
      children:
        - title: "Category"
          url: /categories/
        - title: "Tag"
          url: /tags/
  
    - title: "대목차2"
      children:
        - title: "Category"
          url: /categories/
        - title: "Tag"
          url: /tags/
  ...
  ```

- YAML front matter

  ```yaml
  # navigation.yml에 정의된 사이드바 설정 중 "docs" 적용을 명시
  sidebar:
    nav: "docs"
  ```

- result

  ![sidebar-as-is](/images/2023-06-19-/sidebar-as-is.png){: .image-width-half }

## To Be

sidebar nav를 counts로 변경하기

- nav__list 파일수정
  - 이 부분은 그냥 제공된 파일을 사용하는 것으로 대체
  - 직접 수정은 문서 구조 파악이 필요하며 시간이 제법 걸릴 것 같아 패스

- root._data.navigation.yml

  ```yaml
  ...
  counts: 
  	- title: "카테고리" # 원하는 분류 명칭으로 변경 가능
  		use: true
  	- title: "태그"  # 원하는 분류 명칭으로 변경 가능
  		use: true
  ...
  ```

- posting의 YAML front matter

  ```yaml
  # 사이드바 설정 중 위에서 정의한 "counts" 적용하는 것으로 변경
  sidebar:
    nav: "counts"
  ```

- result

  ![sidebar-to-be](/images/2023-06-19-/sidebar-to-be.png){: .image-width-half }

- caution
  - 단, 이렇게 sidebar 설정을 적용하는 경우 기존의 문서에서 "docs" 양식을 적용한 문서에서는 sidebar 가 사라지는 문제가 나타났다.