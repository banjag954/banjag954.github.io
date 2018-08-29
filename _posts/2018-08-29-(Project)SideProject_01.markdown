---

title: "SideProject_01 : KaKaoTalk을 Clone하며, CSS와 친해지기"
layout: post
date: 2018-08-29 00:10
comment : true
tag:
- SideProject
- Kakao-clone

headerImage: true
projects: true
star: false
hidden: true # don't count this post in blog pagination
description: "KaKaoTalk을 Clone하며, CSS와 친해지기"
category: project
author: Columbus
externalLink: false

---
<br>

### Summary
---

* [사이드 프로젝트를 시작한 동기와 배경](#reason_01)
* [결과물과 복습](#output)
* [레퍼런스](#reason_02)

---
<br>
<br>
<br>

<div id="reason_01">
<h2>사이드 프로젝트를 시작한 동기와 배경</h2>
</div>

---

![Start]({{ site.url }}/assets/images/startup-photos.jpg)

- 눈에 보이는 단순 __그리는 UI__ 가 아닌 __구축하는 UI__ 의 과정을 경험해보기 위해
- 눈앞에 보이는 __디자인/기획__ 의 시야를 __개발__ 까지 확대하고 싶어서
- 개발자의 입장을 느껴보고 싶어서
- 순수 내 욕심 때문에...등

<br>
내가 개발 을 배운 __배경__ 은 여러가지였지만, 시작하게된 __동기__ 는 __생존__ 을 위해서였다.

<br>
> ___" 개발을 다 배울 필요는 없는데, 적당히 개발자랑 소통할 수 있을 만큼은 아는게 좋은 건 맞는거 같아... "___

<br>

나는 귀가 많이 얇은 편이다.<br>
개발을 배우기 전 주변의 사람들이 위와 같은 의미 전달을 나에게 많이 하더라.<br>
( ~~아님 그 당시의 내가 그냥 민감하게 받아들였을 수도~~ )

나는 명확한 단어가 아니면 이해를 잘하지 못한다. <br>
그 __적당히__ 라는 단어가 어느정돈지 그 당시 이해를 못했고, 내가 경험 할 수 있는 최대한을 경험해보자 생각했다.<br>

__얕게 체험하기 보다는 깊게 빠져보는게 여러모로 경험상 많은 도움이 된다는 걸 느꼈기 때문이다.__

학원, 독학 ...등 그렇게 개발을 배우고 나서 그들의 입장을 조금이나마 고려할 줄 알게 됐고, 그들과 소통을 할 수 있게 될 즈음에 한동안 코딩을 접었는데...

최근에 문득 지금까지 배운 것들을 사용 못 한다는 것이 너무 아쉽고, 아까웠다. <br>
그래도 나름 내 시간 비용이 투자됬는데...

---

__배운 것들이 잊혀지는 느낌이 싫었다.__ <br>
__이것들과 조금 더 친해지고, 코딩에 익숙해지고 싶었다.__

---

지금 프로젝트들을 시작하게된 동기는 단순히 위의 이야기가 전부이다. <br>
그럼 어디까지를 __프로젝트 범위__ 로 잡고 나눠가며 진행하는 것이 좋을까?

<br>
> ___지금까지 건드려본 Front-end 영역의 전반을 다시 더 자세하게 건들여 볼 것이다.___

<br>

어찌됫든 부족한 나의 밑단을 여러 프로젝트들을 진행하며 다지고자 한다. <br>
그래서 시작했고, 처음 결과물이 나왔다.

<br>
<br>
<br>


<div id="output">
<h2>결과물</h2>
</div>

---

이번 __Side-project__ 를 통해 얻은 결과물은 아래 링크를 클릭하면 볼 수 있다.

[[ Kakao-clone ] 결과물 보기](https://banjag954.github.io/sideProject-kakaoClone/)

<br>
![image]({{ site.url }}/assets/images/typography-poster-posters-quote.jpg)

#### _이번 프로젝트는 __HTML__ 과 __CSS__ 친해지는 것이였다._

<br>
순수 __HTML__ 과 __CSS__ 만을 활용하였고,
작업한 __Web Site__ 를 __Web App__ 으로 최적화키는 것까지 작업하였다. ( ~~IOS 쉣!!!~~ )

### 프로젝트 진행시, CSS에서 막혔던 부분 ( 복습 / 참고 )

#### 01.특정 태그를 선택해서 속성을 지정해 줄 수 있는 css

```css

Last-child :
Nth-child :

```

#### 02.Display:flex; 그와 연관되는 css 문법들 <br>

flex가 막힌다면, 레퍼런스에 적어 놓은 [[3.어린아이도 배울 수 있는 Flexbox-froggy]](http://flexboxfroggy.com/#ko) 를 복습해보자.


```css

justify-content :
align-items :
align-self :
flex-direction:
flex-wrap:

```

#### 03.IOS 디바이스 INPUT 최적화

아이폰에서 input 태그를 보면 디바이스에 따른 스타일 속성이 기본으로 적용되는데 그 중 하나가 바로 테두리이고 내부의 그림자이다.
IOS INPUT 최적화시, CSS 문서에 아래의 부분을 주의해서 기입해 놓자.

```css

input {
   -webkit-appearance: none;
   -webkit-border-radius: 0;
}

추가적으로,

input:focus {
   해당 태그 내부에서, placeholder 클릭시 생성되는 border 속성을 조절할 수 있음
}

```

__appearance__ css속성은 적용된 그림자 또는 기타 디폴트(default) 스타일 속성을 임의로 제거 또는 설정 가능하도록 해준다.
그리고 __border-radius__ 로 테두리를 제거할 수 있다.


노가다는 많았지만,<br>
__CSS__ 와 친밀해 질 수 있어 좋았고, 결과물도 이쁘게 나와 만족한다.
<br>
<br>
<br>

<div id="reason_02">
<h2>레퍼런스</h2>
</div>

---

자잘하지만, 중요하다.<br>
이번 프로젝트 진행 중, 나중에 다시 참고할 레퍼런스들을 모아본다.


1. [ Apple: Safari Web Contents Guide Line ](https://developer.apple.com/library/archive/documentation/AppleApplications/Reference/SafariWebContent/ConfiguringWebApplications/ConfiguringWebApplications.html)
2. [ 최적화를 위해 브라우저 및 디바이스 별 붙여줘야하는 meta tags ](https://speckyboy.com/creating-a-mobile-web-application-with-meta-tags/)
3. [어린아이도 배울 수 있는 Flexbox-froggy](http://flexboxfroggy.com/#ko)
