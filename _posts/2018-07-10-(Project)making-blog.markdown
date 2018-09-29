---

title: "01 : Jekyll & Git으로 블로그 만들기"
layout: post
date: 2018-07-10 22:44
comment : true
tag: jekyll
image: https://koppl.in/indigo/assets/images/jekyll-logo-light-solid.png
headerImage: true
projects: true
hidden: true # don't count this post in blog pagination
description: "왜 나는 Jekyll & Git 블로그를 선택하고, 제작하였나?"
category: project
author: Columbus
externalLink: false

---

### Summary
---

* [Situation](#Why)
* [왜 Jekyll & Git 블로그를 선택하였나?](#Install)
* [관련 자료](#List_01)
* [레퍼런스](#List_02)

<br />
<br />


![blog_image]({{ site.url }}/assets/images/blog_image.png)

<div id="Why">

<h4> Situation : 왜 블로그를 제작하게 되었나? </h4>
</div>

---

필자는 현재 **ARCHISKETCH의 서비스** 및 **각 서비스 컨텐츠 별 UI/UX** 에 관한 전반적인 기획 및 디자인을 담당하고 있습니다.

>_미대와 컴공... 둘다 상관없는 학과를 졸업하고, 화면을 구성하는 대부분의 눈에 보이는 프론트 영역 전부를? (~~이건 뭐 현장에서 코드만 안칠뿐이지...~~) 책임지고 있습니다... 인생의 아이러니... ~~스타트업이라 사람도 없어 해당 영역을 책임질 사람도 나말곤 없다는게 함정...~~_

<div style="color:#999; font-size: 14px;">

주의 : 위의 글은 정말 무의미한 한탄의 글입니다. 아래의 글 부터 읽어주시면 감사하겠습니다.
</div>
<br />
하여튼, 이번에 회사가 **시리즈 A** 투자를 받으며 몇가지 이슈가 발생되었는데, 이슈들은 아래와 같았습니다.

- 트렐로 혹은 아사나 같은 **사내 운영 개발 노트** 말고 타인이 볼 수 있는 **새로운 개발 노트** 가 필요하다.
- 곧 추가될 **ARCHISKETCH API DOC** 를 넣을 장소가 없다.
- ~~세미나든, 학원이든, 뭐든 내가 틈틈히 열심히 공부했는데, 이 코드 자료들을 정리할 장소가 없다 응?~~

저는 위의 이슈에 대한 해결 방법으로 **개발 블로그 제작 및 운영** 을 제시했고, 보시는 바와 같이 제가 제작하게 되었습니다.

```javascript

항상 배우다는 자세로 임하고, 새로운 것을 좋아하니 상관 없어요! 토탁토탁 사절!

```

<br />

<div id="Install">

<h4> 왜 Jekyll & Git 블로그를 선택하였나? </h4>
</div>

---

개발 블로그 제작을 위해 여러가지 블로그 서비스 사이트를 알아보았습니다.<br /> 티스토리[^1], 네이버 블로그[^2], 구글 블로그[^3], 브런치[^4], 텀블러(Tumblr)[^5], 미디엄[^6]...등을 알아보았고, 해당 서비스들의 몇가지 공통적인 단점을 발견하였습니다.

[^1]:https://www.tistory.com
[^2]:https://section.blog.naver.com
[^3]:https://www.blog.google
[^4]:https://brunch.co.kr
[^5]:https://www.tumblr.com
[^6]:https://medium.com
- **단점**
  - 부분 유로 혹은 유료 서비스 다수
  - Markdown 미 지원
  - 커스텀 디자인 및 기능 추가의 용이성 제한

위의 단점 및 기타 여러가지 이유로 우리는 **ARCHISKETCH DEVELOPMENT BLOG** 를 **Jekyll을 활용한 깃허브 블로그** 를 제작하기로 결정했습니다.

Jekyll을 활용한 블로그는 Markdown문서로 작성하고, 이를 정적 페이지로 자동 변환시켜주는 손쉬운? Github 블로그 입니다.

>_**Ruby를 베이스로 한 Jekyll**은 Github 저장소를 클라이언트 화면단에 블로그 포멧으로 변환하여 보여주는 플러그인입니다. 눈에 보이는 것에 신경을 들이지 않으실 것이라면, Gist나 그냥 Github repository를 통해 블로그를 관리하는 것도 괜찮은 방법인 것 같습니다._
>

Jekyll과 Github Page의 조합은 많은이들에게 사용된지 상당히 오래되었으므로, 본 포스팅에서는 **Jekyll 설치방법** 및 **구현** 에 대한 과정은 생략하려 합니다.

>_만약 **설치** 및 **구현자료** 를 보기위해 진입하셧다면, 아래의 **관련자료 및 레퍼런스**를 참고해주신다면 감사하겠습니다._

Jekyll은 전세계 개발자들이 미리 만들어 놓은 좋은 테마를 무료(또는 유료?)로 사용이 가능합니다.<br />themes.jekyllrc.org 혹은 jekyllthemes.org 등을 통하여 본인의 취향에 맞는 테마를 선택 할 수도 있습니다. Archisketch blog는 **type-theme** 라는 단순하고 깔끔한 테마를 선택하여 구축했습니다. fork를 떠서 본인의 repository에 옮긴뒤 약간의 커스터마이징 이후에, config.yml 상단에 Ex] remote_theme : rohanchandra/type-theme 같은 사용 테마 문구를 가미해주는 센스 역시 해주도록 합시다.

<br />


#### 완성
---
그리고 완성된 파일은...?!

```python

archidraw.github.io  # 현재 회사 블로그 사이트입니다.

banjag954.github.io # 현재 보고 계시는 해당 사이트 입니다.

```

  <div id="List_01">

<h4> 관련 자료 </h4>

  </div>

---

1. [Jekyll 공식 사이트](https://jekyllrb.com/)
2. [Markdown 문법 참고 / GitLab](https://docs.gitlab.com/ee/user/markdown.html)
3. [+ 추가 마크다운(Markdown) 작성 문법 / VeriCras](http://blog.vericras.com/markdown-writing-rules.html)

<div id="List_02">

<h4> 레퍼런스 </h4>
</div>

---

1. [Jekyll: GitHub Pages 에 블로그 만들기](https://xho95.github.io/blog/github/pages/jekyll/minima/theme/2017/03/04/Jekyll-Blog-with-Minima.html)
2. [Jekyll을 이용한 .github.io 블로그 만들기[1] - Heee's Development Blog](https://gmlwjd9405.github.io/2017/10/06/Jekyll-github.io-blog-1.html) : **1단계** 부터 **3단계** 까지 순차적으로 따라하면 완성!
3. [Jekyll을 사용하여 GitHub Pages 만들기](http://blog.saltfactory.net/upgrade-github-pages-dependency-versions/)

<br />
<br />


###### 각주
---
