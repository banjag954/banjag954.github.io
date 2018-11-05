---

title: "04 : SaaS Project_Review"
layout: post
date: 2018-09-30 17:12
comment : true
tag:
- SaaS
- Lotte
- Project
headerImage: true
projects: true
star: false
hidden: true # don't count this post in blog pagination
description: "SaaS 프로젝트를 끝내고 나온 리뷰를 작성해본다"
category: project
author: Columbus
externalLink: false

---



# SaaS Project_Review

### Summary
---

* [프로젝트 개발 이슈](#Start)
* [문제.1 : 터치 스크린[Ver. PC]](#first)
* [문제.2 : Map API](#second)
* [문제.3 : Touch selector](#third)

---

#### 프로젝트가 끝났다...

![saas_02]({{ site.url }}/assets/images/saas_02.jpeg)

드디어 __SaaS Project__ 가 끝났다...  __Kickstarter__ 이후, 최초로 우리 서비스를 __L 백화점__ 에 납품하게 되었다.<br>
우리가 처음으로 이루어낸 또 다른 성과에 박수!! ᕕ( ᐛ )ᕗ<br>
__이번 컨텐츠__ 는 프로젝트 도중 겪은 여러 상황에 대해 적어보려한다.
<br />
<br />
<div id="Start">
<h2>프로젝트 개발 이슈</h2>
</div>
---

![saas_01]({{ site.url }}/assets/images/saas_01.jpeg)

프로젝트에서 겪은 모든 이슈를 적고 기록하고 싶지만,<br>
내가 담당했던 영역이 포함된 이슈들에 관해서만 서술할 예정이다.<br>
(~~구축 후, 제품을 운영하며 터지고 있는 이슈들을 다 적기에는 양이 너무 많다.~~)

__내용의 주제__ 는 가장 많은 트러블을 발생시킨 __[ 디바이스의 다양성 문제 ]__ 가 될 듯하다. 

## [ Problem : 디바이스의 다양성 ]

<br>
<div id="first">
<h3>문제.1 : 터치 스크린[Ver. PC]</h3>
</div>

![saas_03]({{ site.url }}/assets/images/saas_03.jpeg)

이전 브라우저 문제로 고생한 적이 몇번있어 이번 __Browser__ 는 __Chrome__ 으로만 사용하기로 했다.

__이유__ 는 __Android__ 디바이스 대부분이 Chromium을 탑재하고 있어 모바일에서도 호환이 잘되고, __IOS__ 의 경우 Safari 및 IOS 특유의 브라우저 디자인 가이드라인만 조금 잡아주면, 화면에 대한 시각적인 문제는 빠르게 잡을 수 있기 때문이였다. 

__문제__ 는 디바이스의 다양성 때문에 터지게 됬는데...<br>
당시 제품 자체가 마우스 터치 형식의 UX로 구성되어있어, 사전에 __데스크탑 PC__ 설치 하는 것으로 합의를 봤었다.

___그런데___

제품 납기 1달 전 갑자기 __터치 스크린__ 역시 매장에 전시되니, 터치 이벤트까지 적용시켜 달라한다. (~~L사 진짜 깡짜 때쓰기, 갑질 오지고 드럽다.~~)

### 문제 1. 그후...

우여곡절 끝에 끝나긴했지만,<br>
이번 경험을 토대로 서비스 구축시 __UI 화면구성__ 이외 __PC의 UX__ 역시 터치 속성을 가진 모바일부터 고려해야 할 것같다는 생각을 정말 많이 했다.
(~~_애초에 __PC는 무조건 마우스를 사용한다.__ 라는 잘못된 관념이 내 머리속에 있었던 것 같다._~~)  

<br>
<br>
<div id="second">
<h3>문제.2 : Map API</h3>
</div>

![saas_04]({{ site.url }}/assets/images/saas_04.png)

#### 초기 제품의 Map API는 __K사 지도 API__ 를 사용하였다.
<br>
__K사__ , __N사__ , __S사__ 모두 IT쪽의 유명한 회사고, 제공되는 목적성은 같기에 지도 API에 관해서 적용된 UI나 자잘한 UX 말고는 크게 다른 것이 없는 줄 알았다.
  
그리고... 제품에 __Touch event__ 가 끼게되면서 문제가 터졌다.

오픈 1주일 전, 제품 완성후 테스트를 진행하려하는데, 터치 스크린의 지도 화면이 작동이 안된다.

그리고 이리저리 만져보고, 몇시간 동안 동료들과 이야기하고 자료를 찾아보며 알았다.

### _K사 API는 개발적인 이슈로 인해, PC 버전 Touch Event를 지원하지 않는다고 한다._

각 사가 제공하는 API 형식 자체가 크게 다르지 않았고, 1~2일만에 N사가 제공하는 API로 모두 교체 할 수 있어 다행이였다.

### 문제 2. 그후...

이 문제 역시 우여곡절 끝에 마무리됬다.<br>
다음번 API를 이용할 땐, 브라우저에 대한 호환성 뿐 아니라 디바이스에 대한 호환성까지 고려하며 봐야겠다 다짐한다.

(~~_KaKao 지도 API는 PC버전 터치 이벤트가 먹지 않는다는 사실 꼭 명심하자_~~)

<br>
<br>
<div id="third">
<h3>문제.3 : Touch selectors</h3>
</div>
 
![saas_05]({{ site.url }}/assets/images/saas_05.png)

__PC 버전의 터치 디바이스__ 를 건드리게되면서, 빼먹은 자잘한 이슈가 몇개 있었는데 그 중 하나가 바로 Touch event에 대한 Selector를 고려하지 않은 부분이였다.
  
__마우스에 대한 indication__ 으로 Tooltip,hover 등의 CSS Selector를 UI에 붙여놨었는데, 터치 스크린으로 가니 아무것도 먹지않아 엄청 정적으로 보였다.

__:active, :focus 등 추가적인 Selector를 붙여주자.__<br>
Touch Selector에 대한 부분은 __Google 개발자 사이트__ 에서 잘 설명해놓았으니 참고하자.

[[ 구글 개발자 노트 : Touch screen 이벤트에 관하여 ]](https://developers.google.com/web/fundamentals/design-and-ux/input/touch/?hl=ko)
<br />
<br />
<br />