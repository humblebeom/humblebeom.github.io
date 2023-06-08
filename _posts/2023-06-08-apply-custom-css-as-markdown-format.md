---
title: "나만의 custom css style을 markdown 형식으로 적용하기"
categories: blog
tag: [jekyll-blog, css, markdown]
typora-root-url: ../
author_profile: false
sidebar:
  nav: "docs"
search: true
---

# minimal-mistakes의 기본 제공 스타일링 리뷰

- 공지사항(notices) 스타일링 리뷰

  ```markdown
  **[공지사항]**[지킬블로그 신규업데이트 안내](https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/)
  {: .notice--danger} # mms에서 제공하는 default 스타일링
  ```

- 파일 검색에서 .notice--danger 로 검색하면 \_notices.scss 파일을 비롯한 관련 파일에 스타일링이 정의되어 있는 것을 확인할 수 있음

  ```css
  # _notices.scss 파일 예시
  
  /* Danger notice */
  
  .notice--danger {
    @include notice($danger-color);
  }
  ```

# Custom style 만들기

- 이미지 삽입시 이미지 크기 50% 축소 및 가운데 정렬 스타일링 만들기

  1. \_sass 폴더 > \_utilities.scss 파일에 image width 축소 클래스 정의

     - css 스타일링 관련 코드는 검색으로 찾아보는 것을 권장

     - 예시: "css image width 50%"로 검색하면 다음과 같은 예시와 코드를 확인 가능

       https://www.w3schools.com/css/tryit.asp?filename=trycss_dim_height_percent

     ```
     .img-width-half {
       width: 50%;
     }
     ```

  2. Image-width-half 사용

     ```markdown
     ![filename]({{site.url}}/images/YYYY-MM-DD-posting-title/filename.png){: .img-width-half}
     ```

- 실제로 적용해보기

  - 원래 사이즈

    ![newjeans-original-size](/images/2023-06-08-apply-custom-css-as-markdown-format/newjeans.jpg)

  - 동일 이미지에 커스텀 스타일 적용

    ![newjeans](/images/2023-06-08-apply-custom-css-as-markdown-format/newjeans.jpg){: .img-width-half}
  
  - 가운데 정렬까지 추가로 적용(가운데 정렬 스타일은 이미 정의되어 있는 클래스를 사용)
  
    ```markdown
    ![filename]({{site.url}}/images/YYYY-MM-DD-posting-title/filename.png){: 
    .img-width-half .align-center}
    ```
  
    - 어느 한 개체에 대해 여러 가지 스타일을 적용할 때는 띄어쓰고 스타일을 계속해서 지정하면 된다. 
  
    ![newjeans](/images/2023-06-08-apply-custom-css-as-markdown-format/newjeans.jpg){: .img-width-half .align-center}
  
  - 개발자 도구에서 적용된 스타일 확인
  
    ![applied-style-check](/images/2023-06-08-apply-custom-css-as-markdown-format/applied-style-check.png){: .align-center}
  
