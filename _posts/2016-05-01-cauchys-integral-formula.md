---
id: 576
title: 'Cauchy&#8217;s integral Formula'
date: 2016-05-01T16:12:48+00:00
author: Abraxas Academy
layout: post
tags: Mathematics
---
Cauchy's Integral Theorem에서 파생된 하나의 또 다른 공식은 Cauchy's Integral Formula 입니다. 이 정리와 이를 보다 일반화시킨 Residue Theorem(유수 정리)를 이용하면 정적분의 계산을 상당히 편하게 할 수 있습니다.

 

복소함수 $f(z)$를 생각합시다. 이 복소함수 $f(z)$가 폐곡선 $C$와 그 내부의 영역에서 해석적이라고 하면 다음 식이 성립합니다.

 

 

\begin{equation}
 f(z_0)=\frac{1}{2\pi i}\oint_c \frac{f(z)}{z-z_0}dz
 \end{equation}
 여기서 \z_0\는 $C$ 내부의 영역입니다. (여기서 자연스럽게 Analytic하지 않은 함수에 대해서는 Cauchy's Integral Theorem이 성립하지 않음이 암시됩니다. $\frac{f(z)}{z-z_0}$는 $z_0$에서 해석적이지 않으니까요.)
 증명은 다음과 같습니다.

 $\dfrac{f(z)}{z-z_0}$을 다음 경로를 따라 적분합시다.

![](https://farm5.staticflickr.com/4750/39764021371_7ddaa6d28c_b.jpg)

  위 경로를 $1,2,3$의 세 경로로 나누어 생각합시다. $1$은 아무 경로나 잡은 것이고, $3$은 $z_0$을 중심으로 하는 반지름 $r$을 가지는 원형의 경로입니다.  그렇다면 위 경로를 따라 적분한다면, Cauchy's Integral Theorem에 의해 그 값은 0 입니다. ($f(z)$가 해석이라는 가정 때문에 해석적이지 않은 유일한 점이 $z_0$뿐입니다.) 이제 $3$의 경로의 반지름 $r$을 $0$으로 보냅시다. 그렇게 된다면 $2$의 경로가 서로 겹치게 되어 상쇄되고, 다음과 같게 됩니다.

 

\begin{equation}
 \oint_{C_1(Clockwise)}\frac{f(z)}{z-z_0}dz+\oint_{C_3(Counter-Clockwise)}\frac{f(z)}{z-z_0}dz=0
 \end{equation}

 

그런데 $C_3$의 경로에서, 이 경로가 원형 경로이므로,

 

 

 

 

\begin{equation}
 \oint_{C_3(Clockwise)}\frac{f(z)}{z-z_0}dz=\lim_{r \to 0}\int^{2\pi}_0\frac{f(z_0+re^{i\theta})}{z_0+re^{i\theta}-z_0}ire^{i\theta}d\theta=2\pi if(z_0)
 \end{equation}

 

$Clockwise$와 $Counter-Clockwise$로 적분한 것은 부호만 반대이므로, 

 

 

\begin{equation}
 \oint_{C_1(Clockwise)}\frac{f(z)}{z-z_0}dz=\oint_{C_3(Clockwise)}\frac{f(z)}{z-z_0}dz=2\pi if(z_0)
 \end{equation}

가 되어 성립합니다.

 