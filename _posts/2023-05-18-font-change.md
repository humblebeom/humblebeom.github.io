---
Layout: single
title: "블로그 폰트 바꾸기"
Categories: blog
Tag: [blog, Jekyll, font, 폰트]
toc: True
typora-root-url: ../
author_profile: false
sidebar:
  nav: "docs"
search: true
---

# 1. 내 블로그 폰트 확인

- 크롬 브라우저의 개발자 모드에서 내 블로그에 적용된 폰트를 확인
- Whatfont라는 크롬 extension을 이용해서 폰트를 간편하게 확인할 수도 있다.

# 2. 구글 폰트에서 사용하고 싶은 폰트 선택

- https://fonts.google.com/

  - Languages에서 한국어를 선택하면 한국어를 지원하는 폰트 확인 가능

  - 나는 JIKJISOFT의 Sunflower 폰트 선택

    ![google-font-sunflower](/images/2023-05-18-font-change/google-font-sunflower.png)

  - 우측 사이드바에서 Use on the web 항목에서 @import 선택 후 나타나는 구문을 복사(@import에서 세미콜론까지)

# 3. 구글 폰트 적용

- 프로젝트의 _sass/minimal-mistakes.scss 파일에 구글 폰트 웹사이트에서 복사해온 import 구문 추가

  ```python
  @import url('https://fonts.googleapis.com/css2?family=Sunflower:wght@300;500;700&display=swap');
  ```

- _sass/minimal-mistakes/_variables.scss 파일의 32th 라인의 $global-font-family: $sans-serif 라인에서 $san-serif를 선택 및 우클릭하여 정의로 이동. 여기서 global-font-family는 $sans-serif 를 참조하며 $sans-serif의 정의에서 적용된 폰트들을 확인할 수 있음. 

  ![add-font-definition](/images/2023-05-18-font-change/add-font-definition.png)
