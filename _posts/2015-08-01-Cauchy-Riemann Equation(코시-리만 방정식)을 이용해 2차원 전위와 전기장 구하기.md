---
id: 65
title: Cauchy-Riemann Equation(코시-리만 방정식)을 이용해 2차원 전위와 전기장 구하기
date: 2015-08-01T17:05:20+00:00
author: Abraxas Academy
layout: post
Tags: Physics
---
기본적으로 어떤 대전되어있는 도체의&nbsp;전위의 함수를 찾는 일은 다음 방정식의 해를 구하는 작업으로 요약되지요.

\begin{equation}\nabla^{2}\phi=0\end{equation}

가우스 법칙에 의해&nbsp;

\begin{equation}\nabla \cdot \vec{E} = \frac{\rho}{\epsilon_{0}}\end{equation}

이니까 자유공간에서는&nbsp;

\begin{equation}\nabla\cdot(\nabla\phi)=\nabla^{2}\phi=0\end{equation}

이 되겠지요.

어쨌든, 풀어쓰면 다음과 같은 식이 됩니다.

\begin{equation}\frac{\partial^{2}\phi}{\partial x^2}+\frac{\partial^{2}\phi}{\partial y^2}=0\end{equation}

이걸 만족하는 함수를 어떻게 찾냐가 문제인데, 여기에 Cauchy-Riemann Equation 을 사용합니다. 다음과 같이 생겨먹었습니다.

복소수 $\delta =x+iy$를 정의역으로 가지는 복소함수가 $F(\delta)=U(x,y)+iV(x,y)$일때, 일반적으로 다음이 성립합니다.

\begin{equation}\frac{\partial U}{\partial x}=\frac{\partial V}{\partial y}\end{equation}

\begin{equation}\frac{\partial V}{\partial x}=-\frac{\partial U}{\partial y}\end{equation}

식을 조금만 찬찬히 뜯어보면 $U$와 $S$가&nbsp;

\begin{equation}\frac{\partial^{2}U}{\partial x^2}+\frac{\partial^{2}U}{\partial y^2}=0\end{equation}

\begin{equation}\frac{\partial^{2}V}{\partial x^2}+\frac{\partial^{2}V}{\partial y^2}=0\end{equation}

를 만족하는 것을 알 수 있죠.



운 좋게도, 아무 $F(\delta)$나 잡으면 거기에 대응되는 &#8220;수학적으로 가능한&#8221; 전위의 함수를 뽑아낼수 있다는 겁니다. 답을 먼저 알아낸 뒤 상황을 끼워맞추는 방식이라는 치명적 단점이 있기는 하지만, 뭐, 그래도 이게 어디에요.

한가지 예를&nbsp;들어보겠습니다.

\begin{equation}F(\delta) = \delta^{2} = x^{2}-y^{2}+i2xy\end{equation}

일때 $x^{2}-y^{2}$의 그래프를 그려보면,





  ![url=https://flic.kr/p/DV6dh8](https://farm5.staticflickr.com/4700/24885991567_e60177b148.jpg)  &nbsp; &nbsp; &nbsp;![url=https://flic.kr/p/DV6dik](https://farm5.staticflickr.com/4653/24885991637_55d8f67336.jpg)

이런 그래프가 얻어집니다. 그라디언트를 씌워서 전기장을 그려보면,

!![url=https://flic.kr/p/DV6djT](https://farm5.staticflickr.com/4655/24885991727_2328a5fa87.jpg) ![url=https://flic.kr/p/DV6dfV](https://farm5.staticflickr.com/4605/24885991497_201144778f.jpg)

이런 그래프가 얻어집니다. 즉, 직각으로 되어있는 전극의 전위와 전기장으로 생각할수 있습니다.

개인취향차는 있겠지만, 아무 함수나 잡아놓고 무슨 상황인지 때려맞춰보는것도 재밌겠네요. 실수부 허수부 분리, 그라디언트 씌우기는 울프럼 알파가 다 해주니, 사람은 그저 생각만 조금 해보면 되겠군요.