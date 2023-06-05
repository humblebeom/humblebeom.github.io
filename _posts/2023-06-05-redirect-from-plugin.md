---
title: "사이트 주소가 바뀌었을 때 JekyllRedirectFrom 플러그인으로 해결하기"
categories: blog
tag: [blog, redirect, jekyll plugin]
typora-root-url: ../
author_profile: false
sidebar:
  nav: "docs"
search: true
redirect_from:
  - /redirect-test/post1
  - /redirect-this-too
---

# JekyllRedirectFrom

- https://github.com/jekyll/jekyll-redirect-from
- 웹사이트에 여러가지 URL로 접속할 수 있는 방법을 제공하는 jekyll-plugin
- 지금 작성하고 있는 포스팅의 파일명이나 카테고리 정보를 변경하면 기존 url로는 404 Error가 발생하면서 접속이 불가하게 된다.

## Installation

- shell에서 플러그인 설치

  ```bash
  gem install jekyll-redirect-from
  ```

- \_config.yml 파일에 플러그인 정보 추가: plugins 섹션과 whitelist 섹션에 동일하게 추가

  ```yaml
  # Plugins (previously gems:)
  plugins:
    - jekyll-paginate
    - jekyll-sitemap
    - jekyll-gist
    - jekyll-feed
    - jekyll-include-cache
    - jekyll-redirect-from # 추가

  # mimic GitHub Pages with --safe
  whitelist:
    - jekyll-paginate
    - jekyll-sitemap
    - jekyll-gist
    - jekyll-feed
    - jekyll-include-cache
    - jekyll-redirect-from # 추가
  ```

- minimal-mistakes-jekyll.gemspec 파일에 runtime dependency 설정 추가

  ```python
  spec.add_runtime_dependency "jekyll-redirect-from", "~> 0.1"
  ```

## 게시물 redirect

- 블로그 게시물의 URL은 다음과 같이 규칙으로 정해진다.

  ```shell
  {site.url}/{category}/{filename}
  ```

- 이 게시물의 url은 다음과 같다.

  ```shell
  {site.url}/blog/redirect-from-plug-in
  ```

- url이 변경되는 경우 redirect를 위해 formatter에 기존 url 정보를 다음과 같이 명시해준다. 복수개의 url도 등록 가능하다.

  ```shell
  ...
  redirect_from:
    - /blog/redirect-from-plug-in
    - /redirect-this-too
  ...

  ```
