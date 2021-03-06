---
id: 518
title: 해석적(Analytic) 함수와 Cauchy-Riemann Condition
date: 2016-04-03T15:59:06+00:00
author: Abraxas Academy
layout: post
tags: Mathematics
---
결론부터 얘기하고 시작합시다. 다음 명제와 그 역이 성립합니다.

 

복소함수 $f(z)=u(x,y)+iv(x,y)$가 어떤 영역에서 해석적이면 , 그 영역에서 다음 식이 성립한다

 \begin{equation}
 \frac{\partial u}{\partial x}=\frac{\partial v}{\partial y},\quad\frac{\partial v}{\partial x}=-\frac{\partial u}{\partial y}
 \end{equation}

 

어떤 함수가 어떤 영역에서 "해석적(Analytic)" 하다는 것은, 그 영역에서 "Single-valued"하고 미분 가능함을, 즉 그 영역 위의 점으로 어떤 방향으로 접근해가더라도 극한값이 같음을 의미합니다.

 

이를 Cauchy-Riemann Condition이라 합니다. 증명은 다음과 같습니다. (사실 이미 전 포스팅에서 전기장을 구할 때 사용한 적이 있습니다.)

 

해석적 함수$f$를 $f=u+iv$ 로 쓰고, $z=x+iy$ 이면, $df=du+idv, \quad dz=dx+idy$입니다.

복소평면위의 점 $z_0$로 다음 두가지 접근이 가능합니다.
  ![](https://farm5.staticflickr.com/4659/39731180962_a24f334236_b.jpg)\begin{equation} \lim_{dx \to 0}\frac{du+idv}{dx}=\frac{\partial u}{\partial x}+i\frac{\partial v}{\partial x}\end{equation}

 

\begin{equation} \lim_{dy \to 0}\frac{du+idv}{idy}=-i\frac{\partial u}{\partial y}+\frac{\partial v}{\partial y}\end{equation}

 

이고, $f$가 해석적이므로 두 식을 비교하여 Cauchy-Riemann Condition이 증명됩니다.

 

이것이 중요한 이유중 하나는 역을 이용해서 어떤 함수가 어느 영역에서 해석적이라는 보장을 얻어낼수 있다는 점입니다. 이제 역을 증명해 봅시다.

$df$를 다음과 같이 씁시다.

$u$와$v$의 $x$와 $y$네 대한 편미분이 연속이면,
 \begin{equation}df=\bigg(\frac{\partial u}{\partial x}+i\frac{\partial v}{\partial x}\bigg)dx+\bigg(\frac{\partial u}{\partial y}+i\frac{\partial v}{\partial y}\bigg)dy \end{equation}

Cauchy-RIemann Condition이 성립한다면, 식(4)는

\begin{equation}df=\bigg(\frac{\partial u}{\partial x}+i\frac{\partial v}{\partial x}\bigg)dx+\bigg(-\frac{\partial y}{\partial x}+i\frac{\partial u}{\partial x}\bigg)dy =\bigg(\frac{\partial u}{\partial x}+i\frac{\partial v}{\partial x}\bigg)(dx+idy)\end{equation}
 이므로,
 \begin{equation}\frac{df}{dz}=\bigg(\frac{\partial u}{\partial x}+i\frac{\partial v}{\partial x}\bigg)\end{equation}로, 어떤 방향으로 접근하더라도 극한값이 그에 무관하게 같음을 보일 수 있습니다.

 