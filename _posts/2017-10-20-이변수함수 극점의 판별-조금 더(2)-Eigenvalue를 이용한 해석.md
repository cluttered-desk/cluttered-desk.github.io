---
id: 988
title: '이변수함수 극점의 판별-조금 더(2): Eigenvalue를 이용한 해석'
date: 2017-10-20T11:51:31+00:00
author: Abraxas Academy
layout: post
tags: Mathematics
---
바로 전의 포스트에서 이변수함수의 Hessian의 determinent와 x에 대한 2계 편도함수의 부호를 통해 어떤 critical point가 local minimum 혹은 local maximum을 가지게 되는지 살펴보았다. 이제 남은 경우인 $D<0$경우이다. 다루는 문제가 2차원인 만큼 사실 $\mathbf{h}=(r\cos\theta,r\sin\theta)$로 잘 지지고 볶아도 큰 문제 없을 듯 싶지만, 일반적인 경우로 확장할때 대략적인 그림을 그릴 수 있도록 선형대수의 지식을 좀 끌고오자. 만약 eigenvalue의 개념에 익숙하지 않은 사람은 [여기](https://en.wikipedia.org/wiki/Eigenvalues_and_eigenvectors)를 참고하자.

**Lemma 1. $2\times2$ matrix $A$가 $A^T=A$, 즉 symmetric matrix이면, $A$는 두개의 eignvalue $\lambda_1,\lambda_2 \in \mathbb{R}$을 가진다.**

증명: $$A=\begin{pmatrix}a&b\\b&c\end{pmatrix}$$라 하자. 그렇다면 $det(A-I\lambda)$를 만족하는 $\lambda$가 고유값이므로, $$det(A-I\lambda)=(a-\lambda)(c-\lambda)-b^2=\lambda^2-(a+c)\lambda+ac-b^2=0$$

에서, 이 이차방정식의 판별식이 $$(a+c)^2-4ac+b^2=(a-c)^2+b^2>0$$이므로 이 이차방정식이 두개의 실근을 가진다.

이제 주목해야 할 것은 이제껏 다뤄온 이변수함수의 Hessian $D$가 $f$가 $C^3$ class 함수라는 가정이 있으므로, Clairaut의 정리에 의하여 symmetric matrix라는 것이다. 이제 lemma 1에 의해 이변수함수의 Hessian이 두개의 eigenvalue를 가지며, $det(D)<0$이라는 조건까지 주어지면 $\lambda_1<0$, $\lambda_2>0$이라는 것 까지 알 수 있다. 그런데 이제 $$Hf(x,y)(\mathbf{h})=\frac{1}{2}(h_1,h_2)\begin{pmatrix}a&b\\b&c\end{pmatrix}\begin{pmatrix}h_1\\h_2\end{pmatrix}$$이므로, (a,b,c는 당연하지만 $f$의 partial derivatives 들이다. 쓰기 귀찮아서 그냥 썼다.) 만약 $\mathbf{h}$가 eigenvector라면 $Hf(x,y)(\mathbf{h})=\dfrac{1}{2}\lambda\lVert \mathbf{h}\lVert ^2$이 된다. 그렇다면 이 전 포스트와 마찬가지로,$ \displaystyle\lim_{\mathbf{h} \to 0} \frac{R_2(\mathbf{x_0},\mathbf{h})}{\lVert \mathbf{h}\lVert ^2}=0$이므로, $\epsilon \in \mathbb{R}^+$인 $\epsilon$에 대해 $\dfrac{R_2(\lvert \mathbf{x_0},\mathbf{h})}{\lVert \mathbf{h}\lVert ^2}\lvert <\epsilon$이면 $\lVert \mathbf{h}\lVert <\delta$인 $\delta \in \mathbb{R}^+$가 존재한다. $\epsilon=\lambda$이라 하면 $\lVert \mathbf{h}\lVert <\delta$일때, $$-\lambda<\dfrac{R_2(\mathbf{x_0},\mathbf{h})}{\lVert \mathbf{h}\lVert ^2}<\lambda$$이므로, $\lVert \mathbf{h}\lVert <\delta$이면

$$f(\mathbf{x_0}+\mathbf{h})-f(\mathbf{x_0})=\lVert \mathbf{h}\lVert ^2(\lambda+\frac{R_2(\mathbf{x_0},\mathbf{h})}{\lVert \mathbf{h}\lVert ^2})>0​$$이므로 이때 $f​$는 증가하며, 여기서는 $\lambda>0​$으로 가정하고 풀었으므로, $\epsilon​$에 $-\lambda​$를 넣고 풀게 되면 $f​$가 감소한다는 결론이 나온다. 즉, saddle point인 것이다.

몇가지 첨언한다면 symmetric matrix에서 eigenvalue $\lambda_1​$과 $\lambda_2​$에 대응하는 eigenvector는 수직이다. 힌트는 두 고유벡터의 내적 $\mathbf{u}\cdot\mathbf{v}=\mathbf{u}\mathbf{v}^T​$라는 점이다. 이를 이용하여 $\lambda_1\mathbf{u}\cdot\mathbf{v}=\lambda_2\mathbf{u}\cdot\mathbf{v}​$를 보인다면 $\lambda_1 \neq \lambda_2​$에서 수직임이 증명된다.

 

 