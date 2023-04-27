---
layout: single
title: "Configure Local Server"
typora-root-url: ../
categories: blog
tag: [jekyll, blog]
---

#  로컬 서버 구성하기 for GitHub blog

## Ruby 설치

- jekyll 공식 홈페이지 가이드에 따라 ruby를 설치한다. (https://jekyllrb.com/docs/installation/macos/)

```bash
brew install chruby ruby-install xz
ruby-install ruby 3.1.3
```

- configure your shell to automatically use chruby
  (아래 shell 명령 실행후 터미널을 닫고 재실행한다.)

```
echo "source $(brew --prefix)/opt/chruby/share/chruby/chruby.sh" >> ~/.zshrc
echo "source $(brew --prefix)/opt/chruby/share/chruby/auto.sh" >> ~/.zshrc
echo "chruby ruby-3.1.3" >> ~/.zshrc # run 'chruby' to see actual version
```

## Jekyll, bundler 설치

```
gem install jekyll
gem install bundler
```

## bundle 설치

- 터미널에서 프로젝트 경로로 이동하여 bundle 설치 명령을 실행한다.

```bash
{project-directory}> bundle install
```

## 로컬 서버 실행

```
bundle exec jekyll serve
```

- 여기까지 실행하면 로컬서버(http://localhost:4000/ )에서 실시간으로 블로그를 확인할 수 있다.

# 참고

### Front matter

- 블로그 포스트 작성시 md 파일의 시작부분에 작성하는 메타정보
- Paragraph의 하나로 분류되며 YAML 형식을 따른다.
- 보통 다음과 같이 내용들이 포함된다.
  - layout: single
  - title: "title"
  - typora-root-url: ../
