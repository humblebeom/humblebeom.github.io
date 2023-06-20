---
title: "블로그 상단에 배너 추가하기"
categories: jekyll-blog
tag: [banner,]
typora-root-url: ../
author_profile: false
sidebar:
  nav: "counts"
search: true
---

### 1. root._include.top-banner.html 파일 생성 및 편집

```xml
<p class="notice--info" style="font-size: 1rem !important;">
  <string>누나는 진짜 욕심쟁이네?</strong>
  <br>
  <a href="https://www.youtube.com/watch?v=RvUGsplnWOk">영상 보러가기</a>
</p>
```

### 2. root._layouts.single.html 파일 편집

- top-banner 위치 지정:  page__inner-wrap 클래스 안의 최상단에 아래 코드 삽입

  &#123;% include top-banner.html %&#125;

### 3. 참고

- 생성한 배너는 블로그의 포스트에서 동일한 스타일로 노출됨
- _config.yml에서 블로그 포스트의 기본 레이아웃을 single로 설정했고 single에 top banner 추가 작업을 했기 때문



