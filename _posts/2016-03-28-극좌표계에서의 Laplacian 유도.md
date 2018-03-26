---
id: 511
title: 극좌표계에서의 Laplacian 유도
date: 2016-03-28T11:37:25+00:00
author: Abraxas Academy
layout: post
tags: Mathematics
---
별 내용은 없고, Chain Rule을 이용한 굉장한 계산으로 뒤덮여 있습니다.

Chain rule은 다음과 같습니다.

 

 \begin{equation}
 \frac{dz}{dt}=\frac{\partial f}{\partial x}\frac{dx}{dt}+\frac{\partial f}{\partial y}\frac{dy}{dt}
 \end{equation}

직교좌표계에서의 Laplacian은 다음과 같습니다.

 

\begin{equation}\nabla^2=\frac{\partial^2}{\partial x^2}+\frac{\partial^2}{\partial y^2}\end{equation}

각 좌표계의 변수들 간에 다음이 성립하므로 

 \begin{equation}
 x=r\cos\theta,y=r\sin\theta
 \end{equation}

다음과 같습니다.

 

 

 \begin{equation}
 \frac{\partial z}{\partial r} =\frac{\partial z}{\partial x}\frac{\partial x}{\partial r}+\frac{\partial z}{\partial y}\frac{\partial y}{\partial r} =\frac{\partial z}{\partial x}\cos\theta+\frac{\partial z}{\partial y}\sin\theta
 \end{equation}

이계도함수를 구하면

 

 

 \begin{equation}
 \begin{split}
 \frac{\partial^2 z}{\partial r^2}&=\frac{\partial}{\partial r}\frac{\partial z}{\partial r}=\frac{\partial}{\partial r}\frac{\partial z}{\partial x}\cos\theta+\frac{\partial}{\partial r}\frac{\partial z}{\partial y}\sin\theta \\ &=\Big(\frac{\partial}{\partial x}\frac{\partial z}{\partial x}\frac{\partial x}{\partial r}+\frac{\partial}{\partial y}\frac{\partial z}{\partial x}\frac{\partial y}{\partial r}\Big)\cos\theta+\Big(\frac{\partial}{\partial y}\frac{\partial z}{\partial y}\frac{\partial y}{\partial r}+\frac{\partial}{\partial x}\frac{\partial z}{\partial y}\frac{\partial x}{\partial r}\Big)\sin\theta\\&=\cos^2\theta\frac{\partial^2 z}{\partial x^2}+\sin 2\theta\frac{\partial^2 z}{\partial x\partial y}+\sin^2\theta\frac{\partial^2 z}{\partial x^2}
 \end{split}
 \end{equation}

 

같은 방법으로 계산하면,

 

 

 

 \begin{equation}
 \begin{split}
 &\frac{\partial^2 z}{\partial \theta^2}=-r\Big(\frac{\partial z}{\partial x}\cos\theta+\frac{\partial z}{\partial y}\sin\theta\Big)+\\&r^2\Big(\sin^2\theta\frac{\partial^2 z}{\partial x^2}-\sin 2\theta\frac{\partial^2 z}{\partial x\partial y}+\cos^2\theta\frac{\partial^2 z}{\partial x^2}\Big)
 \end{split}
 \end{equation}

 

따라서 연립하면 다음을 얻습니다.

 

 

 

 \begin{equation}
 \nabla^2=\frac{\partial^2 z}{\partial x^2}+\frac{\partial^2 z}{\partial y^2}=\frac{\partial^2 z}{\partial r^2}+\frac{1}{r}\frac{\partial z}{\partial r}+\frac{1}{r^2}\frac{\partial^2 z}{\partial \theta^2}=\frac{1}{r}\frac{\partial}{\partial r}\Big(r\frac{\partial z}{\partial r}\Big)+\frac{1}{r^2}\frac{\partial^2 z}{\partial \theta^2}
 \end{equation}