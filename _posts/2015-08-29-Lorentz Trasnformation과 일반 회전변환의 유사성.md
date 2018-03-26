---
id: 356
title: Lorentz Trasnformation과 일반 회전변환의 유사성
date: 2015-08-29T16:59:40+00:00
author: Abraxas Academy
layout: post
tags: Physics
---
Lorentz Transformation은 어떤 관성계에 대해서 일정한 속도로 움직이는 다른 관성계로의 일종의 변환식이라고 할 수 있습니다. 그런데, 일반적인 유클리드 공간에서의 회전변환식을 거의 “끼워 맞추듯” 주물럭거리면, Lorentz Transformation이 튀어나옵니다.

문제의 간소화를 위해서 공간을 1차원으로 간소화시킵시다. 회전변환을 다음과 같이 쓰고,

$$\begin{pmatrix}x^\prime \\ w^\prime \end{pmatrix}=\begin{pmatrix} \cos \theta & -\sin \theta \\ \cos \theta & \sin \theta \end{pmatrix}\begin{pmatrix}x \\ w \end{pmatrix}$$

그리고 여기에 $w=ict$와 $\theta = i\psi$를 대입하고, $\cos i \psi = \cosh\psi$,  $-i\sin i \psi = \sinh\psi$를 이용하면 다음과 같이 바뀝니다.

$$\begin{pmatrix}x^\prime \\ ct^\prime \end{pmatrix}=\begin{pmatrix} \cosh \psi & \sinh \psi \\ \sinh \psi & \cosh \psi \end{pmatrix}\begin{pmatrix}x \\ ct \end{pmatrix}$$

 

$x^\prime$에 $0$을 대입하면,

 

$$x\cosh \psi =-ct\sinh \psi$$

 

따라서 

 

$$\frac{v}{c} = \beta =-\frac{\sinh \psi }{\cosh \psi }$$

이고, 또 

 

$$\cosh^2\psi-\sinh^2\psi = 1$$

를 이용하면

 

$$\cosh \psi = \frac{1}{\sqrt{1- \beta^{2}}} =\gamma,\quad \sinh\psi=-\beta\gamma$$

가 되어 아까 그 행렬은 

$$\begin{pmatrix}x^\prime \\ ct^\prime \end{pmatrix}=\begin{pmatrix} \gamma & -\beta\gamma \\ -\beta\gamma & \gamma \end{pmatrix}\begin{pmatrix}x \\ ct \end{pmatrix}$$

 

으로 Lorentz Transformation이 됩니다.