---
Layout: single
title: "공지사항, 버튼, Youtube 영상 추가하기"
Categories: blog
Tag:
  [blog, Jekyll, notice, 공지사항, button, 버튼, youtube, 유튜브, vedio, 영상]
toc: True
typora-root-url: ../
author_profile: false
sidebar:
  nav: "docs"
search: true
---

# 1. 공지사항 추가하기

## 1-1. 볼드체 강조 및 링크 추가

```markdown
**[공지사항]**[지킬블로그 신규업데이트 안내](https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/)
```

**[공지사항]**[지킬블로그 신규업데이트 안내](https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/)

## 1-2. Notice 강조 기능 사용하기

```mark
**[공지사항]**[지킬블로그 신규업데이트 안내](https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/)
{: .notice--danger}
```

**[공지사항]**[지킬블로그 신규업데이트 안내](https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/)
{: .notice--danger}

## 1-3. 강조할 Notice 단락을 태그로 감싸기

<div class="notice--success">
  <h2>공지사항입니다.</h2>
  <ul>
    <li>항목 1</li>
    <li>항목 2</li>
    <li>항목 3</li>
  </ul>
</div>

# 2. 버튼 추가하기

- 버튼은 일반적으로 클릭을 통한 링크 유도를 하기 위해 사용
- [구글링크](https://google.com){: .btn .btn--primary}

# 3. Youtube 영상 추가하기

- 추가하고 싶은 영상의 youtube id를 확인하여 입력한다.

  ![youtube link](/images/2023-05-22-adding-notice-button-and-youtube-video/youtube link.png)

- 결과
  
  {% include video id="qRUxCTEtKMI" provider="youtube" %}
  
