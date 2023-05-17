---
Layout: single
title: "구글, 네이버 검색엔진에 등록하기"
Categories: blog
Tag: [blog, Jekyll, search engine, 검색엔진, google, naver]
toc: True
typora-root-url: ../
author_profile: false
sidebar:
  nav: "docs"
search: false
---

# 1. Google 검색엔진에 블로그 등록하기

## 1-1. Google Search Console 웹페이지 접속

- 검색하거나 mmistakes의 링크를 따라 가면 된다.
  - https://mmistakes.github.io/minimal-mistakes/docs/configuration/#google-search-console

## 1-2. 콘솔 페이지에서 블로그 URL Prefix 등록

<img src="/images/2023-05-17-register-my-blog-on-search-engines/google-search-console.png" alt="google-search-console" style="zoom: 50%;" />

## 1-3. 블로그 Ownership 인증

- html 파일 다운로드 및 저장

  <img src="/images/2023-05-17-register-my-blog-on-search-engines/verify-ownership.png" alt="verify-ownership" style="zoom:67%;" />

  - 블로그 프로젝트 폴더에서 index.html, LICENSE 파일과 같은 위치에 다운받은 html 파일 저장
  - github push 후 google search console 화면으로 돌아가 인증(Verify) 버튼 클릭

## 1-4. sitemap 제출

![submit-sitemap](/images/2023-05-17-register-my-blog-on-search-engines/submit-sitemap.png)

- 정상적으로 제출이 되었다면 블로그 사이트맵 URL로 접속했을 때 다음과 같은 화면을 볼 수 있다<img src="/images/2023-05-17-register-my-blog-on-search-engines/sitemap.png" alt="sitemap" style="zoom: 50%;" />

# 2. Naver 검색엔진에 블로그 등록하기

## 2-1. 네이버 Webmaster Tools 접속

## 2-2. URL 등록 및 소유권 인증

- HTML 메타태그를 사용한 인증방식 사용

## 2-3. 요청 > Sitemap 제출

## 2-4. 검증 > robot.txt > 수집요청

## 2-5. 웹페이지 최적화
