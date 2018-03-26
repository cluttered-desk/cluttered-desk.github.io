---
id: 578
title: 변분법을 이용해 현수선이 Hyperbolic Cosine임을 증명하기
date: 2016-06-14T05:42:28+00:00
author: Abraxas Academy
layout: post
tags: Physics
---
기본적인 아이디어는 간단합니다. 현수선은 양쪽이 고정되어있는 (밀도가 균일한)줄이 늘어져 있는 모양입니다.

그럼 이 상황에서 "최소화" 되는 물리량이 무엇인지만 알아내서 Euler-Lagrange Equation만 풀어주면 그만이죠.

 

당연히 최소화되어야 할 값은 줄 전체의 퍼텐셜입니다. 퍼텐셜이 극값이여야 힘이 평형을 이룸은 자명하겠지요. 따라서 범함수 $J$를 다음과 같이 설정합시다.

 

$$ J=\rho g \int^{x_2}_{x_1}yds $$

여기서 $\rho$는 선밀도입니다. 딱히 중요하지는 않아요.

따라서 다음과 같습니다. 

 

 

$$ J=\rho g \int^{x_2}_{x_1}y\sqrt{1+(y^\prime)^2}dx $$



Euler-Lagrange Equation 에 대입하면



$$\frac{\partial F}{\partial y}-\frac{d}{dx}\frac{\partial F}{\partial y^{\prime}}=0$$

 

$$\sqrt{1+(y^\prime)^2}-\dfrac{d}{dx}\bigg(\dfrac{y y^{\prime}}{\sqrt{1+(y^\prime)^2}}\bigg)=0$$
 

두번째 항을 계산하면($x$로 미분)

$$\sqrt{1+(y^\prime)^2}-\dfrac{(y^{\prime})^2+yy^{\prime\prime}}{\sqrt{1+(y^\prime)^2}}+\dfrac{y(y^{\prime})^2{y^{\prime \prime}}}{(1+(y^\prime)^2)^{\frac{3}{2}}}=0$$

정리하면 다음을 얻습니다.



$$\dfrac{d}{dx} \dfrac{y}{\sqrt{1+(y^\prime)^2}}=0$$



 따라서 최종적으로 다음을 얻습니다.

 

$$\dfrac{y}{\sqrt{1+(y^\prime)^2}}=C$$

 

해당 미분방정식의 해가 $\cosh$로 표현됨은 명백하므로, 증명이 끝납니다.

 