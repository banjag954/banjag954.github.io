---
title: "05 : Node & NPM 설치 및 버전 관리 방법"
layout: post
date: 2018-09-26 16:24
comment : true
# image: /assets/images/markdown.jpg
headerImage: false
tag:
- development
- learn
star: false
category: blog
author: Cole Kim
description: Node 설치 및 버전 관리 방법
---

# Node & NPM 설치 및 버전 관리 방법

### Summary
---

* [Node& NPM 설치](#Start)
* [버전 업데이트](#reason_01)
* [참고 자료](#ref)

---

CSS 영역만 주구장창 파던 어느날, 다시 Node와 NPM을 다시 건드릴 때가 왔다.
문제는... 너무 Node와 NPM을 예전 살짝만 맛보고, 최근 아예 건드리질 않았더니... 업데이트 방법을 까먹었다는 것!! ㅎ....
다음에도 비슷한 상황이 발생될 것을 알기에, 건망증이 심한 나를 위해 적어 두자! 

<br />

<div id="Start">
<h2>Node 및 NPM 설치</h2>
</div>
---

노드 설치는 구글에 NodeJS라고 치고, Node WebSite에서 설치하자. 링크는 하단에! 

[ Node-install ](https://nodejs.org/ko/)

사이트에 들어가면 2가지의 __Node install__ 파일들이 나온다.

__LTS__ 와 __Current__ 2가지 버전으로 나뉘는데 이것은 무슨 차이일까?

<br />
__LTS(Long Term Supported)__ 는 장기적으로 안정되고 신뢰도가 높은 지원이 보장되는 버전으로, 유지/보수와 보안(서버 운영 등)에 초점을 맞춰 대부분 사용자에게 추천되는 버전이라고 한다.
LTS는 보통 짝수 버전(ex. 8.x.x)을 사용한다.

__Current(현재 버전)__ 은 최신 기능을 제공하고 기존 API의 기능 개선에 초점이 맞춰진 버전으로, 업데이트가 잦고 기능이 변경될 가능성이 높기 때문에 간단한 개발 및 테스트에 적당한 버전이라 한다.
Current는 홀수 버전(ex. 9.x.x)을 사용한다. ~~_근데 지금 버전은 10.11.0 인데... 짝수 번호 무엇?!_~~

<br />

보통 많이 설치하는 __LTS__ 파일로 설치 후, 터미널에 Node 와 NPM이 잘 깔렷는지 확인해보자. 
___(Node를 설치하면, NPM이 1+1으로 설치된다. )___

설치 후, 터미널을 통해 아래와 같이 잘 설치되었는지 확인해보자.

```

$ node -v
# v8.12.0

$ npm -v
# 5.6.0

```

<br />
<br />
<br />

<div id="reason_01">
<h2>버전 업데이트</h2>
</div>
---

 __Node__ 와 __NPM__ 2가지 버전 관리 방법에 대해 짧막한 설명은 다음과 같다.
 

__01. Node Update 방법__

Node 업데이트 관리 방법 툴은 크게 NVM과 N으로 나뉘는데, 사용방법은 아래의 URL을 참고하자 <br>
~~슈퍼 개발자들이 적어논 레퍼런스는 사랑입니다.~~

__NVM__ 과 __N__ 의 차이점은<br>
__NVM__ 은 설치전 충돌 방지를 위해 기존의 설치된 노드 버전을 삭제하고 진행해야하는 반면, __N__ 은 기존 설치된 노드를 제거할 필요없이 전역으로 설치하면 된다는 점이다.

__01.01 NVM 사용법__ <br>
[ Node Version Manager 사용법 바로가기 ](https://github.com/creationix/nvm#usage-1)

__01.02 N 사용법__ <br>
[ N 사용법 바로가기 ](https://github.com/tj/n#usage)


__01.03 Error : N 과 NVM 설치 및 작동이 되지 않을 경우__<br>
__( n: command not found )__

~~후... 현재의 내 상황이다..~~

~~스택오버플로우, 깃 등 여러가지에서 찾아봤는데, 그냥 다시 노드를 설치하라는 답변이 다수... ㅎ....~~<br>

~~과감하게 기존 노드 삭제 후, 터미널에 아래의 코멘트를 입력하자.~~

```
$ brew install node --latest
```

### 2018.10.16

__방법을 찾았다. 쓰벌.__

 __NPM과 연관된 다른 스크립트, 플러그인 다 되지 않아 계속 찾아봤다.__<br>
 __문제를 찾아보는 단어가 잘못됬더라. _(검색 : n: command not found)___<br>
 __이 경우는 NPMRC 패칭 문제일 수도 있다.__
 <br>
 __레퍼런스는 아래를 참고.__

 [Stackoverflow : n: command not found ](https://askubuntu.com/questions/608661/command-not-found-when-executing-node-js-n-package-on-sudo)

추가로 예전에 대답한 답변으로써, 현재 hidden files를 보려면 __[ cmd+shift+. ]__ 을 클릭해야 한다는 점 명심하자.<br>

 나의 경우엔 NPMRC에 /bin 이 하나 더 들어가 있어서...<br>
 (ex] /usr/local/bin/bin 이였다 ㅡㅡ)<br>
 진짜 /bin 하나로 전역으로 설치한 npm 플러그인들이 먹통이되다니 화가난다. 

<br>
__02. NPM Update 방법__

01. 먼저 NPM의 버전을 확인 후,

```
$ npm -v
# 5.4.0
```

02. npm install -g npm 을 입력하자! ~~응? npm이... npm을 재설치..?~~
권한 문제로 설치가 안될 시, 앞에 sudo를 붙여 설치하자!

```html
$ sudo npm install -g npm

or

$ sudo npm i -g npm /* <- 위와 같은 명령어 (i = install) 이다. */

Password:
/Users/kimjunsu/.npm-global/bin/npx -> /Users/kimjunsu/.npm-global/lib/node_modules/npm/bin/npx-cli.js
/Users/kimjunsu/.npm-global/bin/npm -> /Users/kimjunsu/.npm-global/lib/node_modules/npm/bin/npm-cli.js
+ npm@6.4.1
updated 1 package in 6.593s
```

03. 위와 같이 설치가 제대로 됬으면 다시 버전을 확인하자!

```
$ npm -v
# 5.6.0
```

<br />
<br />
<br />

<div id="ref">
<h2>참고 자료</h2>
</div>
---

1. [ How to Upgrade Node.js via NPM ](https://tecadmin.net/upgrade-nodejs-via-npm/)
2. [ N 설치 및 사용방법 ](https://github.com/tj/n)
3. [ 처음 시작하는 Node.js 개발 - 1 - 설치 및 버전 관리(NVM, n) ](https://heropy.blog/2018/02/17/node-js-install/)
<br />
<br />
<br />
