---
id: 1021
title: '임의의 점을 지나는 다항함수 구하기 &#8211; Lagrange Interpolation Formula'
date: 2017-10-25T16:21:53+00:00
author: Abraxas Academy
layout: post
tags: Mathematics
---
근 $c_1,c_2,\ldots,c_n$을 가지는 다항함수는 단순히 $f(x)=\displaystyle\prod_{i=0}^{n}(x-c_i)$로 구할 수 있었다. 근데 $(x_i,y_i)$를 지나는 걸 찾자면 문제가 좀 복잡해지는데, 그때 사용하는 것이 Lagrange Interpolation Fomula이다.

**Definition 1. 실수 $x_i(i\in\mathbb{Z^+},0\leq i \leq n$)에 대하여 Lagrange polynominals $f_i(x)$를 다음과 같이 정의한다.**

$$f_i(x)=\displaystyle\prod_{j=0,j\neq i}^{n}\dfrac{x-x_j}{x_i-x_j}$$

그럼 다음이 자명하다.

$$f_i(x_j)=\delta_{ij}$$

여기서 $\delta_{ij}$는 크로네커 델타이다. 이제 이 Lagrange polynomals의 집합이 $n$차 다항식으로 이루어진 vector space $V$의 basis라는 것을 보이자.
$$\displaystyle\sum^{n}_{i=0}a_{i}f_{i}(x)=0$$이라면, 

$c_i$를 대입해 모든$a_i=0$임을 알 수 있고 (linearly independent), 그리고 set $\\{ f_i\lvert i=0,1,2,...,n\\}$이 $V$의 subset임에서 이를 알 수 있다.

 이제 원하는 다항식($n+1$개의 점을 지나는 다항식)을 이 basis의 선형결합으로 나타내기 위한 $a_i$를 결정하면 되는데,$f_i(x_j)=\delta_{ij}$임에서 구하는 다항식을 $g(x)$라 하면

$$\displaystyle\sum^{n}_{i=0}a_{i}f_{i}(x)=g(x)$$

로부터 $a_i=g(x_i)=y_i$를 얻는다.

여기서 이제 추가로 vector space의 원소를 기저의 합으로 나타내는 방법이 유일하다는 것에서 점 $n+1$개를 지나는 다항식이 유일하다는 점과, $n$차 다항식이 $n+1$개 이상의 점에서 $0$ 이라면 $0$ 이라는 것 또한 알 수 있다.

 

예제)얼마 전에 페북에 돌아다니던 개그짤 중에 이런게 있었다.

![](https://images-cdn.9gag.com/photo/agYGyxv_700b.jpg))

&nbsp;

저 $f(x)$를 직접 구해보자.  $i=,1,2,3,4$에 대해 $(x_i,y_i)=(i,2i-1)$을, 그리고 $(5,217341)$를 지나는 다항식을 찾으면 된다. Definition 1에 의해, $f_i(x)$를 구해보면,

$$f_1(x)=\dfrac{x^4}{24}-\dfrac{7 x^3}{12}+\dfrac{71 x^2}{24}-\dfrac{77 x}{12}+5$$

$$f_2(x)=--\dfrac{x^4}{6}+\dfrac{13 x^3}{6}-\dfrac{59 x^2}{6}+\dfrac{107 x}{6}-10$$

$$f_3(x)=\dfrac{x^4}{4}-3 x^3+\dfrac{49 x^2}{4}-\dfrac{39 x}{2}+10$$

$$f_4(x)=-\dfrac{x^4}{6}+\dfrac{11 x^3}{6}-\dfrac{41 x^2}{6}+\dfrac{61 x}{6}-5$$

$$f_5(x)=\dfrac{x^4}{24}-\dfrac{5 x^3}{12}+\dfrac{35 x^2}{24}-\dfrac{25 x}{12}+14$$



이제 $f_1(x)+3f_2(x)+5f_3(x)+7f_4(x)+217341f_5(x)$을 구하면

$$\dfrac{18111 x^4}{2}-90555 x^3+\dfrac{633885 x^2}{2}-452773 x+217331$$을 얻는다.

