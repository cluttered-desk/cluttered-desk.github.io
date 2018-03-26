---
id: 520
title: 'Cauchy&#8217;s Integral Theorem'
date: 2016-04-03T16:57:39+00:00
author: Abraxas Academy
layout: post
tags: Mathematics
---
코시의 적분정리(Cauchy's Integral Theorem)는 다음과 같습니다.

 

만약$f(z)$가 복소평면의 단순연결된 영역의 모든 점에서 해석적이고, $C$가 그 영역 안에 있는 폐곡선이면, 다음이 성립한다.

 

 

\begin{equation}
 \oint _C f(z)dz = 0
 \end{equation}

 

여기서, 어떤 영역이 단순연결이라는 것은 그 영역 내의 임의의 폐곡선을 연속적으로 축소시켜 점으로 만들 수 있음을 의미합니다. 쉽게 이야기하면 구멍이 뚫려있지 않다는 이야기입니다. 이 정리는 후에 코시의 적분공식(Cauchy's Integral Fomula)을 유도할때 사용하는 등 활용도가 높습니다. 증명은 다음과 같습니다.

 

 

\begin{equation} \oint _C f(z)dz = \oint _C (u+iv)(dx+idy)=\oint _C (udx-vdy)+i\oint _C(vdx+udy)\end{equation}

폐곡선에 대한 선적분이므로 Stokes' 정리를 사용합시다.

따라서

 \begin{equation}\oint _C (udx-vdy)=-\iint_A\bigg(\frac{\partial v}{\partial x}+\frac{\partial u}{\partial y}\bigg)dxdy\end{equation}
 \begin{equation}\oint _C (vdx+udy)=i\iint_A\bigg(\frac{\partial u}{\partial x}-\frac{\partial v}{\partial y}\bigg)dxdy\end{equation}
 대입하면
 \begin{equation}
 \oint _C f(z)dz = -\iint_A\bigg(\frac{\partial v}{\partial x}+\frac{\partial u}{\partial y}\bigg)dxdy+i\iint_A\bigg(\frac{\partial u}{\partial x}-\frac{\partial v}{\partial y}\bigg)dxdy=0\quad(\because Cauchy-Riemann)
 \end{equation}

으로 Cauchy's Integral Theorem이 증명됩니다.