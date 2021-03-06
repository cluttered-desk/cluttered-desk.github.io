---
id: 505
title: 변분법과 Euler-Lagrange Equation 의 유도
date: 2016-03-06T16:09:34+00:00
author: Abraxas Academy
layout: post
tags: Mathematics
---
# 미분



지금부터 약 300여년 전, 처음으로 이뤄낸 것이 누구인지의 논란거리는 여전히 분분하지만, 숫자 등의 보다 근본적인 개념의 깨달음을 제외한다면, 미분이 인류 과학사상 가장 획기적이며, 강력한 도구의 발견인 것은 누구도 의심하지 않을 만한 사실입니다. 인류의 탄생부터 서서히 느껴오게 된 “수”라는 추상적 개념의 발전으로 확장되며 시작되게 된 수학이라는 학문이자 자연을 기술하는 훌륭한 언어가 “무한히 작은”‘, “무한히 가까워지는” 이라는 극한이라는 개념에 도달하며, 다시 이곳에서부터 미적분학까지로 이어진 여정을 뒤돌아보며 묘한 자부심을 느끼지 않는 사람은 아마 드물 것 같습니다. (이런 관점에서 본다면, 어쩌면 뉴턴과 라이프니츠가 서로 미적분학을 “발명” 했다는 논쟁은 어떤 사람들이 보기에는 기가 찬 일일지도 모릅니다.)

“아주” 작은 구간에서의 변화율이라는 개념과 이를 체계적으로 다루는 방법의 발견은 물리학의 발전(이는 곧 전체 과학분야의 발전을 의미하죠) 에 지대한 공을 세웠으며, 그를 좀 더 응용한 최대, 최소를 구하는 과정 역시 두 말할 필요가 없습니다.

# 변분

하지만 최대, 최소를 구하는 영역에는 여전히 수많은 문제들이 존재하고, 그 중에서는 물론 기존의 미분 개념으로 이용해서 풀어내기는 약간 미묘한 문제들이 존재합니다. 요컨대, 두 점 사이를 연결하는 가장 길이가 짧은 선은 무엇인가? 라는 문제나, (물론 답은 당연히 직선이지만, 엄밀하게 따지기는 막막하죠.) 혹은, 어떤 물체가 운동에너지에 그 위치에너지를 뺀 값의 합이 가장 작게 되려면, 어떤 경로를 따라 움직일 것인가? 등의 문제는 기존의 극대-극소 문제와는 다릅니다. 

그 이유는 간단합니다. 기존의 극대-극소 문제는 미분을 이용하여 도함수가 $0$이 되는 $x$값을 찾아 문제를 해결했습니다. 그러나 이 문제들은 다릅니다. “두 점을 연결하는 선”은 실수, 더 나아가서 복소수 집합 따위에 포함되는 “수”가 아닙니다. 결국 수학자들은 새로운 방법을 고안해 내기 위해 다시 한번 머리를 싸매야 했죠.

이러한 문제들을 변분법이라고 부르며, 1750년에 라그랑주와 오일러가 공동 연구 중 그 해법을 제시했습니다. 위에서 언급한 내용을 한번 더 정리한다면 변분법은 일종의 “함수를 정의역으로 가지는 함수” 들의 극값을 찾는 문제인 셈입니다. 이러한 함수를 “범함수”라 부르며, 둘은 이 문제를 해결하기 위해 다음과 같은 해법을 생각해 냈습니다.

우리가 찾는, 즉 범함수의 값을 극대 또는 극소를 가지는 경로를 $\overline{f(x)}$라 합시다. 그렇다면, 만약 이 경로에서 아주 작은 변화 $\epsilon \eta(x)$만큼의 변화를 취한 경로를 $f(x)$라 하면, 다음과 같이 쓸 수 있습니다.

$$f(x) = \overline{f(x)}+\epsilon \eta(x)$$

어떤 범함수 $J$가 경로 $f(x)$ 에서 극값을 가진다면, $\eta(x)$가 매우 작으므로, 다음을 추측해 볼 수 있습니다.

$$J(f(x))-J(\overline{f(x)})=0$$

물론 엄밀한 논증은 아니지만, 롤의 정리를 증명할 때를 연상한다면 직관적으로 받아들이는 데에는 큰 문제는 없으리라 생각됩니다. 바로 이것이 이러한 종류의 문제, 변분을 해결하는데 핵심적인 아이디어가 되며, 두명의 수학자(라그랑주와 오일러)는 이를 일반화시켜 Euler-Lagrange Equation을 유도해내었고, 즉 변분 문제의 일반적 해법을 제시하였습니다.


범함수 $J$를 다음과 같이 정의합시다.

$$J=\int_{a}^{b}F\lbrace{x,f(x),f^{'}(x)}\rbrace dx$$

여기서 $F$를 위와 같이 정의하는 이유는 변분법의 문제들 중 위와 같은 꼴로 썼을 때 더 편한 경우가 많기 때문입니다.

우리가 찾는 "진짜"경로를 $\overline{f(x)}$라고 하면, 이경로에서 조그마한 변화를 준 경로들은 다음과 같이 쓸 수 있습니다.

$$f(x)=\overline{f(x)}+\epsilon \eta(x)$$

이제 $J$를 $\epsilon$에 대하여 미분합시다.

$$\frac{dJ}{d\epsilon}=\int_{a}^{b}\frac{dF}{d\epsilon}\lbrace{x,f(x),f^{'}(x)}\rbrace dx$$

적분 기호 내부에 변수가 여러개인 함수의 미분이 생겨 버렸는데, 다음과 같이 생각하여 해결할수 있습니다(전미분). 변수가 여러개인 함수는 말 그대로 여러개의 변수에 의해 그 함숫값이 변합니다. $dy=\dfrac{dy}{dx}dx$ 였던 것처럼, 각 변수에 의한 기울기에 미소 변위만큼을 곱하면 함숫값의 차를 얻을 수 있죠. 따라서 다음과 같이 생각할 수 있습니다.

$$df(x,y,z)=\frac{\partial f}{\partial x}dx+\frac{\partial f}{\partial y}dy+\frac{\partial f}{\partial z}dz$$

따라서,

$$\frac{dJ}{d\epsilon}=\int_{a}^{b}\frac {dF}{d\epsilon}dx = \int_{a}^{b}\lbrace\frac{\partial F}{\partial x}\frac{dx}{d\epsilon} + \frac{\partial F}{\partial f}\frac{df}{d \epsilon} + \frac{\partial F}{\partial f^{'}}\frac{df^{'}}{d \epsilon}\rbrace dx \\= \int_{a}^{b}\lbrace \eta(x) \frac{\partial F}{\partial f} + \eta'(x) \frac{\partial F}{\partial f^{'}} \rbrace dx$$

$\epsilon$이 0이라면 $f(x)=\overline{f(x)}$이므로

$$\frac{dJ}{d\epsilon} \bigg|_{\epsilon=0} = 0 =\int_{a}^{b}\lbrace \eta(x) \frac{\partial F}{\partial \overline{f}} + \eta'(x) \frac{\partial F}{\partial \overline{f^{'}}} \rbrace dx$$

두번째 항에 부분적분을 하면,

$$\int_{a}^{b}\eta'(x) \frac{\partial F}{\partial \overline{f^{'}}} dx=\eta(x)\frac{\partial F}{\partial \overline{f^{'}}}\bigg|_{a}^{b}-\int_{a}^{b}\eta (x) \frac{d}{dx}\frac{\partial F}{\partial \overline{f^{'}}}dx$$

이 식의 첫번째 항은 0입니다. $a$에서 시작해 $b$로 가는 경로들에 대해 다루고 있기 때문에, $\eta(a)=\eta(b)=0$이 됨은 자명합니다. 이제 다시 쓰면,

$$\int_{a}^{b}\eta(x)\bigg[\frac{\partial F}{\partial \overline{f}}-\frac{d}{dx}\frac{\partial F}{\partial \overline{f^{'}}}\bigg]dx$$

따라서

$$\frac{\partial F}{\partial \overline{f}}-\frac{d}{dx}\frac{\partial F}{\partial \overline{f^{'}}}=0$$

이고, 이것이 Euler-Lagrange Equation 입니다.