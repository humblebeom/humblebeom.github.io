---
title: "이미지 에러 해결하기"
Categories: blog
Tag: [blog, Jekyll, image, path, error]
typora-root-url: ../
author_profile: false
sidebar:
  nav: "docs"
search: true
---

# 이미지 상대경로 > 절대경로로 변경하기

- 상대경로를 이용한 image path

  ```ruby
  ![filename](../images/YYYY-MM-DD-posting-title/filename.png)
  ```

  YAML formatter에서 typora-root-url: ../을 적용하면 상대경로 맨 앞에 있는 "../" 생략 가능

- 절대경로 이용하기

  ```ruby
  ![filename]({{site.url}}/images/YYYY-MM-DD-posting-title/filename.png)
  ```

  ruby 문법에서 이중 중괄호는 변수에  할당된 값을 반환한다.

  ```ruby
  # 다음 예시들은 _config.yml에 설정된 값들을 가져오게 된다.  
  
  {{ site.url }}
  {{ site.title }}
  {{ site.description}}
  
  ```

  <img src="/images/2023-06-04-image-path-error-handling/image-20230604202321320.png" alt="image-20230604202321320" style="zoom:50%;" />
