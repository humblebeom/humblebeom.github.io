---
title: "mathjax 적용하기"
categories: jekyll-blog
tag: [LaTex, mathjax]
typora-root-url: ../
author_profile: false
sidebar:
  nav: "docs"
search: true
use_math: true
---

# mathjax

- LaTex 수식을 컴파일해서 원하는 수식이나 행렬 등의 형태로 변환

- Jekyll Blog에서는 LaTex 수식을 지원하지 않음

  ```markdown
  # 다음의 LaTex 수식이 변환되지 않고 그대로 표현됨

  $\[ x^2 + y^2 = z^2 \]$
  $y = f(x)^2$
  ```

- LaTex 수식을 지원하기 위한 조치

  - mathjax-support.html 다운로드

  - 프로젝트 경로에 파일 위치 시키기

    - root > \_includes > mathjax-support.html

  - mathjax 사용을 정의

    - Project root > \_includes > head > custom.html 파일

      ![apply-mathjax](/images/2023-06-18-apply-mathjax/apply-mathjax.png)

  - YML Front Matter에서 수식 사용 여부를 정의

    ```yaml
    # 블로그 포스트 중 LaTex를 사용하는 페이지에만 LaTex 사용을 명시하여 리소스를 절약할 수 있음
    use_math: true
    ```

- mathjax 기능으로 LaTex 수식이 적용된 결과

  $\[ x^2 + y^2 = z^2 \]$

  $y = f(x)^2$
