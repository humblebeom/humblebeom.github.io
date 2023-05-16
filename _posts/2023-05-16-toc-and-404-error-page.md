---
Layout: single
title: "글 목차 및 404 에러 페이지 구현하기"
Categories: blog
Tag: [blog, Jekyll, toc]
toc: True
---

# 1. 글 목차(toc) 구현

- 글 목차(=Table of Contents), 줄여서 toc 라고 표현하는 경우가 많음
- md 파일의 YAML front matter에서 toc: true 설정

# 2. 404 에러 페이지 구현

- \_pages 폴더에 404.md 파일 생성

- minimal misstakes에서 제공하는 \_test.\_pages.404.md 파일 내용을 방금 생성한 404.md 파일에 붙여넣는다.

- 필요시 404.md 파일에 내용 추가

- 404 에러 표시 페이지에 이미지 추가하는 경우

  - 사용할 이미지의 url을 복사한 후

  ```markdown
  ![](https://{image-url})
  ```
