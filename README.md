# Blog

### 0 .마크다운 사용법
https://gist.github.com/ihoneymon/652be052a0727ad59601

### 1. 목적

* 공부한 내용을 스스로 정리할겸 아카이브로 사용하면서 나중에 쉽게 찾으려고 만듦.

### 2. 템플릿: 

* jekyll을 이용한 millennial (https://github.com/LeNPaul/Millennial/blob/gh-pages/README.md)

### 3. 특징

* Compatible with GitHub Pages.

* Support for Jekyll's built-in Sass/SCSS preprocessor and data files for making customizing easier.

* [Google Analytics](https://www.google.com/analytics/) support.

* Commenting support powered by [Disqus](https://disqus.com/).

* Optimized for search engines.

* LaTeX support through [MathJax](https://www.mathjax.org/).

### 4. layout
```
---
layout:
title:
author:
categories:
tags: []
image:
---
```

### 5. 디폴트 디렉토리 구조

```bash
Millennial/
├── _data                      # Data files
|  └── settings.yml            # Theme settings and custom text
├── _includes                  # Theme includes
├── _layouts                   # Theme layouts (see below for details)
├── _posts                     # Where all your posts will go
├── assets                     # Style sheets and images are found here
|  ├── css                     # Style sheets go here
|  |  └── _sass                # Folder containing SCSS files
|  |  └── main.scss            # Main SCSS file
|  |  └── syntax.css           # Style sheet for code syntax highlighting
|  └── img                     # Images go here
├── pages                      # Category pages
├── _config.yml                # Site build settings
├── Gemfile                    # Ruby Gemfile for managing Jekyll plugins
├── index.md                   # Home page
├── LICENSE.md                 # License for this theme
├── README.md                  # Includes all of the documentation for this theme
└── rss-feed.xml               # Generates RSS 2.0 file which Jekyll points to
```

```
* 링크(파일)명 수정 시 : 
[/pages], [/category] 경로의 [html 문서] 수정 
-> 상위메뉴 수정할 경우 [/_pages/-.html]의 [{% %}속 템플릿 변수] 수정
-> 하위메뉴 수정할 경우 [/category/-.html]의 [{% %}속 템플릿 변수] 수정 
-> [/_posts] 경로의 [폴더명] 수정 
-> [/_data/settings.yml]의 [file] 수정 
-> 상위메뉴 수정할 경우 [/_includes/header.html]의 <li class="menu-item dropdown"><a - href> 의 [href 속성] 수정
-> [/_posts/-.md]의 [categories] 수정

* 메뉴명 수정시 : 
[/_data/settings.yml]의 [name] 수정 
-> [/_includes/header.html]의 [태그 속 콘텐츠] 수정 
-> [/_posts/-.html]의 [title] 수정
-> 상위메뉴 수정할 경우 [/pages/-.html]의 title 수정
-> 하위메뉴 수정할 경우 [/category/-.html]의 title 수정
```

### 6. Table of Contents

1. [Introduction](#introduction)
   1. [What is Jekyll](#what-is-jekyll)
   2. [Never Used Jeykll Before?](#never-used-jekyll-before)
2. [Installation](#installation)
   1. [GitHub Pages Installation](#github-pages-installation)
   2. [Local Installation](#local-installation)
   3. [Directory Structure](#directory-structure)
   4. [Starting From Scratch](#starting-from-scratch)
3. [Configuration](#configuration)
   1. [Sample Posts](#sample-posts)
   2. [Site Variables](#site-variables)
   3. [Adding Menu Pages](#adding-menu-pages)
   4. [Posts](#posts)
   5. [Layouts](#layouts)
   6. [YAML Front Block Matter](#yaml-front-block-matter)
4. [Features](#features)
   1. [Design Considerations](#design-considerations)
   2. [Disqus](#disqus)
   3. [Google Analytics](#google-analytics)
   4. [RSS Feeds](#rss-feeds)
   5. [Social Media Icons](#social-media-icons)
   6. [MathJax](#mathjax)
   7. [Syntax Highlighting](#syntax-highlighting)
   8. [Markdown](#markdown)
5. [Everything Else](#everything-else)
6. [Contributing](#Contributing)
7. [Questions?](#questions)
8. [Credits](#credits)
9. [License](#license)

### 7. License

Open sourced under the [MIT license](https://github.com/LeNPaul/Millennial/blob/gh-pages/LICENSE.md).

### 8. 블로그 작성 참고 사항

태그는 모두 소문자

