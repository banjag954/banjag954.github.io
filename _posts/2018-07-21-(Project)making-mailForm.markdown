---
title: "02 : 온라인 명함 [Signature / 서명] 만들기"
layout: post
date: 2018-07-21 16:55
comment : true
tag:
- mailForm
- Signature
headerImage: true
projects: true
hidden: true # don't count this post in blog pagination
description: "온라인 명함 [Signature / 서명] 만들기"
category: project
author: Columbus
externalLink: false
---

#### 개요

과거에 비해 인기가 많이 식었지만,
페이스북, 인스타, 트위터 등 여러가지 미디어 채널과 함께 현재까지 많이 사용되는 도구 ‘__E-mail__’

‘__E-mail__’은 마케팅 용도 뿐만이 아니라, 그룹 혹은 업체간의 소통을 위한 수단으로 현재까지 널리 사용되고있다.
한번이라도 회사에서 컴퓨터로 업무를 보고, 타 부서 혹은 업체와의 소통을 위해 보통 메일을 작성한 경험이 있는 사람이라면, 메일 하단에 아래의 문구를 본 적이 있을 것이다.

---
__홍 길 동__ <br />

시니어 풀스택 개발자<br />
010-1234-5678<br />
xxx@xxxx.xxx<br />

---

위와 같은 메일을 꾸며주는 자료 혹은 소스를 가르켜 ‘Mail Form’이라 명시한다.
오늘은 이 mailForm 제작기에 대해 적어보려한다.


### Summary
---

* [상황](#Why)
* [프로젝트 진행 계기](#Situation)
* [프로젝트 결과](#Project)
* [결과물 적용](#Upload)
* [프로젝트 고려사항](#List)

---

<div id="Why">
<h4>상황</h4>
</div>

현재 다니고 있는 아키드로우라는 회사에서 몇일 전 대표님께 이런 이야기를 들었다.
<br />

_“ 이메일 하단에 명함처럼 꾸며진 메일폼 때문에, 메일을 받는 VC 혹은 다른 외부 사람들이 많은 핀잔을 받아 화가난다. "_
<br />

![anger_image]({{ site.url }}/assets/images/giphy.gif)

대체 왜? 무엇 때문에 욕을 먹었을까?<br />
당시 대표님이 받아온 컨펌의 내용은 여러가지 였지만, 그것들이 공통적으로 이야기하는 결론은 __"너희 회사가 정말 존재하고, 제대로 운영되는 것이 맞느냐?"__ 였다.

---

__로고, 명함, 웹사이트, 다른 SNS 매체... 등__

---
회사를 설립할때, 기업은 자신의 정체성을 간략하게 노출시킬 수 있는 몇가지 매개물을 준비한다.

그 중에서 외부 사람들과의 접촉 전/후에 서로 나눠같는게 보통 __'명함'__ 인데, 외부 사람들이 보기에 온라인 명함격인 __[서명/Signature]__ 이라는 컨텐츠 조차 만들어있지 않은 것이 기업으로서 미흡한 것처럼 보였나보다.

~~사실 그것말고도 여러가지 엄청 미흡한 것들이 많이 보였을 텐데... 그 중 하나를 디테일하게 언급한것 같다.~~

---

<div id="Situation">
<h4>프로젝트 진행 계기</h4>
</div>

위와 같은 이유로 Signature_MailForm을 제작하게 되었는데, 이 작은 프로젝트를 진행한 내가 진행한 배경은 다음과 같다.

<div style=" font-size:15px; font-style: italic; line-height : 24px; ">

- 개발자분들에게 만들어 달라부탁하니, 정말 사소한 업무라 하며 하기 귀찮아했고, <br />
- 상대방이 나에게 요청한 디자인소스 workForce가 더 커보였고, <br />
- 요청한 작업의 완료기한은 미정, 그리고 부탁한 개발자가 정말 대충 만들 것 같아서였다. <br />

</div>

그래서 그냥 내가 만들기로 했다.

---

<div id="Project">
<h4>프로젝트 결과</h4>
</div>
내가 __간단하게 제작한 소스__ 및 __작업 중간에 겪은 문제 및 해결방법__ 에 대한 정보를 적어본다.

일단 MailForm에 관한 코드는 아래와 같다.

~~~html
<!doctype html>
<html lang="en">
 <head>
  <meta charset="UTF-8">
  <meta name="Generator" content="">
  <meta name="Author" content="">
  <meta name="Keywords" content="">
  <meta name="Description" content="">
  <meta name="viewport" content="width=device-width,user-scalable=no" />
  <title>Archisketch - mail</title>
 </head>
 <body>

   <div style="width:100%; margin:0 auto;">
     <div style="padding:0px; background:#67AFC2;">
         <div><img src="https://i.imgur.com/M2ukmNp.png" alt="ARCHISKETCH_LOGO" title="source: imgur.com" style="float:right; padding: 54px 20px 0px 0px; display:block; width:140px;"></div>
         <div><img src="https://i.imgur.com/3z5BBVz.png" alt="ARCHIDRAW_LOGO" title="source: imgur.com" style="float:left;padding: 20px 0px 0px 20px;display:block;width:140px;"></div>
         <div style="padding:48px 20px 0px;font-size: 16px;font-weight:bold;color:#fff;line-height: 32px;">
            ​Columbus( Junsu ) Kim
            <div style="padding: 10px 0px;font-size: 10px;color:#fff;font-weight:lighter;line-height:140%;">
              Service architect &amp; product management<br>
              Tel : +82)10-2090-3029<br>
              E-mail : banjag954@archidraw.net​​​​<br>
            </div>
          </div>
     </div>
   </div>

 </body>
</html>
~~~

어짜피 이메일 서명란에 사용된 후, 언제 다시 사용될지 모를 코드이기에 간단하게 html 파일 하나로 만들었다.

> 1. _div 옆에 Style 이라 붙어있는 것들은 CSS 코드 입니다._
> 2. _위의 문법은 정말 기초적인 html 문법만 알아도 사용가능 하실 겁니다._
> 3. _위의 코드 수정이 어려우시다면, __'생활 코딩'__, 혹은 __'W3SCHOOL'__ 같은 무료 강의 사이트에서 1시간만 투자하여 html,css 강의를 듣는 것을 추천드립니다._
> 4. ~~코드가 이쁘지 않은건... 귀엽게 봐주세요. 있을 건 다 있어요! ㅎ~~

모양은 아래의 이미지와 같다.

![mailForm_image]({{ site.url }}/assets/images/e-mail_01.png)

---
<div id="Upload">
<h4>결과물 적용</h4>
</div>

우리는 이제 mailForm을 다 만들었다.
그럼 이것을 어디에 붙여야하는가?

1. E-mail 사이트의 위, 아래를 찬찬히 살펴보면 __[SETTING/설정]__ 이라는 버튼이 보일 것이다. 그 __[SETTING/설정]__ 버튼을 클릭하자.

2. __[SETTING/설정]__ 버튼 클릭후, __[Signature / 서명]__ 탭에 들어가자.

3. 그 후, Input Bar 안에 제작한 __HTML CODE__ 를 서명 글에 집어 넣자. 그럼 끝이다.

---
<div id="List">
<h4>프로젝트 고려사항</h4>
</div>

<br />

##### 1. Viewport 설정

요즘은 이메일을 노트북, PC 말고 모바일 디바이스에서도 E-mail 많이 읽는다.

모바일 <-> PC 디바이스 전역의 최적화를 위해 Head 태그안에 아래와 같은 Viewport를 설정해준다.

~~~html
<meta name="viewport" content="width=device-width,user-scalable=no" />
~~~

Viewport에 대한 자세한 내용이 궁금하면 더보기 클릭! [[더보기]](https://developer.mozilla.org/ko/docs/Mozilla/Mobile/Viewport_meta_tag)

<br />

##### 2. 무료 이미지 공유 사이트 활용

![mailForm_image]({{ site.url }}/assets/images/imgur_01.png)

보통 메일폼에 보면 글자들과 함께 이미지들이 같이 노출되는데, 이는 사용될 이미지를에 서버에 저장하고, 웹에 띄우기에 반영이 되는 것이다.

> _그렇다면... 메일폼 __'하나'__ 만드는데, 이를 위한 독자적인 서버를 하나 구축해야 한단 말인가..? ~~(크게 일벌리기는 생각 및 행위는 지양하도록하자.)~~_

위의 코드를 쭉 읽다보면, img 태그 옆에 어딘가로 통하는 링크가 걸려있는 것을 볼 수 있다.

~~~
img src="https://i.imgur.com/M2ukmNp.png"
~~~


그렇다. <br />
__imgur__ 라는 무료 이미지 공유 사이트를 이용할 것이다.<br />
이 사이트는 웹에 사용할 수 있게 자동으로 이미지 최적화도 해주고, 각 소스를 이용할 수 있는 호환된 코드도 제공해준다.

![mailForm_image]({{ site.url }}/assets/images/imgur_02.png)

추가적으로 imgur는 이미지'만' 관리하기도 가능하니 이런 여러가지 서비스들을 유용하게 사용하도록 하자.
