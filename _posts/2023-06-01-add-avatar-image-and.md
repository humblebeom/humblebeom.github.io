---
Layout: single
title: "메인 페이지 사진 추가, 유튜브 아이콘/링크 추가하기"
Categories: blog
Tag:
  [blog, Jekyll, avatar, bio]
toc: True
typora-root-url: ../
author_profile: false
sidebar:
  nav: "docs"
search: true

---

# 1. 메인 페이지 사진 추가

- _config.yml 파일

  ```yaml
  # Site Author
  author:
    name: "HumbleBeom"
    avatar: "/images/teddynote.png"   # 아바타 이미지 링크 추가
    bio: "험블범의 개발블로그 입니다"
  ```

- 아바타 이미지 추가 전

  <img src="/images/2023-06-01-add-avatar-image-and/before_avatar_applied.png" alt="before_avatar_applied" style="zoom:50%;" />

- 아바타 이미지 추가 후

  <img src="/images/2023-06-01-add-avatar-image-and/after_avatar_applied.png" alt="after_avatar_applied" style="zoom:50%;" />

# 2. Youtube 아이콘 / 링크 추가하기

## Side bar에 추가하기

- Font awesome youtube icon 검색

  YouTube icon* in the Solid style 링크 페이지 확인

  ![youtube-icon](/images/2023-06-01-add-avatar-image-and/youtube-icon.png)

- _config.yml 파일 수정

  ```yaml
  # Site Author
  author:
  	...
  	links:
  		...
      - label: "YouTube"
  			icon: "fab fa-fw fa-youtube"
        url: "https://www.youtube.com/@NewJeans_official"
  ```

  

## Footer에 추가하기

- 동일한 방법으로 Site Footer 영역에 유튜브 아이콘 및 링크 추가

